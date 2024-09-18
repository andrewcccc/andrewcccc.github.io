---
layout: page
title:  My Internships at the UofA!
---


 
## An iPhone app for the Facial Movement Tracking Project 
University of Alberta (January 2020 - August 2020). 

**Funding:** Alberta Innovates Summer Research Studentship

**Project Background:** 
- 3D face tracking is a clinical tool which can provide significant information on facial, jaw, and lip motions. 
- The analysis of facial, jaw, and lip movements can be used as an early indicator of neurological diseases, such as Parkinson’s and amyotrophic lateral sclerosis (ALS).
- Previous works have also shown that video-based analysis can help early diagnosis and disease progression in patients with ALS.

**Problems:** 

- Some commercial tracking systems, such as Optotrak, are used in clinical research to capture facial motion. These tracking systems are expensive, and the tracking procedure can be time-consuming. These tracking systems have limited availability because they cannot provide remote tracking applications, such as speech therapy and linguistic data gathering.
- Kieran Armstrong, a Master's student in Dr. Daniel Aalto's lab, laid out the groundwork for an iPhone facial tracking app. However, the app was not yet suitable for clinical settings for two reasons: 1) The data collection method relied on TCP/IP data communication (app sent data the computer's address on the network) and necessitated an external device (e.g., computer) capable of running a Python script. 2) The app lacked the capability to provide facial exercises for patients. The design was:

<img width="300" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/b8146067-dc5e-460f-9c2e-f268c73aef57">

**Objective:** 
- Design and improve the mobile app to provide a full-face tracking system during speech production.
- My contribution involved improving the user interface and data collection methods for clinical use.

**Understanding the App and Re-Design**: 

The development of this mobile application utilized ARKit, Apple’s augmented reality platform, and the iPhone’s front-facing TrueDepth camera. The application projects an array of infrared dots onto the user’s face, creating a geometric face mesh with 1220 vertices, at 60 frames per second (FPS). The tracking method employed was markerless, meaning no attached sensors were required. The application was developed in Xcode and is available on iOS devices equipped with the TrueDepth camera. The tracking coordinate system is right-handed: 
- the positive x direction points to the viewer’s right,
- the positive y direction points to the viewer’s up, 
- the positive z direction points toward the viewer,
- the collected data is the positional changes corresponding to the change of the vertices on the face mesh. The units of face coordinate are in meters. The projected face mesh moves in real time corresponding to the user’s face movement.

 
![image](https://user-images.githubusercontent.com/61716028/210809986-993a6781-9541-4669-be6c-7cfa7469d852.png) [Reference:  Apple’s documentation: ARKit and ARFaceAnchor]


- The data collection method was redesigned to save locally on the user's device.

- Worked extensively with researchers and speech-language pathologists to develop target sentences for speech exercises.


**Results**:


<table>
  <tr>
    <td>
      <img width="700" img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/e0bc94e3-55ad-48c5-8327-ace69896b9de" alt="Image">
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

**The project aligns with the DMAIC (Define, Measure, Analyze, Improve, Control) methodology:**

1. Define
- Objective: Develop a facial movement tracking app for clinical use during speech production, addressing the limitations of existing systems.
- Problems Identified: High costs, time-consuming processes, lack of remote tracking, reliance on external devices, and lack of facial exercises.
2. Measure
- Tools: Utilized ARKit and the iPhone’s TrueDepth camera for 3D face tracking.
- Data Collection: Measured facial movement using a 1220-vertex mesh at 60 FPS and recorded both audio (44.1kHz) and video.
3. Analyze
- System Analysis: Identified that the existing app's TCP/IP communication and external device requirement hindered clinical usability.
- Feedback: Worked with researchers and speech-language pathologists to analyze the app’s effectiveness in capturing target speech data.
4. Improve
- Redesign: Improved the app’s user interface and data collection method to store data locally on the device.
- New Features: Added speech exercises and streamlined the control buttons for ease of use during speech tasks.
5. Control
- Validation: Tested the app to ensure real-time tracking and accurate data capture for clinical research.
- Future Applications: Highlighted potential for remote speech therapy, biofeedback for stuttering, and facial prosthesis design.

## Human Chewing Force Measurement and Verification Device Project 
University of Alberta  (June 2019 - December 2019)

**Funding:** Dean's Research Awards from the UofA Faculty of Engineering

**Project Background:**  Typically, after jaw reconstruction surgery, patients struggle with chewing, swallowing, and speaking. Additionally, patients can lose sensation around the jaw, meaning they may not know how hard they are biting or chewing while eating. As a result, patients require custom-made oral prosthetics to recover oral functionality. However, the process of making the prosthetic can be challenging due to these personalized conditions.

**Objective:** Develop a reliable intra-oral force measurement device for the design, fabrication, and verification of an oral prosthesis.

**Design:** The project places a high priority on quality assurance and quality control. To recreate human chewing force, the prosthesis needs to meet the following specifications: 1) the normal load rate is from 0 to 500 Newtons (estimated human bite force range); 2) the maximum load rate without breaking the oral prosthesis is 1000 N (estimated human maximum voluntary bite force); and 3) the lateral force is 50 N (estimated human tongue force).

The project utilized a 3D-printed apparatus, designed by Clayton Molter (a previous co-op student), to maintain a consistent calibration procedure. Additionally, the 3D-printed apparatus consists of an arched jig that contains holes; it can attach an air cylinder at various angles from 0 to 180 degrees at 30-degree intervals for different loadings.

<div style="display: flex; flex-direction: row;">
  <img width="300" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/81e52cbd-5b87-4bab-b7e7-689dd2b2023d">
  <img width="300" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/a8144f0e-b874-4fd7-a014-346c7aaae4f3">
</div>



**Schematic Eletrcial System:**
- The concept involved utilizing the attached air cylinder to exert force on the oral prosthesis. With regulated air pressure (1-100 PSI) and the available pneumatic cylinder, a theoretical force range of 7.82-781.95 N was achievable. This range was intended to meet the desired calibration force range of 0-300N (vertical force) and 0-50N (horizontal force). Remote control of piston extension and retraction was facilitated through LabVIEW, utilizing an off-the-shelf solenoid valve, a solid-state relay, and a National Instruments Data Acquisition (NI-DAQ) system. Additionally, calibration of the pneumatic cylinder was conducted using a load cell.
  
![image](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/b71265b1-40cf-4b88-b60f-2c5c5bd7c0ec)

- To electrically control the extension and retraction of the piston, NI-DAQ USB6210, Crydom DC60S3 relay, and CIC 4V220-08 FT Electric Solenoid were wired using standard solid core wires. The following block diagram displays the electrical wiring connection for the extension of the piston.
  
![image](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/d6b1e1c0-6559-47cb-bb76-a54590b26453)



The following picture shows the complete electrical components in the lab:

<img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/464870cb-e66a-4cbc-b39a-1d53da69f138" alt="Image 1" width="600"/>

<img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/c0289d12-bd8e-4548-b232-a4d083547c3f" alt="Image 2" width="600"/>



**Results:**
- The pressure range available from the wall supply was 1 to 100 psi. The diameter of the piston rod of the air cylinder was 11mm, and the bore size of the air cylinder was 38.1mm. Using the formula F=PA, the range of the theoretical extension force generated by the air cylinder was calculated as Fe = 7.82N to Fe = 781.95N.

- Once the user adjusted the pressure to the appropriate level for calibration, they would then position the linear load cell at the hexagonal base and proceed with calibration.

  
<img width="700" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/4701813b-eb0d-4c47-b344-3a506beda9f8">


**Support System and Finite Element Analysis for a Prosthesis Prototype (Additional Task)**
- An oral prosthesis prototype was designed by a biomedical engineer and a dental technologist. We planned to fabricate it and use it in the verification system.
  
<img width="500" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/35fa0de0-3608-4c8d-b424-38896f9248d1">

- A support system is needed to fit future oral prostheses into the hexagonal structure. Design considerations include: 1) the prosthesis must fit with sufficient height for the piston to reach all angles; 2) the support system location must remain consistent for reliable calibration, even if the prosthesis design changes; 3) the support system must be removable to allow space for the linear load cell calibration.

<table>
  <tr>
    <td><img width="469" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/8d379f7d-5d6d-4076-88ba-e8da0c5287be"></td>
    <td><img width="392" alt="image" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/709fa671-e15b-4d28-aff4-9352a6b38815"></td>
  </tr>
  <tr>
    <td style="text-align: center;">Top view of the support system</td>
    <td style="text-align: center;">The support system with the oral prosthesis</td>
  </tr>
</table>


- Before conducting the calibration procedure and 3D printing the support system, finite element analysis (FEA) simulation was employed to forecast the static loadings exerted on the support system. This analysis aimed to ascertain the suitability of the base structure to withstand the associated forces encountered during measurement, utilizing Autodesk Fusion 360. The parameters for the FEA simulation were as follows:
- Applied a 300N vertical force to the top surface and a 50N horizontal force to the lateral surface of the prosthesis prototype.
- Selected acrylic materials for both the structural base and the oral prosthesis prototype to mimic real oral prostheses made of PMMA.
- Imposed a fixed constraint on the bottom surface of the hexagonal base.

<table>
  <tr>
    <td><img width="400" alt="Caption for image 1" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/33339dfd-b125-4466-b4c5-a80b8198bbf7"></td>
    <td><img width="400" alt="Caption for image 2" src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/9f2b3598-6e56-49cb-b14e-48680a684d47"></td>
  </tr>
  <tr>
    <td style="text-align: center;">Vertical 300N force simulation acting on the oral prosthesis</td>
    <td style="text-align: center;">Horizontal 50N force simulation acting on the oral prosthesis</td>
  </tr>
</table>

**Note:** The oral prosthesis prototype began to deform when the 300N force was applied. Overall, the FEA simulation results demonstrated that the support system could handle the vertical force (0-300N) and the horizontal force (0-50N).

**The project fits into the DMADV (Define, Measure, Analyze, Design, Verify) methodology**

1. Define
- Objective: Develop an intra-oral force measurement device to aid in designing and verifying oral prostheses for post-jaw reconstruction surgery patients.
- Specifications: Force requirements: 0-500N (normal), 1000N (max), 50N (lateral).

2. Measure
- System: Calibrated pneumatic cylinder controlled via LabVIEW for precise force application.
- Calibration: Measured vertical and horizontal forces with a load cell.

4. Analyze
- FEA Simulation: Predicted deformations under 300N vertical and 50N horizontal forces.
- Force Calculations: Used F = PA to calculate the force range.

4. Design
- Apparatus: 3D-printed jig with adjustable air cylinder for consistent force application.
- Eletrcial System: Solenoid valve, a solid-state relay, and a National Instruments Data Acquisition (NI-DAQ) system.
- Support System: Removable design for reliable calibration and prosthesis positioning.

6. Verify
- Verification: FEA and calibration results confirmed the system could apply forces without damaging the prosthesis.
