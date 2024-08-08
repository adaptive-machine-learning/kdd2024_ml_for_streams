# Practical Machine Learning for Streaming Data
## KDD 2024 Hands-on Tutorial, Barcelona (Spain). 

ID: HO-1
Date and Time: Monday, August 26, 10:00 AM – 1:00 PM


## Introduction
Machine Learning for Data Streams has been an important area of research since the late 1990s, and its usage in industry has grown significantly over the last few years. However, there is still a gap between the cutting-edge research and the tools that are readily available, which makes it challenging for practitioners, including experienced data scientists, to implement and evaluate these methods in this complex domain.
Our tutorial aims to bridge this gap with a dual focus. We will discuss important research topics, such as partially delayed labeled streams, while providing practical demonstrations of their implementation and assessment using CapyMOA, an open-source library that provides efficient algorithms implementations through a high-level Python API. Source code is available in [https://github.com/adaptive-machine-learning/CapyMOA](https://github.com/adaptive-machine-learning/CapyMOA) while the accompanying tutorials and installation guide are available in [https://capymoa.org/](https://capymoa.org/).

## Tutorial Overview
In this tutorial, our aim is to familiarize participants with the application of various machine-learning tasks to streaming data. Alongside providing an introductory overview outlining the typical supervised learning cycle (classification and regression), we direct our attention to challenges such as:


* **Prediction Intervals** for regression tasks
* **Concept drift** detection, visualization and evaluation
* Modelling and addressing **partially and delayed labeled data streams** using semi-supervised learning
* Applying and analysing **clustering** and **anomaly detection** algorithms on streaming data


# Tools and programming language

The tutorial is divided into three parts. Each part will be illustrated through Python examples, even though we will discuss Java implementations the attendees are not expected to have any knowledge of Java. Our objective is for attendees to exit the tutorial equipped with the ability to utilize all the algorithms introduced and possess a clear comprehension of their practical functioning. To facilitate this understanding, we have streamlined the presentation to feature key algorithms per task, thus allowing us to delve beyond theoretical aspects and concentrate on the practical aspects. 
The following tools will be used during the tutorial: 

* **MOA {Massive Online Analysis} framework**[1]. MOA is a machine learning framework tailored for data streams, boasting an extensive library of algorithms for a variety of tasks. MOA's implementation in Java poses a significant challenge for many newcomers due to its complexity. 
* **CapyMOA** ([https://capymoa.org/](https://capymoa.org/)). CapyMOA is a new open-source project offering a high-level Python API for stream learning algorithms. Its primary advantage lies in the accessibility of Python-based API, providing both efficiency and flexibility. 


To streamline the setup process, attendees can **follow the instructions to install CapyMOA [here](https://capymoa.org/installation.html)


## Tutorial Outline

* Supervised learning (Classification and Regression)
* Concept drift (Detection, Simulation and Evaluation)
* Unsupervised learning (Clustering) and Anomaly Detection 
* Partially and delayed labeled data (Semi-supervised learning)


### Supervised Learning

We will introduce through examples the supervised setting for data stream classification and regression. This includes evaluation procedures, the learning cycle, and algorithms. 
Additionally, we will illustrate how prediction intervals can augment the interpretability and confidence of streaming regression algorithms. The key algorithms discussed in this part will include Hoeffding Trees~\cite{domingos2000mining}, PLASTIC~\cite{heyden2024leveraging}, Streaming Gradient Boosted Trees (SGBT)~\cite{SGBT}, Self-Optimising K-Nearest Leaves (SOKNL)~\cite{sun2022soknl} and ADAptive Prediction Interval (ADAPI)~\cite{sun2024adapi}. 

## Concept Drift

We will discuss concept drift detection, showcasing methods for visualization, and evaluation. Departing from the conventional approach of regarding drift detectors solely as a component of adaptive learning algorithms, we will also showcase their utility in assessing the degradation of traditional machine learning pipelines, and how they can be evaluated. The key algorithms discussed include the Adaptive Windowing algorithm~\cite{ADWIN} and STUDD~\cite{cerqueira2023studd}. 

## Unsupervised learning and Anomaly Detection
In this section, we will address the challenges related to clustering and anomaly detection in a streaming context. For clustering, we will delve into the concepts of microclusters, providing practical examples of algorithm execution, visualization, and evaluation. For anomaly detection, we will cover both classic and recent algorithms, discussing their challenges and evaluation procedures.
The key algorithms discussed include CluStream~\cite{aggarwal2003framework}, StreamKM++~\cite{ackermann2012streamkm}, Half-Space Trees~\cite{tan2011fast} and Online Isolation Forest~\cite{Leveni2024}. 

## Partially and delayed labeled data
Finally, we will delve into the exploration of methods designed to tackle the complexities of partially and delayed labeled data in streaming environments. 
We will bridge the gap between theory and how that can be translated into code, for example, the different scenarios shown in a recent survey~\cite{gomes2022survey}. 
Moreover, we will illustrate how evaluation can be conducted in such settings, where labeling ratios and delays may vary. We will use the basic algorithms cluster-and-label and incremental self-training~\cite{le2019semi} to illustrate the scenario. 


## Presenters' biography

**Heitor Murilo Gomes** is a senior lecturer at the Victoria University of Wellington (VuW) in New Zealand. Before joining VuW, Heitor was a senior research fellow and co-director of the AI Institute at the University of Waikato were he taught from 2020 to 2022 the ``Data stream mining'' course. His main research area is the application of machine learning for data streams in a variety of tasks. 
In his field, he has introduced innovative approaches to ensemble learning, particularly focusing on regression and classification tasks. His research has also delved into unsupervised drift detection, clustering methods and the intersection of online continual learning and data streams. Additionally, he has authored several survey papers.
In 2023, he received a Marsden Grant from the New Zealand government to conduct fundamental research on novel theories and algorithms for partially delayed labeled streams.
Furthermore, Heitor has contributed to several open-source projects like MOA (Massive Online Analysis) and recently lead the development of CapyMOA ([https://capymoa.org/](https://capymoa.org/)), a python library for efficient stream learning. 

Website: [http://www.heitorgomes.com](http://www.heitorgomes.com)

Professor **Albert Bifet** is the Director of the Te Ipu o te Mahara AI Institute at the University of Waikato and Co-chair of the Artificial Intelligence Researchers Association (AIRA). His research focuses on Artificial Intelligence, Big Data Science, and Machine Learning for Data Streams. He is leading the TAIAO Environmental Data Science project and co-leading the open source projects MOA (Massive On-line Analysis), StreamDM for Spark Streaming and SAMOA (Scalable Advanced Massive Online Analysis). He is the co-author of a book on Machine Learning from Data Streams published at MIT Press. He is one of the winners of the best paper award at the ACM Conference on Fairness, Accountability, and Transparency (ACM FAccT) 2023, and he will be the general co-chair of the European Conference on Machine Learning and Principles and Practice of Knowledge Discovery in Databases (ECML-PKDD) 2024.

Website: [https://albertbifet.com/](https://albertbifet.com/)



## References

[1] Albert Bifet, Ricard Gavalda, Geoffrey Holmes, and Bernhard Pfahringer. 2017.
Machine learning for data streams: with practical examples in MOA. MIT press.