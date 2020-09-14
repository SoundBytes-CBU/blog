Return [Home](index.md)

# Week of 9/7/20

This week, the team set out to complete the following tasks

- Updating the Weekly Log Sheet for Week 3.
- Interview the client to specify the project needs.
- Develop the Initial Problem Statement.
- Create questions to ask the client.
- Summarize information from the client interview.
- Research & Analysis of Algorithms.
- Updating the Blog for Week 3

## Client Interview & Summary

![Image from the Client Interview](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week3/meeting.jpg?raw=true)

On Friday, September 11, 2020 around 5pm, members of the team, specifically Rigoberto & Jacob met with Professor L. Clement, the client, to discuss the goals for the project and what is expected by the client & the CBU College of Engineering at the completion of the project.

This project, which can be found [here](project.md), focuses on the efficiency and the comparison of algorithms when given a particular challenge or task. In this project, the task is to detect and determine anomalies that can be detected on a public roadway or interstate based on the sounds. This can be, but is not limited too: Screeching Tires, Emergency Vehicle Sirens, Children/Pedestrians, etc.

The goal is to determine these anomalies quickly and efficiently. To do this, we intend to compare the same sounds and anomalies to multiple different AI/ML algorithms and determine how fast these systems can detect and respond to the anomaly and compare how they work with each specific anomaly.

## Initial Problem Statement

The team worked together throughout the week to create an Initial Problem Statement that we understand to be submitted with the SRS (Software Requirements Specification). The problem statement as given by the client: "A recent article in Wired magazine highlighted the computing demands of current AI and ML algorithms is so great that progress on tasks such as translation and autonomous vehicles is likely to slow."

This statement was understood as such by the team: "The AI and ML algorithms for autonomous vehicles require massive amounts of computational power that is currently not available. The current algorithms are not time efficient enough to be dependable in every situation. If progress is to continue in the realm of autonomous vehicles, a better understanding of the core attributes of these AI and ML algorithms must be analyzed and compared."

The Initial Problem Statement was added to the SRS and submitted on 9/13/2020.

![Image from the Client Interview](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week3/srs_2.jpg?raw=true)

## Research & Analysis of Algorithms

The research was conducted to determine the different algorithms we to research and potentially use in this 

![Learning Features for Subsequent Anomaly Measures vs Direct Learning of Anomaly Scores](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week3/anomaly_1.jpg?raw=true)
[View larger image](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week3/anomaly_1.jpg?raw=true)

Above is a visual representation of what is actually going on behind the scenes, when the anomaly is being discerned.  

In figure A above, the system requires some form of general data input, and once acquired, the system presents all of the calculated data with distinctions between normal and anomalies within the data, otherwise known according to the source as Learning Representations for Anomaly Detection.

In figure B above, this is a data chart displaying the End-To-End Differentiable Learning of Anomaly Scores found from the dataset. Figure A, with the original data as inputs, we directly learn and output the anomaly scores rather than the feature representations. Specifically, as shown in Figure B, given a training data object, the proposed framework first uses a neural anomaly score learner to assign it an anomaly score and then defines the mean of the anomaly scores of some normal data objects based on a prior probability to serve as a reference score for guiding the subsequent anomaly score learning. Lastly, the framework defines a loss function, called deviation loss, to enforce statistically significant deviations of the anomaly scores of anomalies from that of normal data objects in the upper tail.

![Learning Features for Subsequent Anomaly Measures vs Direct Learning of Anomaly Scores b](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week3/anomaly_2.jpg?raw=true)
[View larger image](https://github.com/SoundBytes-CBU/blog/blob/gh-pages/images/week3/anomaly_2.jpg?raw=true)

What is being introduced above is a novel framework that synthesizes neural networks, a prior probability distribution of anomaly scores, and a new loss function to train a deep anomaly detector in an end-to-end fashion, with an objective to assign statistically significantly larger anomaly scores to anomalies than normal objects. The resulting model is expected to yield more optimized anomaly scores and be more data-efficient than the two-step approach.. ϕ(x; Θ) is an anomaly score learner with the parameters Θ. µR is the mean of the anomaly scores of some normal objects, which is determined by a prior F . σR is a standard deviation associated with µR. The loss L ϕ(x; Θ), µR, σR is defined to guarantee that the anomaly scores of anomalies statistically significantly deviate from µR in the upper tail while enforcing normal objects have anomaly scores as close as possible to µR.

Works Cited: [*Deep Anomaly Detection with Deviation Networks (Pang, et. al.)*](http://arxiv-export-lb.library.cornell.edu/pdf/1911.08623)

## Updating the Blog for Week 3
The blog was updated to support this blog entry for the week of 9/7/20 through 9/13/20.

#### Update and Submitted by Timothy Roe, Jr. on 9/13/2020
#### Return [Home](index.md)


