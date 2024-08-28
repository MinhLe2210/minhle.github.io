+++
title = "Khởi tạo DynamoDB"
date = 2024
weight = 1
chapter = false
pre = "<b>4.1. </b>"
+++

#### Hướng dẫn tạo và cấu hình DynamoDB Table trên AWS


1. Truy cập vào DynamoDB:
    1. Ở thanh bên trái của giao diện AWS Management Console, tìm và chọn DynamoDB.
    2. Sau khi vào trang DynamoDB, nhấp vào mục Create Table để bắt đầu quá trình tạo bảng mới.
![DynamoDB](/images/4/1.png)
![DynamoDB](/images/4/2.png)
2. Tạo bảng (Table):
   1. Tại trang Create Table, nhập vào tên bảng (Table Name) mà bạn muốn tạo. Ví dụ, bạn có thể đặt tên là PowerOfMathDatabase.
   2. Đặt tên cho Partition key là ID. Đây sẽ là khóa chính để xác định các mục (items) trong bảng.
![DynamoDB](/images/4/3.png)

3. Cấu hình bảng:
    1. Kéo xuống dưới và chọn Default Settings nếu bạn muốn sử dụng các thiết lập mặc định.
    2. Sau khi chọn xong, nhấp vào nút Create Table để tạo bảng.





![DynamoDB](/images/4/4.png)
![DynamoDB](/images/4/5.png)


