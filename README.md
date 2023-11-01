# disease_guava_classification**
This model predicts guava diseases.This model prediction accuracy is 90.73%(test data) && 92.38% accuracy (validation_data)


# **1. Động lực và mục tiêu**
- Hệ thống giám sát và cảnh báo chất lượng cây ăn quả trong nông nghiệp ứng dụng trí tuệ nhân tạo. Với mục đích giát sát để kịp thời phát hiện những cây ăn quả bị bệnh, hệ thống bao gồm fly camera sẽ thu hình ảnh của cây, lá cây, quả về hệ thống server. 
- Toàn bộ thông tin sẽ được gửi lên hệ thống WebServer. Qua đó giúp người quản lý dễ dàng quan sát và điều khiển từ xa qua hệ thống IoT. 
**2. Các bước thực hiện**

**2.1 Thu thập dữ liệu**
- Thu thập dữ liệu từ Kaggle, Google, các nguồn trên Internet
- Thu thập dữ liệu trực tiếp tại các vườn ổi bằng điện thoại và flycam
- Dữ liệu là ảnh chụp lá cây và quả với các trường hợp khỏe mạnh và bị bệnh: (4 loại bệnh biểu hiển ở lá và quả: Canker, Dot, Mummification, Rush)
- Ảnh được chụp với góc độ từ trên cao nhìn xuống, ánh sáng tự nhiên
**2.2 Tiền xử lí dữ liệu**
- Tiến hành phân loại ảnh dựa các loại bệnh và gán nhãn
- Trích xuất đặc trưng, tăng cường dữ liệu khi xoay, lật ngược, thu phóng,...
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
## Build CNN model
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
### Compile model
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
Or Import disease_guava_classification.ipynb to Kaggle and Run all.


# Reference
* [Tensorflow](https://www.tensorflow.org/)
* [data_augmentation](https://www.tensorflow.org/tutorials/images/data_augmentation)

For more about the dataset, follow this: https://www.kaggle.com/datasets/quangtranminh25/guava-disease-dataset-custom
