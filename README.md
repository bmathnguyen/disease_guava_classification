# disease_guava_classification**
This model predicts guava diseases.This model prediction accuracy is 90.73%(test data) && 92.38% accuracy (validation_data)
**1. Động lực và mục tiêu**
- Hệ thống giám sát và cảnh báo chất lượng cây ăn quả trong nông nghiệp ứng dụng trí tuệ nhân tạo. Với mục đích giát sát để kịp thời phát hiện những cây ăn quả bị bệnh, hệ thống bao gồm fly camera sẽ thu hình ảnh của cây, lá cây, quả về hệ thống server. 
- Toàn bộ thông tin sẽ được gửi lên hệ thống WebServer. Qua đó giúp người quản lý dễ dàng quan sát và điều khiển từ xa qua hệ thống IoT. 
**2. Các bước thực hiện**

    2.1 Thu thập dữ liệu
        -Thu thập dữ liệu từ Kaggle, Google, các nguồn trên Internet
        -Thu thập dữ liệu trực tiếp tại các vườn ổi bằng điện thoại và flycam
        -Dữ liệu là ảnh chụp lá cây và quả với các trường hợp khỏe mạnh và bị bệnh: (4 loại bệnh biểu hiển ở lá và quả: Canker, Dot, Mummification, Rush)
        -Ảnh được chụp với góc độ từ trên cao nhìn xuống, ánh sáng tự nhiên
    2.2 Tiền xử lí dữ liệu
        -Tiến hành phân loại ảnh dựa các loại bệnh và gán nhãn
        -Trích xuất đặc trưng, tăng cường dữ liệu khi xoay, lật ngược, thu phóng,...
    2.3 Xây dựng mô hình CNN
  
        
For about the dataset, follow this: https://www.kaggle.com/datasets/quangtranminh25/guava-disease-dataset-custom
