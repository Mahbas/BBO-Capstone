Model Card for the BBO Optimisation Approach
Overview
Model name: Adaptive Bayesian Optimisation Strategy

Type: Sequential black-box optimisation

Version: Capstone implementation (Round 10)

This approach combines Gaussian Process surrogates with adaptive acquisition strategies and human-in-the-loop decision-making.
Intended use
The approach is suitable for:
•	Low- to medium-budget black-box optimisation
•	Educational analysis of optimisation behaviour
•	Benchmark function experimentation
It should not be used as a fully automated optimiser in safety-critical or real-time systems.
Strategy and evolution
Across ten rounds, the strategy evolved from broad exploration using UCB to increasingly selective exploitation using EI. Early rounds prioritised mapping uncertainty, while later rounds focused on stabilising improvements. Neural network and SVM surrogates were explored but largely abandoned due to instability under limited data. Manual interventions were introduced when acquisition functions repeatedly suggested identical queries or stalled, reflecting informed critique rather than blind automation.
Performance
Performance was evaluated using best-so-far objective values and convergence behaviour across eight functions. Improvements were strongest in low-dimensional settings, while gains diminished with increasing dimensionality. No formal regret bounds were computed; evaluation focused on relative improvement under fixed query budgets.
Assumptions and limitations
The approach assumes smoothness and stationarity of objective functions, making GP surrogates appropriate. It also assumes that late-stage exploitation is preferable to continued exploration. Limitations include sampling bias, lack of formal strategy comparison and reduced generalisability to noisy or highly non-stationary functions.
Ethical considerations and transparency
Transparency is supported through detailed logging of decisions, transformations and strategy changes. This documentation enables reproducibility, critical review and adaptation by other researchers. While not designed for deployment, the approach demonstrates how explicit reasoning and documentation reduce the risk of opaque or misleading optimisation outcomes.
Overall, the current model card provides sufficient detail to understand and reproduce the approach. Additional complexity would risk obscuring the central methodological lessons rather than improving clarity.

