# Restricted Boltzmann Machines for Collaborative Filtering

A well-known technique used mainly for designing recommender systems is collaborative filtering. In this project, we’ll use the RBM algorithm to recommand for a random user a set of specified movies.

### What is RBM 
**Note**: A detailed explanation on RBMs can be found on the artcile review in the (XX).

RBMs are two-layered artificial neural network with generative capabilities. They have the ability to learn a probability distribution over its set of input. RBMs were invented by Geoffrey Hinton and can be used for dimensionality reduction, classification, regression, collaborative filtering, feature learning and topic modeling.

RBMs are a special class of Boltzmann Machines and they are restricted in terms of the connections between the visible and the hidden units. As stated earlier, they are a two-layered neural network (one being the visible layer and the other one being the hidden layer) and these two layers are connected by a fully bipartite graph. This means that every node in the visible layer is connected to every node in the hidden layer but no two nodes in the same group are connected to each other. This restriction allows for more efficient training algorithms than are available for the general class of Boltzmann machines, in particular the gradient-based contrastive divergence algorithm.

A Boltzmann Machine             |  A Restricted Boltzmann Machine
:-------------------------:|:-------------------------:
<img src = "https://miro.medium.com/max/864/1*Ere0a83PN-Rj7DF5_IVZdg.png" width = "300">  |  <img src = "https://pathmind.com/images/wiki/multiple_inputs_RBM.png" width = "300">

# Why use RBMs for recommendation?

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

To get the env running, you'll need the following packaged installed


```
Pip3 install numpy
Pip3 install matplotlib
Pip3 install pandas
Pip3 install torch==1.3.1+cpu torchvision==0.4.2+cpu -f https://download.pytorch.org/whl/torch_stable.html
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

