---
layout: page
title: My School Projects!
---


## COMP551 Applied Machine Learning Projects 
McGill University (September 2022 - December 2022)

**Project 1: Getting Started with Machine Learning (Garde: A)**

The goal of this project is to build K Nearest Neighbour(KNN) and Decision Tree (DT) models on two health datasets and compare the model performance. The project report can be found [here](https://andrewcccc.github.io/assignment1_group_47.pdf).

* Implemented KNN feature selection function based on linear coefficient
* Contributed to the model  evaluation, such as AUROC, of the two models


**Project 2: Classification of Textual Data (Garde: A)**

The goal of this project was to build logistic regression and multiclass regression models and compare them to a KNN model on two textual datasets (IMDb and 20 Newsgroup). The project report can be found [here](https://andrewcccc.github.io/assignment2_group_47.pdf).
* Implemented LASSO feature selection functions
* Evaluated the logistic regression and multiclass regression models w.r.t KNN models 


**Project 3: Classification of Image Data (Garde: A)**

The goal of this project was to build a multilayer perceptron (MLP) and CNN model to classify image data. The project report can be found [here](https://andrewcccc.github.io/assignment3_group_47.pdf).

* Implemented CNN using Keras library 
* Contributed to the hyper-parameters fine-tuning of L2 regularization
* Investigated the effects of test accuracy using different network depth, width, and activation functions 




## ECE Capstone Project 
University of Alberta (September 2020 - May 2021) - (Garde: A)

**Problems:** Greenhouse operations in Alberta are often restricted in scale as a consequence of low-profit margins arising from high energy costs. Reducing these high costs through the incorporation of greenhouse technology could make greenhouse operations more feasible and common in Alberta. Since careful environmental control is required to ensure a crop’s quality and yield, growers are challenged to have enough knowledge to interpret the information provided by the monitoring system and adjust control setpoints accordingly.

**Objective:** The goal of this project is to address this need with the development of an integrated mini-production facility equipped with sensors, controllers and actuators that features both a monitoring-reporting system and an artificial intelligence- based control-decision-making system to optimize conditions for plant growth and the overall energy cost.

**Design**:
- Below shows the overall setup of the project design and the interaction point between the hardware and software
components. A temperature/humidity dual sensor within the tank enclosure feeds temperature and humidity values into
the central controller (Rasp Pi) while an infrared (IR) camera module takes and saves pictures of the KOM into the same device. An AC current sensor provides the controller with insight into the system power draw.
- At the controller side,object detection and analysis is first performed on the recently captured image to measure heights of individual KOM. A combination of historical and current readings of the system temperature and humidity will then be used by the controller to determine any responsive reactions that the heater and/or humidifier will undertake.
- All system parameters are saved within a database and accessible to the user through the use of an Android application.

![cachedImage](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/2d900b22-29db-4c77-9a34-b87bcfa448e4)


**Tasks:** I designed and developed an Android mobile application to retrieve current, humidity, temperature sensor data and mushroom images for monitoring the conditions of our mushrooms in the greenhouse. The project code for the app can be found [here](https://github.com/andrewcccc/Greenhouse).

The app was built in Android Studio programming in Java.

Highlights: 
* Used Retrofit API to retrieve JSON sensor data
* Used MPAndroidChart library to display graphical data
* Used Picasso library to retrieve image results

**How does Retrofit API work?**


Screenshots:

<table>
  <tr>
    <td>The numerical sensor data view</td>
     <td>The graphical data view</td>
     <td>The mushroom image view</td>
  </tr>
  <tr>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/dataviewcopy.JPG" width="300" height="600" /></td>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/grahpviewcopy.JPG" width="300" height="600" /></td>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/mushroomgrowthcopy.PNG" width="300" height="600" /></td>
  </tr>
 </table>

 **Final Product**
