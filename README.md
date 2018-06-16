# Heterogeneous Multi-output Gaussian Processes

This repository contains the implementation of our Heterogeneous Multi-output Gaussian Process model (HetMOGP). The entire code is written in Python and connected with the GPy package, specially useful for Gaussian Process models. Our code consists of two main blocks:

- **hetmogp**: This module contains all model definitions, inference, and important utilities.
- **likelihoods**: General library of probability distributions for the heterogeneous model.

If you want to include a new likelihood function, please add your new script here. We provide further details about usage below.

Please, if you use this code, cite the following paper:
```
@article{MorenoArtesAlvarez18,
  title={Heterogeneous Multi-output {G}aussian Process Prediction},
  author={Pablo Moreno-Mu\~noz, Antonio Art\'es-Rodríguez and Mauricio A. \'Alvarez},
  journal={arXiv preprint arXiv:1805.07633},
  year={2018}
}
```

## Usage

* Output and input data definition:
```
Y = [Y_hg, Y_ber, Y_cat]
X = [X_hg, X_ber, X_cat]
```
* Heterogeneous Likelihood definition:
```
likelihood_list = [HetGaussian(), Bernoulli(), Categorical(K=3)]
```
* Model and definition:
```
model = SVMOGP(X=X, Y=Y, Z=Z, kern_list=kern_list, likelihood=likelihood, Y_metadata=Y_metadata)
```

In notebooks>demo

* Missing Gap Prediction
![gap](tmp/gap.png)

* London House Prices
![london](tmp/london.png)

## Contributors

[Pablo Moreno-Muñoz!](http://www.tsc.uc3m.es/~pmoreno/), [Antonio Artés-Rodríguez!](http://www.tsc.uc3m.es/~antonio/) and [Mauricio A. Álvarez!](https://sites.google.com/site/maalvarezl/)

For further information or contact:
```
pmoreno@tsc.uc3m.es
```
