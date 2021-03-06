﻿# Understanding Time-Series Data
## Using Neural Networks to work with Time-Series data

### Different Stages that I broke down working with such a different kind of data.
This was my first type, understanding and working in depth with the time series data.
1. Creating a *Synthetic* dataset, Preprocess it for the model and extract out **features** and **targets** from it.
[Notebook](https://github.com/Stalwart-GS/Tensorflow-Developer-Practise/blob/main/Working%20on%20Time%20Series%20Data/Dataset%20-%20Create%2C%20Preprocessing%2C%20Extract%20Features%20%26%20Targets.ipynb)
2. Using a Single Neuron Neural Network to see how the data and targets react with the model to get weights. How good of a prediction is  possible with a single neuron in terms of Time-Series Data. 
[Notebook](https://github.com/Stalwart-GS/Tensorflow-Developer-Practise/blob/main/Working%20on%20Time%20Series%20Data/Single%20Neuron%20NN%20for%20Time_Series.ipynb)
3. Here we have a 3-layered Full connected DNN for Synthetic Time-Series Data that we generated earlier. First 2 layers are 10 neurons each and output layer containes 1 neuron. The processing of dataset into Neural network as Input involved sliding window concept. [Notebook](https://github.com/Stalwart-GS/Tensorflow-Developer-Practise/blob/main/Working%20on%20Time%20Series%20Data/Basic%20DNN%20for%20Time-Series.ipynb)
4. Time-Series data is not just discrete value, there are lot of patterns and relationships between data at different time and other factors involved in the environment. Handling and learning from such data using sequence models gives us a model where output is dependent on the behavious encountered in past. We get to use those relationships during the inference for more accurate prediction. Here I am using a Simple RNN of 2 layers with 2 custom **Lambda layers** from Keras API. [Notebook](https://github.com/Stalwart-GS/Tensorflow-Developer-Practise/blob/main/Working%20on%20Time%20Series%20Data/Dual%20layered%20RNN%20with%20lambda%20layer%20for%20Time-Series.ipynb)
5. To learn on the pattern present in the time-series dataset **BOTH** ways, we are using longer _Bidirectional LSTMs_ (Long Short Term Memory). Here 2-layered Birdirectional LSTMs are used with some Lambda Layers from *Keras API*. [Notebook](https://github.com/Stalwart-GS/Tensorflow-Developer-Practise/blob/main/Working%20on%20Time%20Series%20Data/Dual%20Layered%20Bidirectional%20LSTMs%20on%20Time%20series%20data.ipynb)
6. We generally use a convolutional layer to extract features from an image, but it is not restricted for such a use case only. Here we have used a single **Conv** layer to extract some features from the time serise data and on those features, we applied our previous Bidirecitonal LSTMs layers.[Notebook](https://github.com/Stalwart-GS/Tensorflow-Developer-Practise/blob/main/Working%20on%20Time%20Series%20Data/Convolution%20on%20Top%20of%20LSTMs%20for%20Time%20series%20data.ipynb)
---

### Final Project
After studying and working through all the stages, Now it was time to apply the knowledge on a real world data. So, there is a very famous time series data available for Open Source on [*Kaggle*](https://www.kaggle.com/): 
<br>Sunspots: Monthly mean Total Sunspot Number - from 1749 to july 2018<br>
[Link to Dataset](https://www.kaggle.com/robervalt/sunspots)<br>
<br>
In this project, I have used the power of various different layers and their behavious to get the best result out their symphony (combination)
. These are the different layers used in making the MODEL:
1. Convolutional Layer
2. Long Short Term Memory cell (LSTMs)
3. Dense Layer
4. Lambda Layer

[**Notebook**](https://github.com/Stalwart-GS/Tensorflow-Developer-Practise/blob/main/Working%20on%20Time%20Series%20Data/%5BFinal%20Project%5D%20Predicting%20on%20Kaggle's%20Sunspots%20Time%20series%20Dataset.ipynb)
---
---