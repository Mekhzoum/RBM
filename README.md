# Restricted Boltzmann Machines for Collaborative Filtering

A well-known technique used mainly for designing recommender systems is collaborative filtering. In this project, we’ll use the RBM algorithm to recommand for a random user a set of specified movies.

The implementation done was based on the article: https://www.cs.toronto.edu/~rsalakhu/papers/rbmcf.pdf

### What is RBM 
**Note**: A detailed explanation on RBMs for recommander systems can be found on the artcile review in (https://drive.google.com/file/d/1NLcUYhBUaEddT653zRbaUC_ddNuSPpzT/view).
This article review was done by: 

**Mekhzoum Hamza**

**BOUSSOUF Omar**

**HAMAMA Krimo**

RBMs are two-layered artificial neural network with generative capabilities. They have the ability to learn a probability distribution over its set of input. RBMs were invented by Geoffrey Hinton and can be used for dimensionality reduction, classification, regression, collaborative filtering, feature learning and topic modeling.

RBMs are a special class of Boltzmann Machines and they are restricted in terms of the connections between the visible and the hidden units. As stated earlier, they are a two-layered neural network (one being the visible layer and the other one being the hidden layer) and these two layers are connected by a fully bipartite graph. This means that every node in the visible layer is connected to every node in the hidden layer but no two nodes in the same group are connected to each other. This restriction allows for more efficient training algorithms than are available for the general class of Boltzmann machines, in particular the gradient-based contrastive divergence algorithm.

A Boltzmann Machine             |  A Restricted Boltzmann Machine
:-------------------------:|:-------------------------:
<img src = "https://miro.medium.com/max/864/1*Ere0a83PN-Rj7DF5_IVZdg.png" width = "300">  |  <img src = "https://pathmind.com/images/wiki/multiple_inputs_RBM.png" width = "300">

### Why use RBMs for recommendation?

RBMs are unsupervised learning algorithms which try to **reconstruct** user input and in order to achieve this, they try to learn patterns from the examples in our data. This is then used to create a lower-dimensional representation of the pattern which can later be used to reconstruct approximations of the original input. Their ability to do this makes them a good fit for our problem because we need the algorithm to identify a pattern (the reading taste of a user) from the input and reconstruct it in the form of a score for each book (a rating essentially). This ultimately would help us in providing recommendations to that user based on the reconstructed scores.

<center><img src = "https://miro.medium.com/max/2560/1*jaAbI77jDbLJcxaqS4t2BA.jpeg" width = "500"></center>


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

### Prerequisites

To run the program, you'll need:

```
Python version 3.7.3
Jupyter notebook
```

### Dataset
The Dataset used can be found in : https://grouplens.org/datasets/movielens/1m/

Inside, there're 1,000,209 anonymous ratings of approximately 3,900 movies made by 6,040 MovieLens users 
who joined MovieLens in 2000.

### Installing

<img src = "https://img.shields.io/badge/requirements-compatible-blue.svg">

- Python 3.6 and above
- Pytorch
- NumPy
- Pandas
- Matplotlib

### Results
#### Training Error Graph
This graph was obtained on training the data for 50 epochs with a mini-batch size of 100:
<img src = "https://i.ibb.co/pWnT1vS/Plot.png">

#### Recommendation for a random user
As shown in the results, the algorithm ran smoothly and performed good recommendations for the random user, specifying a set of movies never seen by the random user, according to the collaborative filtering that we performed. For example, the user already saw the 4th movie. Thus, the system recommended that movie with a percentage of 100%, also the random user tends to watch drama and comedy movies a lot, and as seen in the results, the algorithm recommended similar genres of films, which means that the algorithm was well performed.
<img src ="https://i.ibb.co/txLMM56/reco.png">

## Built With

* [Python](https://www.python.org/) - The language used
* [Pytorch](https://pytorch.org/) - Deep learning package used 

## References
- Inspired from the idea presented in paper [Salakhutdinov, R., Mnih, A., & Hinton, G. (2007, June). Restricted Boltzmann machines for collaborative filtering](http://www.cs.utoronto.ca/~hinton/absps/netflixICML.pdf)
- Additional Notes used for understanding
  - [Gibbs Sampling (MCMC)](https://bayes.wustl.edu/Manual/RadfordNeal.review.pdf)
  - [Contrastive Divergence learning](https://www.cs.toronto.edu/~hinton/absps/cdmiguel.pdf)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
