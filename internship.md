---
layout: page
title:  My internships at the UofA!
---


 
## Apple's Facial Movement Tracking (Co-op) Project 
University of Alberta (January 2020 - August 2020)

**Project background:** 
- 3D face tracking is a clinical tool which can provide significant information on facial, jaw, and lip motions. 
- The analysis of facial, jaw, and lip movements can be used as an early indicator of neurological diseases, such as Parkinson’s and amyotrophic lateral sclerosis(ALS).
- Previous works have also shown that video-based analysis can help early diagnosis and disease progression in patients with ALS.


**Problems:** Some commercial tracking systems, such as Optotrak, are used in clinical research to capture facial motion. These tracking systems are expensive, and the tracking procedure can be time-consuming. These tracking systems have limited availability because they cannot provide remote tracking applications, such as speech therapy and linguistic data gathering.

**Objective:** develop a novel mobile application to provide a full-face tracking system during speech production.

**Design**:

- It is developed in Xcode and is available on iOS devices with the TrueDepth camera.  

- The development of this mobile application uses ARKit, Apple’s augmented reality platform, and the iPhone’s front-facing TrueDepth camera. 

- The mobile application projects an array of infrared dots onto the user’s face and creates a geometry face mesh with 1220 vertices, at 60 frames per second (FPS). 

- The tracking method is markerless (i.e. no attached sensors).  

Tools: Xcode, an iOS device with a TrueDepth camera, and ARKit (Apple’s augmented reality platform).

Ideas: The tracking coordinate system is right-handed: 
- the positive x direction points to the viewer’s right,
- the positive y direction points to the viewer’s up, 
- the positive z direction points toward the viewer,
- the collected data is the positional changes corresponding to the change of the vertices on the face mesh. The units of face coordinate are in meters. The projected face mesh moves in real time corresponding to the user’s face movement.

 
![image](https://user-images.githubusercontent.com/61716028/210809986-993a6781-9541-4669-be6c-7cfa7469d852.png) [Reference:  Apple’s documentation: ARKit and ARFaceAnchor]




**Results**:

<table>
  <tr>
    <td>
      <img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/e0bc94e3-55ad-48c5-8327-ace69896b9de" alt="Image">
    </td>
    <td>
      <ul>
        <li>The projected face mesh moves in real time corresponding to the user’s face movement.</li>
        <li>It captures both video (60fps) and audio (44.1kHz) recordings during the speech task.</li>
        <li>The bottom part of the screen contains 3 control buttons:
          <ol>
            <li>Start button: Start capturing the video and audio of the experiment</li>
            <li>Change button: Allows the user to read the target sentence at their own pace and change to the next sentence</li>
            <li>Stop button: Stop recording the video and audio and save the position data and recordings locally on the device.</li>
          </ol>
        </li>
      </ul>
    </td>
  </tr>
</table>


<table>
  <tr>
    <td>
      <img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/5cdae747-a085-408a-b776-eef0f0e3b356" alt="GIF">
    </td>
    <td>
      <img width="594" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/625ecefd-08f6-4ee3-863f-80fcc831e2a0">
    </td>
  </tr>
</table>

**Conclusions**:
- The mobile application demonstrates a remote and markerless face-tracking system that can collect articulatory data for research and clinical purposes.
- This mobile application can expand its usage in clinical research, such as speech therapy and automated analysis using biofeedback for stuttering.
- Another future usage of this application is in the facial prosthesis design.  Animating the 3D facial motions, including gestures, can potentially improve soft tissue and its margin fit.

## Calibration of an Intra-Oral Force Measurement Device (Co-op) Project 
University of Alberta  (June 2019 - December 2019)

**Project background:**  Typically, after jaw reconstruction surgery, patients struggle with chewing, swallowing and speaking. In addition, patients can lose their sensation around the jaw, which means that patients may not know how hard they are biting or chewing while eating. As a result, patients require custom-made oral prosthetics to recover oral functionality. However, the process of making the prosthetic can be challenging due to these personalized conditions. 

**Objective:** Develop a more reliable and feasible intra-oral force measurement method for the calibration of an oral prosthesis. 

**Design:** The project places a high priority on quality assurance and quality control.  To recreate a human's occlusal force, the prosthesis needs to meet the following specifications: 1) the normal load rate is from 0 to 500 Newton (estimated human bite force range) 2) the maximum load rate without breaking the oral prosthesis is 1000 N (estimated human maximum voluntary bite force) and 3) the lateral force is 50 N (estimated human tongue force). 

The project used a 3D-printed apparatus, designed by Clayton Molter, to maintain a consistent calibration procedure. In addition, the 3D printed apparatus consists of an arched jig that contains holes; it can attach an air cylinder at various angles from 0 to 180 degrees at 30-degree intervals for various loadings. 

<div style="display: flex; flex-direction: row;">
  <img width="300" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/81e52cbd-5b87-4bab-b7e7-689dd2b2023d">
  <img width="300" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/a8144f0e-b874-4fd7-a014-346c7aaae4f3">
</div>



**Schematic  eletrcial system:**
- The idea was to use the attached air cylinder to apply force to the oral prosthesis. Regulated air (1-100 PSI) and the available pneumatic cylinder provided a theoretical force range of 7.82-781.95 N; this range should satisfy the desired calibration force range of 0-300N (vertical force) and 0-50N (horizontal force). Piston extension and retraction were remotely controlled using an off-the-shelf solenoid valve, a solid-state relay, and a Nation Instruments Data Acquisition (NI-DAQ) system. In addition, calibration of the pneumatic cylinder was done using a load cell.   
![image](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/b71265b1-40cf-4b88-b60f-2c5c5bd7c0ec)

- To electrically control the extension and retraction of the piston, NI-DAQ USB6210, Crydom DC60S3 relay, and CIC 4V220-08 FT Electric Solenoid were wired using standard solid core wires. The following block diagram displays the electrical wiring connection for the extension of the piston.
  
![image](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/d6b1e1c0-6559-47cb-bb76-a54590b26453)

**Finite Element Analysis of the Prosthesis**
- Before the calibration procedure and 3D print the support system, finite element analysis (FEA) simulation was used to predict the static loadings performed on the support system to determine the suitability of the base structure as an object able to withstand the associated forces being presented during measurement using Autodesk Fusion 360. The settings of the following FEA simulation were: 1) applying a 300N vertical force and a 50N horizontal force to the top and lateral surface of the prosthesis prototype respectively 2) selecting acrylic materials for both the structural base and the oral prosthesis prototype (similar to the real oral prosthesis that is made of PMMA) 3) setting a fixed constraint to the bottom surface of the hexagonal base. 

<div style="display: flex; flex-direction: row;">
<img width="400" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/33339dfd-b125-4466-b4c5-a80b8198bbf7">
<img width="400" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/9f2b3598-6e56-49cb-b14e-48680a684d47">
</div>


The following picture shows the complete electrical components in the lab:

![image](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/464870cb-e66a-4cbc-b39a-1d53da69f138)

![image](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/c0289d12-bd8e-4548-b232-a4d083547c3f)


**Results:**
- The available pressure range from the wall supply was 1 to 100 psi. The diameter of the piston rod of the air cylinder was 11mm and the bore size of the air cylinder was 38.1mm. Since we know F=PA, Therefore, the range of the theoretical extension force generated by the air cylinder was F_e = 7.82N to F_e = 781.95N. 

- Once the user adjusted to the proper pressure for calibration, the user then would place the linear load cell at the hexagonal base and calibrate.
  
<img width="700" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/4701813b-eb0d-4c47-b344-3a506beda9f8">





