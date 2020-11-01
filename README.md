# BayesianOptimization
Bayesian Optimization with several acquisition functions.  
Plot these behavior.

## Overview
Bayesian Optimization (BO) is used in the optimization of black box functions with high observation costs.
In BO, black box function is estimated by a Bayesian model and the next observation point is determined by the acquisition function.
The balance between exploitation and exploration depends on the acquisition function.
I use following acquisition functions.

### Probability of Improvement (PI)
Using the improvement probability for the current best function value.

paper: [A new method of locating the maximum point of an arbitrary multipeak curve in the presence of noise.](https://asmedigitalcollection.asme.org/fluidsengineering/article-abstract/86/1/97/392213) (Journal of Fluids Engineering 1964)

### Expected Improvement (EI)
Using the expected improvement for the current best function value.

paper: [On Bayesian methods for seeking the extremum](https://link.springer.com/content/pdf/10.1007/3-540-07165-2_55.pdf) (IFIP Technical Conference 1974)

### Lower Confidence Bound (LCB)
Using lower confidence bound.
In LCB, we need to set the exploitation-exploration trade-off parameter β^{1/2}.
I use β^{1/2}=1,4.

In GP-UCB,  β^{1/2} is determined according to iterations and in the following paper, it is shown that regret bounds are sublinear.

paper: [Gaussian process optimization in the bandit setting: no regret and experimental design](https://arxiv.org/pdf/0912.3995) (ICML2010)

### Max-value Entropy Search (MES)
Using mutual information between the optimal value and function value at observation point .
I sampled the optimal values using sampling from the Gumbel distribution.
A method of sampling the optimal value using randam feature map is also proposed in the following paper.

paper: [Max-value entropy search for efficient Bayesian optimization](https://arxiv.org/pdf/1703.01968) (NeurIPS 2019)

## Plot
### PI
![iteration1](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/pi_1.png)![iteration2](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/pi_2.png)
![iteration3](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/pi_3.png)![iteration4](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/pi_4.png)


### EI
![iteration1](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/ei_1.png)![iteration2](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/ei_2.png)
![iteration3](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/ei_3.png)![iteration4](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/ei_4.png)


### LCB (β^{1/2} = 1)
![iteration1](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb1_1.png)![iteration2](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb1_2.png)
![iteration3](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb1_3.png)![iteration4](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb1_4.png)


### LCB (β^{1/2} = 4)
![iteration1](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb4_1.png)![iteration2](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb4_2.png)
![iteration3](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb4_3.png)![iteration4](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/lcb4_4.png)


### MES
![iteration1](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/mes_1.png)![iteration2](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/mes_2.png)
![iteration3](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/mes_3.png)![iteration4](https://github.com/SK-tklab/BayesianOptimization/blob/main/image/mes_4.png)
