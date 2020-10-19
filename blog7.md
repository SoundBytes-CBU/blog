# Week of 10/12/20 - 10/18/20 (Week 8)

This week, the team set out to complete the following tasks:

- Complete SRS 4 - Requirements Specification
- Complete SRS 4.1 - Agile Overview
- Complete SRS 4.1 - System Architecture
- Complete SRS 4.2.2 - Software Specification
- Complete SRS 4.6 - Algorithm Specification

## Requirements Specification (SRS 4)

## Agile Overview (SRS 4.1)

![Agile Methodoloy](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week7/agile.jpg?raw=true)

The team has decided to adopt the Agile Methodoloy when developing. The team intends to begin one-week sprints at the start of the week, and continue to meet, discuss, and plan the next course of action. Due to the impact of COVID-19, the team intends to meet over a Voice over IP Platform, in this case Discord. All audible and video conferencing will take place through Discord. The team will begin each week discussing the previous tasks and the upcoming tasks for the week. The team will then divide into small sub-teams and work in parallel, one focused on implenetation of the tasks of a specific sprint, and the other sub-team being more researched focus based. This will allow of quicker development and quicker understanding and foreknowledge when it comes to developing come time. Each team and individual is held to their set measureable goals at the start of the week and is expected to report when their goals can not be met for some reason.

## Implementation Plan (Iteration One)

The team has started implementation this week and have decided to to host their repository publicly on [GitHub](https://github.com/egr-401-402-capstone-2020-21/Soundbytes_Implementation). The team has a few branches already up and running including a `main` branch and a `Documentation` branch. The `Documentation` will be used specifically only for the building of documentation. While the `main` branch will only host functioning code. The team has also setup some branch rules that apply to both `main` and `Documentation`. The rules enforce code reviews for every contributor when merging into that branch.  

![Github Repository](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week7/image1.jpg?raw=true)

![IDE Version Control](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week7/image2.jpg?raw=true)

As the `Documentation` branch indicates the team will iteratively be adding documentation during each iteration. The team is currently using ReadTheDocs to host public documentation as the project develops. The current documentation build can be seen [here](https://soundbytes.readthedocs.io/en/latest/?badge=latest). There is currently only one entry under the API section of the documentation, the ModelWrapper class and package. However, as the team updates the GitHub repository the documentation on ReadTheDocs will also update to reflect the current status of the repository. The team is using a software package called Sphinx to generate the documentation based off of the documentation the team provides in their source code.

![Documentation Home Page](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week7/docs.jpg?raw=true)

### System Architecture (SRS 4.2.1)

#### model_wrapper.py

The ModelWrapper that is being developed will allow the team to experiment with the parameters and conditions that have been recordered and allow them to be passed into a model. This model will utilized a KVPair and will be able to quickly and efficiently "score" a given dataset. 

#### Research

![Research 1](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week7/ai1.png?raw=true)

For the research sub-team this week, they focused on analyzing a couple of different areas. It consists of models, concepts, and relevant software libraries. For the models, the ones that were recognized for this week were Generative Adversarial Networks (GANs). The concepts that were identified composed of the contrast between Artificial Intelligence (AI), Machine Learning (ML), and Deep Learning (DL). Finally, some relevant software libraries that were looked into were pytorch and tensorflow. Beginning with the contrast, typically when beginning with the field of research with AI, there can be quite a bit of confusion and overlap between what exactly AI and ML are. Artificial Intelligence is a study, it’s a science. It is the study of methods to build intelligent programs and machines that can creatively solve problems, which has always been considered a human prerogative. Machine Learning is a subset of AI that provides systems the ability to learn and improve in automated sequences simply from experience and does not need to be explicitly programmed. In ML, there are different algorithms (e.g. neural networks) that help to solve problems. Finally, there is DL, a subset of machine learning, which uses the neural networks to analyze different factors with a structure that is similar to the human neural system. These are very powerful tools that are used in thousands of software applications today.

![PyTorch Logo](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week7/pytorch.jpg?raw=true)
[PyTorch](https://pytorch.org/)

![TensorFlow Logo](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week7/tf.png?raw=true)
[TensorFlow](https://www.tensorflow.org/)

For the relevant software libraries, pytorch and tensorflow were the most established and used for many machine learning models. PyTorch is an open source machine learning library based on the Torch library, used for applications such as computer vision and natural language processing, primarily developed by Facebook's AI Research lab. It is free and open-source software released under the Modified BSD license. Wikipedia TensorFlow is a free and open-source software library for dataflow and differentiable programming across a range of tasks. It is a symbolic math library and is also used for machine learning applications such as neural networks. These software libraries specialize in programming machine learning models and have been widely used.

### Software Specification (SRS 4.2.2)

#### model_wrapper.py (SRS 4.2.2.1)

The wrapper operates by few constraints and can be started by an user with any set of permissions. 

![Model Wrapper Constructor](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week7/image3.jpg?raw=true)

As referenced in the image above. The wrapper takes in a constraint of "model_class" defining the type of model. A constraint of dataset, or the dataset that will be passed to the model. A constraint of train_percent, or a float of how far the execution of training the model should go. A constraint of test_percentage, or how much of the dataset should be tests, and a random_state integer input.

#### Research

For the model portion of the research, a suggestion by one of the technical advisors was to look into GANs. These models are categorized as deep-learning-based, generative type of models. Generally speaking, GANs are a model architecture for training a generative model. GANs, however, are trained to describe how a dataset is generated in terms of a probabilistic model. By sampling from a generative model, you’re able to generate new data. While discriminative models are used for supervised learning, generative models are often used with unlabeled datasets and can be seen as a form of unsupervised learning. To output new samples, generative models usually consider a stochastic, or random, element that influences the samples generated by the model. The random samples used to drive the generator are obtained from a latent space in which the vectors represent a kind of compressed form of the generated samples. generative models learn the probability P(x) of the input data x, and by having the distribution of the input data, they’re able to generate new data instances.

![Basic Overview of a GAN Model](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week7/figure21.png?raw=true)

The image above shows the basic idea of a generative model, where there are training samples and random data being used in the input and, it generates sample data based on what the model “learned”. 

![More Sophisticated Example](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week7/figure22.png?raw=true)

The image above shows a more complex example with sample graphs and functions.

### Component Specification (SRS 4.2.4)

The model_wrapper.py will contain multiple components and functions to allow the user to train a certain dataset to their liking. The dataset will be able to be broken up for fast processing. The dataset will utilize a KVPair component which is composed of a key and a value. These components are intended to be used for easy data manipulation and processing when handling mass amounts of data.

### Data Specification (SRS 4.2.5)

The data structure that is being used throughout the system is a custom KVPair that is designed for easy data manipulation. It stores a dictionary, much like a NSDictionary in Objective-C or a HashMap in Java however it is easily modifable and not a read only variable that must be copied if it needs to be mutable.

### Algorithm Specification (SRS 4.2.6)

The sorting algorithm is from a built in package from Python. The module will analyze the dataset and sort data accordingly. The algorithm is a hybrid model of a sort and a merge algorithm. The hybrid model is intended to save time.

#### Updated and Submitted by Timothy Roe, Jr. on 10/18/2020
#### Return [Home](index.md)