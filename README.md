Welcome to the tutorial website for the package ``countsplit``
-----

For the main package website, please visit [https://anna-neufeld.github.io/countsplit/](https://anna-neufeld.github.io/countsplit/). 

The ``countsplit`` R package splits an integer-valued matrix into two or more folds of data that can be used for cross validation or for inference after latent variable estimation. If the entries in the original matrix follow a Poisson or a negative binomial distribution with known overdispersion parameter, then the folds of data will be independent and the inference or validation will be valid. The ability to handle negative binomial data and more than two folds of data is a new feature of the `countsplit` package; please read the new documentation carefully if you are an existing user.

The motivation for this method is described in Neufeld et al., 2022 [(link to paper)](http://arxiv.org/abs/2207.00554) in the context of inference after latent variable estimation for Poisson distributed single cell RNA sequencing data. Briefly, count splitting allows users to perform differential expression analysis to see which genes vary across estimated cell types (such as those obtained via clustering) or along an estimated cellular trajectory (pseudotime). Additional motivation, along with the extension to negative binomial data, is described in Neufeld et al., 2023 [(link to preprint)](https://arxiv.org/abs/2307.12985).

The tutorials on this website currently focus on the Poisson setting and on the inference after latent variable estimation setting, but they are being updated to include more negative binomial examples and more cross validation examples. 

This material is based upon research supported in part by the Office of Naval Research under Award Number N000142312589 and the National Science Foundation under Award Number 2322920.


How can I get countsplit?
-----

Make sure that ``remotes`` is installed by running ``install.packages("remotes")``, then type

```{r}
remotes::install_github("anna-neufeld/countsplit")
```

To also download the data needed to reproduce the package vignettes, be sure to also install the ``countsplit.tutorials" package.

```{r}
remotes::install_github("anna-neufeld/countsplit.tutorials"). 
```


Where can I learn more? 
-----

See the [introductory tutorial](articles/countsplit_tutorial.html) tab for an introduction to our framework on simple simulated data. This tutorial focuses on the setting where we wish to test genes for differential expression. See the [cross validation tutorial](articles/MSE_tutorial.html) for an additional introduction on simple simulated data, where the goal is instead to evaluate a given clustering model. See the [seurat](articles/seurat_tutorial.html),
[scran](articles/scran_tutorial.html), and [monocle3](articles/monocle3_tutorial.html) tutorials for examples of how the count splitting package can be integrated with common scRNA-seq analysis pipelines. 

Please see the [double dipping demonstration](articles/demonstrating_problem.html) for the code that goes with Appendix A of Neufeld et al., 2022. 

Please visit [https://github.com/anna-neufeld/countsplit_paper](https://github.com/anna-neufeld/countsplit_paper) for code to reproduce the figures and tables from Neufeld et al., 2022. Please visit [https://github.com/anna-neufeld/nbcs_paper_simulations](https://github.com/anna-neufeld/nbcs_paper_simulations) for code to reproduce the figures and tables from Neufeld et al., 2023. 


References 
----

Neufeld, A.,Gao, L., Popp, J., Battle, A. & Witten, D. (2022), ‘Inference after latent variable estimation for single-cell RNA sequencing data’, Biostatistics. 

Neufeld, A.,Dharamshi, A., Gao, L., & Witten, D. (2023), ‘Data thinning for convolution-closed distributions’, https://arxiv.org/abs/2301.07276/ . 

Neufeld, A., Popp, J., Gao, L., Battle, A. & Witten, D. (2023), ‘Negative binomial count splitting for single-cell RNA sequencing data'. https://arxiv.org/abs/2307.12985 . 





