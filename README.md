Các bước run :

Bước 1. Thu thập dữ liệu khuôn mặt — build_dataset.py
+ Nhập id và tên trên giao diện
+ Webcam khởi động và hiển thị video trực tiếp
+ Đưa khuôn mặt vào khung hình và nhấn phím s (khoảng 10-15 tấm)
+ Nhấn q để thoát khỏi webcam
+ Các ảnh được lưu vào thư mục dataset

Bước 2: 
+ Chương trình đọc tất cả ảnh trong thư mục dataset.
+ Phát hiện khuôn mặt trong từng ảnh.
+ Trích xuất đặc trưng khuôn mặt và chuyển thành vector số.
+ Lưu vector đặc trưng cùng tên người tương ứng để sử dụng khi nhận diện.

Bước 3. Nhận diện khuôn mặt — recognize_faces_video.py
+ Webcam ghi hình trực tiếp.
+ Hệ thống phát hiện khuôn mặt trong từng khung hình.
+ Chuyển khuôn mặt thành vector encoding 128 chiều.
+ So sánh vector mới với các vector đã lưu bằng hàm so sánh của face_recognition.
+ Nếu khoảng cách nằm trong ngưỡng cho phép, hệ thống hiển thị tên người tương ứng; nếu không khớp, có thể hiển thị Unknown.
