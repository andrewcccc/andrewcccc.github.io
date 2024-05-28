---
layout: page
title: "Projects"
---

## COMP551 Applied Machine Learning Projects 
McGill University (September 2022 - December 2022)

**Project 1: Getting Started with Machine Learning (Garde: A)**

The goal of this project is to build K Nearest Neighbour(KNN) and Decision Tree (DT) models on two health datasets and comapre the model performance. The project report can be found [here](https://andrewcccc.github.io/assignment1_group_47.pdf).

* Implemented KNN feature selection function based on linear coefficient
* Contributed the model evulation, such as AUROC, of the two models


**Project 2: Classification of Textual Data (Garde: A)**

The goal of this project was to build logistic regression and multiclass regression models and compare them to a KNN model on two textual datasets (IMDb and 20 Newsgroup). The project report can be found [here](https://andrewcccc.github.io/assignment2_group_47.pdf).
* Implemented LASSO feature selection functions
* Evaluated the logistic regression and multiclass regression models w.r.t KNN models 


**Project 3: Classification of Image Data (Garde: A)**

The goal of this project was to build a multilayer perceptron (MLP) and CNN model to classify image data. The project report can be found [here](https://andrewcccc.github.io/assignment3_group_47.pdf).

* Implemented CNN using Keras library 
* Contributed to the hyper-parameters fine tuning of L2 regularization
* Investigated the effects of test accuracy using different network depth, width, and activation functions 




## ECE Capstone Project 
University of Alberta (September 2020 - May 2021)

Objective: The goal of this project is to address this need with the development of an integrated mini production facility equipped with sensors, controllers and actuators that features both a monitoring-reporting system and an artificial intelligence based control-decision-making system to optimize conditions for plant growth and the overall energy cost.

I designed and developed an Android mobile application to retrieve our sensor data and mushroom images for monitoring the conditions of our mushrooms in the greenhouse. The project code for the app can be found in [here](https://github.com/andrewcccc/Greenhouse).

The app was built in Andorid Studio programming in Java.

Hightlights: 
* Used Retrofit API to retrieve JSON sensor data
* Used MPAndroidChart librsry to display graphical data
* Used Picasso library to retrieve image results


Screenshots:

<table>
  <tr>
    <td>The numerical sensor data view</td>
     <td>The grpahical data view</td>
     <td>The mushroom image view</td>
  </tr>
  <tr>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/dataviewcopy.JPG" width="300" height="600" /></td>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/grahpviewcopy.JPG" width="300" height="600" /></td>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/mushroomgrowthcopy.PNG" width="300" height="600" /></td>
  </tr>
 </table>

## Apple's Facial Movement Tracking (Co-op) Project 
University of Alberta (January 2020 - August 2020)

**Project background:** 
- 3D face tracking is a clinical tool which can provide significant information on facial, jaw, and lip motions. 
- The analysis of facial, jaw, and lip movements can be used as an early indicator of neurological diseases, such as Parkinson’s and amyotrophic lateral sclerosis(ALS).
- Pervious works have also shown that the video-based analysis can help early diagnosis and disease progression in patents with ALS.


**Problems:** Some commercial tracking systems, such as Optotrak, are used in clinical research to capture facial motion. These tracking systems are expensive, and the tracking procedure can be time consuming. These tracking systems have limited availability because they cannot provide remote tracking applications, such as speech therapy and linguistic data gathering.

**Objective:** develop a novel mobile application to provide a full-face tracking system during speech production.

**Design**:

- It is developed in Xcode and is available on iOS devices with TrueDepth camera.  

- The development of this mobile application uses ARKit,  Apple’s augmented reality platform, and the iPhone’s front facing TrueDepth camera. 

- The mobile application projects an array of infrared dots onto the user’s face and create a geometry face mesh with 1220 verticies, at 60 frames per second (FPS). 

- The tracking method is marker-less (i.e. no attached sensors).  

Tools: Xcode, an iOS device with TrueDepth camera, and ARKit (Apple’s augmented reality platform).

Ideas: The tracking coordinate system is right-handed: 
- the positive x direct points to the viewer’s right,
- the positive y direction points to the viewer’s up, 
- the positive z direction points toward the viewer,
- The collected data is the positional changes corresponding to the change of the verticies on the face mesh. The units of face coordinate are in meters. The projected face mesh moves in real time corresponding to the user’s face movement.

 
![image](https://user-images.githubusercontent.com/61716028/210809986-993a6781-9541-4669-be6c-7cfa7469d852.png) [Reference:  Apple’s documentation: ARKit and ARFaceAnchor]

<table>
  <tr>
    <th> ![image](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/e0bc94e3-55ad-48c5-8327-ace69896b9de) </th>
    <td> 
            <ul>
        <li>The projected face mesh moves in real time corresponding to the user’s face movement.</li>
        <li> It captures both video (60fps) and audio (44.1kHz) recordings during the speech task. </li>
        <li> The bottom part of the screen contains 3 control buttons: 1. Start 2. Change 3. Stop
          1. Start button: Start capturing the video and audio of the experiment 
          2. Change button: Allows the user to read the target sentence at their own pace and change to the next sentence 
          3. Stop button: Stop recording the video and audio and save the position data and recordings locally on the device. </li>
      </ul>


</td>
  </tr>
</table>





A demo: 

<!-- ![ezgif com-gif-maker](https://user-images.githubusercontent.com/61716028/212986866-659ec9e0-a98e-4842-9d23-e34cc201ba2e.gif) -->

<img src="https://user-images.githubusercontent.com/61716028/212986866-659ec9e0-a98e-4842-9d23-e34cc201ba2e.gif" width="350" height="500"/>
