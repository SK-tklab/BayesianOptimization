# BayesianOptimization
Bayesian Optimization with several acquisition functions

## Overview

### Probability of Improvement (PI)
Using the improvement probability for the current best function value.

paper:https://asmedigitalcollection.asme.org/fluidsengineering/article-abstract/86/1/97/392213

### Expected Improvement (EI)
Using the expected improvement for the current best function value.

paper:https://link.springer.com/content/pdf/10.1007/3-540-07165-2_55.pdf

### Lower Confidence Bound (LCB)
Using lower confidence bound.
In LCB, we need to set the exploitation-exploration trade-off parameter β^{1/2}.
I use β^{1/2}=1,4.

In GP-UCB,  β^{1/2} is determined according to iterations and in the following paper, it is shown that regret bounds are sublinear.

paper:https://arxiv.org/pdf/0912.3995

### Max value Entropy Search (MES)
Using mutual information with the optimal value.
I sampled the optimal values using sampling from the Gumbel distribution.

paper:https://arxiv.org/pdf/1703.01968
