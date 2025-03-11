---
layout: page
title: Seattle Weather Prediction
description: Introduction to Artifical Intelligent, Fall 2024
img: assets/img/12.jpg
importance: 3
category: 2024
---
Resources used:
[Seattle Weather Dataset](https://www.kaggle.com/datasets/petalme/seattle-weather-prediction-dataset)
Source code:
[Github Repository](https://github.com/cindyddang/SeattleWeatherPrediction?tab=readme-ov-file)

Predicting the next day’s weather category (drizzle, rain, snow, fog, or sun) in Seattle using historical weather data (precipitation, temperature, wind speed). Examine the performance of 4 different deep learning and machine learning models, including random forest, support vector machine, gradient boosting, and Long Short-Term Memory.

# Data Preprocessing
- Encode categorical 'weather' column
- Normalize numerical columns

# Models
Long-Short term Memory (LSTM):

Preparing input sequence and spilling into training/testing sets. LSTM model includes 1 layer of LSTM and 1 lense layer using softmax activation function.

```python
model = Sequential([
    LSTM(50, input_shape=(sequence_length, len(features))),
    Dense(len(weather_categories), activation='softmax')
])
```

The result shows 66% accuracy. However, the model only predicted rain and sun days, which is a clear sign of overfitting.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/seattle_project/LSTM_confusionmatrix.png" %}
    </div>
</div>
<div class="caption">
    Confusion matrix of LSTM model.
</div>

Three machine learning models used in this projects are Gradient Boosting, Random Forest, and Support Vector Machine (SVM). All models show the accuracy within the range of 21-66%

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/seattle_project/GB_cm.png" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/seattle_project/RF_cm.png" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/seattle_project/SVM_cm.png" %}
    </div>
</div>
<div class="caption">
    Confusion matrix of Gradient Boosting, Random Forest, SVM (from left to right)
</div>

The accuracy cannot be higher than 67% even if models are switching from deep learning and machine learning. All of them tends to predict sun and rain. This could be because of the size of dataset is still small, which is difficult for the models to learn the pattern lying under the numbers and lead to overfitting.

To further study which model is suitable for this predicting problem, a larger dataset will be needed. 



