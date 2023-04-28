# Reducing the Noise: A Deep Dive into Dimensionality Reduction Methods

## What is Dimensionality Reduction?
We are generating a tremendous amount of data daily. In fact, 90% of the data in the world has been generated in the last 3–4 years! The numbers are truly mind-boggling. Below are just some of the examples of the kind of data being collected:
- Facebook collects data about what we like, share, post, visit places, and like restaurants.
- Smartphone apps collect a lot of personal information about us
- Amazon collects data on what we buy, view, click, etc. on their site
- Casinos keep track of every move each customer makes

The abundance of data in current datasets is a challenge for researchers, as it requires the development of clever algorithms to extract important information effectively. Here the curse of dimensionality comes into the picture; this phenomenon occurs in data analysis when dealing with high-dimensional data. In high-dimensional spaces, the data becomes more sparse and the distances between points become more similar, making distinguishing between different classes or patterns difficult.

## The Data Analyst's Dilemma: The Curse of Dimensionality
The curse of dimensionality is a challenging problem that arises when dealing with high-dimensional data in data analysis.
- High-dimensional data: When dealing with data that has a large number of features or dimensions, it is considered high-dimensional. For example, an image can have thousands or even millions of pixels, and each pixel is considered a feature or dimension. Similarly, text data can have a large number of words or terms, each of which is a feature.
- Sparse data: In high-dimensional spaces, the amount of data required to fill the space increases exponentially with the number of dimensions. As a result, the data becomes sparse, meaning that there are fewer data points per unit volume. This makes it harder to estimate the underlying distribution of the data accurately.
- Increased complexity: With high-dimensional data, the number of possible interactions between features increases, leading to an exponential growth in the complexity of the data. This can make it challenging to develop accurate models or algorithms to analyze the data effectively.
- Increased computation: Dealing with high-dimensional data can require a lot of computational resources, as more complex models or algorithms are needed to analyze the data accurately. This can lead to longer processing times, increased memory requirements, and higher computational costs.

## Main Approaches for Dimensionality Reduction
- Projection: Projecting high dimensional data on a low dimensional hyperplane, minimizing the variance. (PCA)
- Manifold Learning: In many cases where the subspace may twist and turn(Swiss roll), projection is not the best approach to dimensionality reduction. Manifold Learning techniques measure how each training instance linearly relates to its closest neighbors, then it looks for a low-dimensional representation of the training set where these local relationships are best preserved. (T-SNE)

This article aims to provide an introductory exposition on the following 3 methods as well as to portray their visualizations.
1. Principal Component Analysis ( PCA ) - Unsupervised, linear method, Projection 
2. Linear Discriminant Analysis (LDA) - Supervised, linear method 
3. t-distributed Stochastic Neighbor Embedding (t-SNE) - Nonlinear, probabilistic method, manifold learning

The dataset we will be using for exploration is MNIST Digital Digits dataset.
