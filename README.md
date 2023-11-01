# disease_guava_classification**
This model predicts guava diseases.This model prediction accuracy is 90.73%(test data) && 92.38% accuracy (validation_data)


## **1. Motivation and goals**
- Fruit tree quality monitoring and warning system in agriculture applying artificial intelligence. For the purpose of monitoring to promptly detect diseased fruit trees, the system includes a fly camera that will capture images of trees, leaves, and fruits to the server system.
- All information will be sent to the WebServer system. Thereby helping managers easily observe and control remotely via the IoT system. 
## **2. Các bước thực hiện**

# **2.1 Data collection**
- Collect data from Kaggle, Google, and sources on the Internet
- Collect data directly in guava gardens using phones and flycams
- Data are photos of leaves and fruits with healthy and diseased cases: (4 types of diseases showing on leaves and fruits: Canker, Dot, Mummification, Rush)
- Photo was taken from a high angle looking down, with natural light
# **2.2 Data preprocessing**
- Classify images based on disease types and label them
- Extract features, enhance data when rotating
* Flip (horizontal)
* Roation (0.2)
* Zoom (0.2)
* Height (0.2)
* Width (0.2)
* Rescaling (0-255)-(0-1)
## Original Images 
![screenshot](https://github.com/bmathnguyen/disease_guava_classification/blob/main/output/output.png)

## After augmetation
![augmetation_image](https://github.com/bmathnguyen/disease_guava_classification/blob/main/output/output1.png)
## 3.Build CNN model
CNN model is used to train the network.<br>
Layer parameters:<br>
* Input size (224,224,3)
* Conv2D with 64 filters
* Conv2D with 64 filters
* MaxPool2D (pool_size=2)
* Conv2D with 64 filters
* MaxPool2D (pool_size=2)
* GlobalAveragePooling2D
* Output
### 4.Compile model
Compile the model with the following options:
* Loss function (categorical_crossentropy)
* optimizer (Adam lr=0.001)
* metrics (accuracy)
### Fit model
Then fit the model with the following parameters:
* train_data
* epochs (500)
* validation_data (test data)
* validation_steps (len of test_data)
### Load weight
If you want to optimized this model, you can load weight follow Keras libraly.
For about the dataset, follow this: https://www.kaggle.com/datasets/quangtranminh25/guava-disease-dataset-custom




#### 0.Input image
![layer_0](https://github.com/bmathnguyen/disease_guava_classification/blob/main/output/output.png)
#### 1.Loss 
![layer_0](https://github.com/bmathnguyen/disease_guava_classification/blob/main/output/output2.png)
#### 2.Accurancy 
![layer_2](https://github.com/bmathnguyen/disease_guava_classification/blob/main/output/output3.png)
#### 3.Prediction (final output)
![prediction](https://github.com/bmathnguyen/disease_guava_classification/blob/main/output/output4.png)

## Confusion Matrix
![confusion_matrix](https://github.com/bmathnguyen/disease_guava_classification/blob/main/output/output5.png)



# Demo
Import disease_guava_classification.ipynb to Kaggle and Run all.


# Reference
* [Tensorflow](https://www.tensorflow.org/)
* [data_augmentation](https://www.tensorflow.org/tutorials/images/data_augmentation)
* [paper] (https://ieeexplore.ieee.org/document/9343827)

For more about the dataset, follow this: https://www.kaggle.com/datasets/quangtranminh25/guava-disease-dataset-custom
