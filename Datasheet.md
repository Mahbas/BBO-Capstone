Datasheet for the BBO Capstone Project Data Set
Motivation
This data set was created to support a capstone project on black-box optimisation (BBO) under limited query budgets. The task it supports is the systematic evaluation of optimisation strategies—particularly Bayesian Optimisation—across a range of synthetic benchmark functions with varying dimensionality and characteristics. The data set enables reflection on exploration–exploitation trade-offs, surrogate model behaviour and practical decision-making under uncertainty. The primary motivation was not to build a predictive model, but to document and analyse the optimisation process itself, including successes, failures and manual interventions.
Composition
The data set consists of the query history and corresponding function evaluations collected across ten optimisation rounds for eight benchmark functions ranging from 2D to 8D. Each data point includes:
	Input vector X
	Scalar objective value y
	Function identifier
	Round index and iteration order
The data are stored in structured tabular form (CSV/notebook format). The data set is complete in terms of recorded queries but does not represent uniform coverage of the search space. Some regions are densely sampled due to exploitation, while others remain sparsely explored, particularly in higher dimensions.
Collection process
Queries were generated iteratively using Bayesian Optimisation strategies, primarily Gaussian Process surrogates with UCB and Expected Improvement acquisition functions. Additional strategies included manual exploration, duplicate avoidance and fallback sampling when acquisition functions stagnated. The data were collected over the duration of the capstone project, spanning ten rounds of optimisation. No random sampling was used beyond initialisation; query selection was adaptive and informed by previous outcomes.
Preprocessing and uses
Several preprocessing steps were applied, including output scaling and logarithmic transformations for functions with extreme dynamic ranges. No transformations were applied to the input space. The intended use of this data set is educational and methodological: analysing optimisation behaviour, comparing strategies and supporting reproducibility of optimisation decisions. Inappropriate uses include treating the data as a benchmark for supervised learning or assuming it represents ground-truth optima.
Distribution and maintenance
The data set is available locally alongside the capstone notebook and report. It is intended for academic use only. The author maintains the data set, with no planned future updates beyond documentation corrections.
