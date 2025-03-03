---
layout: page
title: My School Projects!
---

## Master's Thesis Project
McGill University (September 2021 - October 2023)

**Title: Design, Development, and Usability Evaluation of a Mobile Application for Monitoring Voice and Upper Airway Health**

**Funding:** Fonds de Recherche du Québec - Santé (FRQS) and Centre for Research on Brain, Language (CRBLM).

**Background:** 

- Asthma and chronic obstructive pulmonary disease (COPD) are highly prevalent chronic respiratory diseases worldwide and in Canada. Asthma is a long-term condition that causes the airways to become inflamed, leading to repeated episodes of coughing, wheezing, difficulty breathing, and chest tightness. COPD is another lung condition that causes ongoing symptoms like shortness of breath, coughing, and mucus buildup due to damage or inflammation in the airways or air sacs in the lungs, which makes it hard to breathe and gets worse over time.

- Despite the availability of telemonitoring methods, adequate symptom control in asthma and COPD remains a challenge due to the unpredictable nature of exacerbations and nighttime awakenings, which can lead to increased hospitalizations, healthcare costs and mortality. 
 
- Wearable devices and mobile health (mHealth) technology can help control asthma and COPD symptoms through continuous real-time monitoring of lifestyle and weather conditions and early detection of exacerbations. Many wearable devices use audio sensing technology to detect audible symptoms (e.g., cough, wheeze etc.) associated with asthma and COPD and smartphones to collect/analyze the audio data.
  
- However, with wearables that use acoustic microphones, their audio signals carry identifiable speech information and personal privacy becomes a significant concern. In addition, computing capacity on a smartphone alone has shown to be maxed out rapidly with the detection of one single symptom due to the complexity of audio signals.
- To address the privacy concern, Dr. Li-Jessen’s team has developed a wearable device, namely AIrway, based on the neck surface accelerometer (NSA) technology, to monitor upper airway symptoms. The NSA is a miniaturized sensor placed on the neck surface to detect and transfer the mechanical skin vibrations (transmitted from the vocal folds and vocal tract) to electrical signals. Therefore, instead of collecting microphone-acoustic signals, the NSA captures negligible vocal tract resonance information, which preserves a person’s speech privacy. Furthermore, AIrway’s machine learning algorithms will be allocated in both the wearable device (for symptom event classification) and the smartphone (for exacerbation prediction) to leverage the computing resources.
  
<table>
  <tr>
    <td><img width="600" img src="https://github.com/user-attachments/assets/81f24b49-3750-4e71-97d9-1eec1e547dd2" alt="Project Overview"></td>
  </tr>
  <tr>
    <td style="text-align: center;">Project Overview</td>
  </tr>
</table>

**Objective:** 

- The research aims are to 1) design and develop a mobile app to support a wearable device for data collection and visualization, and 2) perform a usability evaluation of the app.

- User needs: a wireless and user-friendly mHealth solution that provides self-management for symptoms, medication, and action plans.
   

**Methods:**

- The AIrway app was designed and developed for Android smartphone devices in accordance with industral mobile app design prcoesses and clinical guidelines, such as the Global Initiative for Asthma (GINA) and the Global Initiative for Chronic Obstructive Lung Disease (GOLD), to meet the needs of symptom monitoring. The app also complies with the Personal Information Protection and Electronic Documents Act (PIPEDA) to ensure the protection of user information. Essential features include journaling asthma/COPD diaries, utilizing the Google Firestore cloud service for data storage, parsing local weather information, as well as sending medication reminders and action plans.
  
- Color Contrast: We optimized color contrast for app interfaces to improve user accessibility and usability. According to Web Content Accessibility Guidelines (WCAG), text and images should have a contrast ratio of at least 7:1 for AAA compliance.
 
- Literacy Analysis: We used an open-source readability calculator to check the app’s written materials, including the privacy policy, FAQ, and action plans for asthma and COPD. We aimed for a readability level equivalent to grade 9, suitable for most English-educated adults in the U.S.

<table>
  <tr>
    <td><img width="600" img src="https://github.com/user-attachments/assets/e4b8e4fb-8d5e-4f37-a397-7408ad30910a" alt="Project Overview"></td>
  </tr>
  <tr>
    <td style="text-align: center;">mHealth Design Prcoess</td>
  </tr>
</table> 

- Usability Testing: We recruited five app developers (i.e., technical raters) who were Computer Science Ph.D. students or post-doctoral fellows with at least one year of mobile app programming experience or who had taken at least one mobile app development course to evaluate the AIrway app. These technical raters completed the User Version of the Mobile Application Rating Scale (uMARS) survey, provided open-ended feedback, and responded to the IQVIA items after testing the app. The uMARS survey was designed to assess the app's engagement, functionality, aesthetics, and information quality while the IQVIA items were intended to assess the app's self-management functionality.


**Results:** The results indicate that the AIrway app was easily understandable to individuals with nine years of formal education and high colour constatct (12.15: 1 for app background and text). The app received a high uMARS overall mean score of 3.6 out of 5.0 and an IQVIA overall median score of 8 out of 11. These scores align with similar mHealth apps in the literature (MARS: 3.0-4.2 and IQVIA: 6-10). Open-ended feedback suggested incorporating more graphical icons for better user interface display and improving the input field for the password reset function.

<table>
  <tr>
    <td><img width="600" img src="https://github.com/user-attachments/assets/ca154dcd-2129-4c4d-9998-cc4358b7b33a" alt="Project Overview"></td>
  </tr>
  <tr>
    <td style="text-align: center;">1a) Login page1b) Register page 1c) Register page with info. 1d) Forgot password prompt.</td>
  </tr>
</table> 


<table>
  <tr>
    <td><img width="600" img src="https://github.com/user-attachments/assets/c2d6e3fa-ce4a-44a4-b91d-ac849469a91c" alt="Project Overview"></td>
  </tr>
  <tr>
    <td style="text-align: center;">2a) Today interface 2b) Report interface 2c) Profile interface 2d) Help interface.</td>
  </tr>
</table> 

**Conclusion:** The app met mobile app design principles and development guidelines, achieving appropriate color contrast, readability, and layout presentations. Additionally, asthma and COPD diaries, medication profiles, and action plans were developed based on clinically validated guidelines. These steps are essential for meeting industrial standards and ensuring the app’s credibility, accessibility, and usability. Future steps include expanding the app’s compatibility to cross-platform frameworks to enhance accessibility and equity.


**This project aglins with the DMADV methodology**
- Define: Identifying the need for a mobile app to monitor respiratory symptoms while addressing privacy concerns.
- Measure: Assessing user needs, accessibility, and privacy requirements (color contrast, readability, data protection).
- Analyze: Gathering insights from technical raters to evaluate app functionality and user experience.
- Design: Creating the app with features like symptom journaling, cloud storage, and medication reminders.
- Verify: Conducting usability testing to ensure the app meets industry standards and achieves high user ratings.

## COMP551 Applied Machine Learning Projects 
McGill University (September 2022 - December 2022)

**Project 1: Getting Started with Machine Learning (Grade: A)**

The goal of this project is to build K Nearest Neighbour (KNN) and Decision Tree (DT) models on two health datasets (Hepatitis and Diabetic Retinopathy Debrecen Messidor Dataset) and compare the model performance. The project report can be found [here](https://andrewcccc.github.io/assignment1_group_47.pdf).


* Implemented KNN feature selection function based on linear coefficient
* Contributed to the model  evaluation, such as AUROC, of the two models
  
What I learned: 
- Select a pair of important numerical features and evaluate the feature importance by LinearRegression for the KNN model and RandomForestRegressor for the DT model. Both of these built-in functions from sklearn output a score for each feature, and a higher score reflects a greater significance of the feature.
- For KNN evaluation, K is the hyperparameter. We aim to avoid overfitting (i.e., when the model learns the training data too well) or underfitting (i.e., when the model fails to capture the underlying patterns in the data). A higher AUC (Area Under the Curve) indicates better performance.

<table>
  <tr>
    <td><img width="600" img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/1b279c41-b6f0-41f0-b365-62ab7454b457" alt="image"></td>
   <td><img width="600" img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/c43aa521-06c9-4a60-9cc4-8992a788e069" alt="image"></td>
  </tr>
  <tr>
    <td style="text-align: center;">A feature selection example for the Hepatitis dataset</td>
    <td style="text-align: center;">KNN Evaluation</td>
  </tr>
</table>



**Project 2: Classification of Textual Data (Grade: A)**

The goal of this project was to build logistic regression and multiclass regression models and compare them to a KNN model on two textual datasets (IMDb and 20 Newsgroup). The project report can be found [here](https://andrewcccc.github.io/assignment2_group_47.pdf).

* Used Z-score for feature selection 
* Evaluated the multiclass regression model

<table>
  <tr>
    <td><img width="600" img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/a8978a20-ebdd-45e3-a136-b41d739e7f7b" alt="image"></td>
   <td><img width="600" img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/0ff705d9-3010-485e-b890-a7b25b7ce31f" alt="image"></td>
  </tr>
  <tr>
    <td style="text-align: center;">Z-score selection for IMDb dataset</td>
    <td style="text-align: center;">Heat Map based on the highest weights for the multi-class classifier</td>
  </tr>
</table>

What I learned: 
- Z-score is a statistical measure that indicates how many standard deviations a data point is from the mean of a dataset. Before calculating z-scores for feature selection, the features are typically standardized (also known as normalization). This involves transforming each feature such that it has a mean of 0 and a standard deviation of 1. Features with higher absolute z-scores are considered more important.

**Project 3: Classification of Image Data (Grade: A)**

The goal of this project was to build a multilayer perceptron (MLP) and CNN model to classify the Fashion-MNIST dataset (a collection of fashion-based images). The project report can be found [here](https://andrewcccc.github.io/assignment3_group_47.pdf).

* Implemented CNN using Keras library 
* Contributed to the hyper-parameters fine-tuning of L2 regularization
* Investigated the effects of test accuracy using different network depth, width, and activation functions 

What I learned: 
- A loss function evaluates how well a model is performing by comparing its predictions with the actual target values in the training data. During the training process, the goal is to minimize the loss function.
- L2 regularization (aka weight decay) is a technique used to prevent overfitting and improve the generalization ability of a model. In the context of neural networks, L2 regularization works by adding a penalty term to the loss function during training. This penalty term is proportional to the squared magnitude of the weights in the network. It is expressed:

```java
L2 regularization term = λ * ∑(wᵢ²)
```


## Optimal Energy Management of Mini Greenhouses (ECE Capstone Project) 
University of Alberta (September 2020 - May 2021) - (Grade: A)

**Problems:** Greenhouse operations in Alberta are often restricted in scale as a consequence of low-profit margins arising from high energy costs. Reducing these high costs through the incorporation of greenhouse technology could make greenhouse operations more feasible and common in Alberta. Since careful environmental control is required to ensure a crop’s quality and yield, growers are challenged to have enough knowledge to interpret the information provided by the monitoring system and adjust control setpoints accordingly.

**Objective:** The goal of this project is to address this need with the development of an integrated mini-production facility equipped with sensors, controllers and actuators that features both a monitoring-reporting system and an artificial intelligence- based control-decision-making system to optimize conditions for plant growth and the overall energy cost.

**Design**:
- Below is an overview of the project design and the interaction points between hardware and software components. A temperature/humidity dual sensor within the tank enclosure feeds temperature and humidity values into the central controller (Raspberry Pi), while an infrared (IR) camera module captures and saves pictures of the King Oyster Mushrooms (KOM) in the same device. An AC current sensor provides the controller with insights into the system's power draw.
- On the controller side, object detection and analysis are first performed on the recently captured image to measure the heights of individual KOM. A combination of historical and current readings of the system's temperature and humidity is then used by the controller to determine any responsive actions that the heater and/or humidifier will undertake.
- All system parameters are saved within a database and can be accessed by the user through an Android application.

![cachedImage](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/2d900b22-29db-4c77-9a34-b87bcfa448e4)


**Tasks:** 
- I designed and developed an Android mobile application to communicate with a MySQL database and retrieve current humidity, temperature sensor data, and mushroom images for monitoring the conditions of our mushrooms in the greenhouse. The project code for the app can be found [here](https://github.com/andrewcccc/Greenhouse). The app was built in Android Studio, programmed in Java.

- Below is the workflow:
  

![334936993-420e831c-8623-4857-9c45-915d218c201b](https://github.com/user-attachments/assets/305be3ac-0dd8-4161-8aaa-6d7900f9c17c)



Highlights: 
* Used Retrofit API to retrieve JSON sensor data
* Used the MPAndroidChart library to display graphical data
* Used the Picasso library to retrieve image results
* Communicated with the MySQL database through PHP

**How does Retrofit API work?**
- Retrofit is a high-level HTTP client library for Android and Java applications. It allows developers to define API endpoints as Java interfaces, then automatically converts JSON responses into Java objects. Retrofit simplifies (constructing HTTP requests, mapping server responses to data models, handling asynchronous network calls.) tasks. Steps are:

- Data Model: The Details class serves as a data model to represent the structure of JSON responses received from the API. Data models are essential for mapping the JSON data to Java objects, making it easier to work with the response data in the application code.

```java
public class Details {
    @SerializedName("temperature")
    @Expose
    private String temperature;

    @SerializedName("humidity")
    @Expose
    private String humidity;

    // Getters and Setters
    public String getTemperature() {
        return temperature;
    }

    public void setTemperature(String temperature) {
        this.temperature = temperature;
    }

    public String getHumidity() {
        return humidity;
    }

    public void setHumidity(String humidity) {
        this.humidity = humidity;
    }
}
```

- Interface Definition: Developers define an interface representing the API endpoints they intend to interact with. This interface contains methods annotated with HTTP verbs like @GET, @POST, @PUT, @DELETE, along with relative URL paths and any required parameters. These methods indicate the desired action to be performed on a resource identified by the given URL.

```java
public interface Api {
    String BASE_URL = "http://192.xxx.x.xx";
    
    @GET("Apppi.php")
    Call<List<Details>> getstatus();
}
```

- Retrofit Configuration: Retrofit is configured by creating a Retrofit object with the base URL of the API. This base URL serves as the foundation for all API endpoints, allowing Retrofit to construct the complete URL paths for requests. Additionally, converters like GsonConverterFactory can be added to handle serialization and deserialization of JSON data.

```java

Retrofit retrofit = new Retrofit.Builder()
        .baseUrl(Api.BASE_URL)
        .addConverterFactory(GsonConverterFactory.create())
        .build();
```


- API Call: With Retrofit configured, we can now create an instance of the defined interface using the Retrofit object. This instance acts as a proxy for making API requests. To execute an API call, simply invoke the methods defined in the interface. Retrofit handles the heavy lifting of making the network request asynchronously and processing the response.

```java
private void fetchData() {
    Api api = retrofit.create(Api.class);
    Call<List<Details>> call = api.getstatus();
    call.enqueue(new Callback<List<Details>>() {
        @Override
        public void onResponse(Call<List<Details>> call, Response<List<Details>> response) {
            if (response.isSuccessful() && response.body() != null) {
                List<Details> adslist = response.body();
                Details details = adslist.get(0);

                // Use details to update UI...
                float power = details.getCurrent() * 120;
                temperaturetxt.setText(details.getTemperature());
                humiditytxt.setText(details.getHumidity());
                timestampstxt.setText(details.getTimestamps());
                currenttxt.setText(String.valueOf(power));
                heatertxt.setText(details.getHeater());
                humidifiertxt.setText(details.getHumidifier());
            }
        }
```

Screenshots:

<table>
  <tr>
    <td>The numerical sensor data view</td>
     <td>The graphical data view</td>
     <td>The mushroom image view</td>
  </tr>
  <tr>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/dataviewcopy.JPG" width="280" height="550" /></td>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/grahpviewcopy.JPG" width="280" height="550" /></td>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/mushroomgrowthcopy.PNG" width="280" height="550" /></td>
  </tr>
 </table>
