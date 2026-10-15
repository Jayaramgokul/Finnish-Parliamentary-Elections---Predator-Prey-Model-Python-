# Finnish elections as a predator-prey system

Can a model built for foxes and rabbits describe voters? This project treats
Finnish parliamentary elections from 1954 to 1983 as a **Lotka-Volterra
predator-prey system**: the communist-led SKDL alliance as the "predator" and
all other parties combined as the "prey", following Durand and Durand (1992).

## The model

$$\frac{dP}{dt} = 0.6\,P - 0.0013\,PS \qquad \frac{dS}{dt} = -0.39\,S + 0.00022\,SP$$

*P* = votes for all other parties, *S* = votes for SKDL (thousands), starting
from the 1954 result (*P* = 1,575, *S* = 433). The system is solved
numerically with an explicit Euler scheme over 10,000 time steps.

## What it shows

- **Both vote series cycle**, as predator-prey theory predicts. SKDL's cycle is
  roughly 12.5 years with an amplitude of about 55,000 votes; the other
  parties' cycle is roughly 14 years with an amplitude of about 275,000.
- The **phase-plane plot** shows trajectories orbiting the equilibrium point,
  rather than settling on it.
- A two-equation model captures the *shape* of the interaction; real
  elections have many drivers it leaves out, so it is a lens, not a forecast.

## Files

| File | Contents |
|---|---|
| `Finnish Parliamentary- Predator Prey.ipynb` | Model, numerical solution, component and phase-plane plots |
| `Predator Prey Model Report.pdf` | Write-up: background, derivation, results and interpretation |

Data: Durand, J. and Durand, R. (1992), *Fitting and testing a "predator-prey"
model*. Built in Python with NumPy and Matplotlib (2020).
