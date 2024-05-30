---
layout: page
title: My School Projects!
---


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
    <td><img width="650" img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/1b279c41-b6f0-41f0-b365-62ab7454b457" alt="image"></td>
   <td><img width="650" img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/c43aa521-06c9-4a60-9cc4-8992a788e069" alt="image"></td>
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
    <td><img width="650" img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/a8978a20-ebdd-45e3-a136-b41d739e7f7b" alt="image"></td>
   <td><img width="650" img src="https://github.com/andrewcccc/andrewcccc.github.io/assets/61716028/0ff705d9-3010-485e-b890-a7b25b7ce31f" alt="image"></td>
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
