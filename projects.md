---
layout: page
title: My School Projects!
---


## COMP551 Applied Machine Learning Projects 
McGill University (September 2022 - December 2022)

**Project 1: Getting Started with Machine Learning (Garde: A)**

The goal of this project is to build K Nearest Neighbour (KNN) and Decision Tree (DT) models on two health datasets (Hepatitis and Diabetic Retinopathy Debrecen Messidor Dataset) and compare the model performance. The project report can be found [here](https://andrewcccc.github.io/assignment1_group_47.pdf).


* Implemented KNN feature selection function based on linear coefficient
* Contributed to the model  evaluation, such as AUROC, of the two models

What I learned: 

**Project 2: Classification of Textual Data (Garde: A)**

The goal of this project was to build logistic regression and multiclass regression models and compare them to a KNN model on two textual datasets (IMDb and 20 Newsgroup). The project report can be found [here](https://andrewcccc.github.io/assignment2_group_47.pdf).

* Implemented LASSO feature selection functions
* Evaluated the logistic regression and multiclass regression models w.r.t KNN models 

What I learned: 

**Project 3: Classification of Image Data (Garde: A)**

The goal of this project was to build a multilayer perceptron (MLP) and CNN model to classify image data. The project report can be found [here](https://andrewcccc.github.io/assignment3_group_47.pdf).

Datasets:

* Implemented CNN using Keras library 
* Contributed to the hyper-parameters fine-tuning of L2 regularization
* Investigated the effects of test accuracy using different network depth, width, and activation functions 

What I learned: 


## ECE Capstone Project 
University of Alberta (September 2020 - May 2021) - (Garde: A)

**Problems:** Greenhouse operations in Alberta are often restricted in scale as a consequence of low-profit margins arising from high energy costs. Reducing these high costs through the incorporation of greenhouse technology could make greenhouse operations more feasible and common in Alberta. Since careful environmental control is required to ensure a crop’s quality and yield, growers are challenged to have enough knowledge to interpret the information provided by the monitoring system and adjust control setpoints accordingly.

**Objective:** The goal of this project is to address this need with the development of an integrated mini-production facility equipped with sensors, controllers and actuators that features both a monitoring-reporting system and an artificial intelligence- based control-decision-making system to optimize conditions for plant growth and the overall energy cost.

**Design**:
- Below is an overview of the project design and the interaction points between hardware and software components. A temperature/humidity dual sensor within the tank enclosure feeds temperature and humidity values into the central controller (Raspberry Pi), while an infrared (IR) camera module captures and saves pictures of the KOM in the same device. An AC current sensor provides the controller with insights into the system's power draw.
- On the controller side, object detection and analysis are first performed on the recently captured image to measure the heights of individual KOM. A combination of historical and current readings of the system's temperature and humidity is then used by the controller to determine any responsive actions that the heater and/or humidifier will undertake.
- All system parameters are saved within a database and can be accessed by the user through an Android application.

![cachedImage](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/2d900b22-29db-4c77-9a34-b87bcfa448e4)


**Tasks:** 
- I designed and developed an Android mobile application to communicate with a MySQL database and retrieve current humidity, temperature sensor data, and mushroom images for monitoring the conditions of our mushrooms in the greenhouse. The project code for the app can be found [here](https://github.com/andrewcccc/Greenhouse). The app was built in Android Studio, programmed in Java.

- Below is the workflow:
  
  ![image](https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/420e831c-8623-4857-9c45-915d218c201b)



Highlights: 
* Used Retrofit API to retrieve JSON sensor data
* Used the MPAndroidChart library to display graphical data
* Used the Picasso library to retrieve image results
* Communicated with the MySQL database through PHP

**How does Retrofit API work?**
- Retrofit is a type-safe HTTP client for Android and Java applications. It simplifies the process of making HTTP requests to web services and processing their responses. Steps are:
- Interface Definition: Developers define an interface representing the API endpoints they intend to interact with. This interface contains methods annotated with HTTP verbs like @GET, @POST, @PUT, @DELETE, along with relative URL paths and any required parameters. These methods indicate the desired action to be performed on a resource identified by the given URL.

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

- Retrofit Configuration: Retrofit is configured by creating a Retrofit object with the base URL of the API. This base URL serves as the foundation for all API endpoints, allowing Retrofit to construct the complete URL paths for requests.

```java
public interface Api {
    String BASE_URL = "http://192.xxx.x.xx";
    
    @GET("Apppi.php")
    Call<List<Details>> getstatus();
}
```

- API Call: With Retrofit configured, we can now create an instance of the defined interface using the Retrofit object. This instance acts as a proxy for making API requests. To execute an API call, simply invoke the methods defined in the interface. Retrofit handles the heavy lifting of making the network request asynchronously and processing the response.

```java
private void fetchData() {
    Retrofit retrofit = new Retrofit.Builder()
            .baseUrl(Api.BASE_URL)
            .addConverterFactory(GsonConverterFactory.create())
            .build();

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
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/dataviewcopy.JPG" width="300" height="600" /></td>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/grahpviewcopy.JPG" width="300" height="600" /></td>
    <td><img src="https://raw.githubusercontent.com/andrewcccc/andrewcccc.github.io/master/mushroomgrowthcopy.PNG" width="300" height="600" /></td>
  </tr>
 </table>
