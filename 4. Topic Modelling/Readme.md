# Latent Dirichlet Allocation

## Overview
latent Dirichlet allocation (LDA), a generative probabilistic model for collections of discrete data such as text corpora. LDA is a three-level hierarchical Bayesian model, in which each item of a collection is modeled as a finite mixture over an underlying set of topics

## Bag-of-words v/s LDA

Consider the below BOW model where we have documents *d*, topics *t* and probability that given the document *d*, the word is *t* as `P(t|d)`. Now if we compute the number of parameters in this model (C-BOW), we get **500 times 1000 = 500,000 parameters.**<br><br>

<img src="./images/1. C-BOW.png" height="200"></img>

This is too many parameters to figure out. Another way to appraoch this problem is by adding a notion of small set of *topics or latent variables* to our model. So in the above example, every document is associated with underlying mixture of topics. In the refactored example below, we see 2 sets of probabilities :<br>

1. Probability of a particular topic *z*, given the document *d* : `P(z|d)`
2. Probability of a particular term *t*, given the topix *z* : `P(t|z)`

The final probability of a term given a document (`P(t|d)`) will be the sum of above mentioned probabilities.

<img src="./images/2. Latent Variables.png" height="200"></img>

Now using LDA, the number of parameters will be **(500 (documents) times 10 (topics) = 5000) + (10 (topics) times 1000 (terms)) = 15,000 parameters** which is significantly less than C-BOW.
