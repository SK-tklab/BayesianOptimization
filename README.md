# BayesianOptimization
Bayesian Optimization with several acquisition functions

## Overview
Bayesian Optimization (BO) is used in the optimization of black box functions with high observation costs.
In BO, black box function is estimated by a Bayesian model and the next observation point is determined by the acquisition function.
The balance between exploitation and exploration depends on the acquisition function.
I use following acquisition functions.

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

### Maxvalue Entropy Search (MES)
Using mutual information with the optimal value.
I sampled the optimal values using sampling from the Gumbel distribution.
A method of sampling the optimal value using randam feature map is also proposed in the following paper.

paper:https://arxiv.org/pdf/1703.01968

## Plot
### PI
![iteration1](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/pi_1.png)
![iteration2](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/pi_2.png)
![iteration3](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/pi_3.png)
![iteration4](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/pi_4.png)


### EI
![iteration1](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/ei_1.png)
![iteration2](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/ei_2.png)
![iteration3](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/ei_3.png)
![iteration4](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/ei_4.png)


### LCB (β^{1/2} = 1)
![iteration1](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb1_1.png)
![iteration2](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb1_2.png)
![iteration3](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb1_3.png)
![iteration4](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb1_4.png)


### LCB (β^{1/2} = 4)
![iteration1](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb4_1.png)
![iteration2](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb4_2.png)
![iteration3](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb4_3.png)
![iteration4](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb4_4.png)


### MES
![iteration1](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/mes_1.png)
![iteration2](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/mes_2.png)
![iteration3](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/mes_3.png)
![iteration4](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/mes_4.png)
