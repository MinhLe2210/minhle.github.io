+++
title = "Khởi tạo API Gateway"
date = 2021
weight = 2
chapter = false
pre = "<b>3.1 <b>"
+++

#### Hướng dẫn tạo và triển khai AWS API Gateway

1. Truy cập vào API Gateway:
   1. Ở thanh bên trái của giao diện AWS Management Console, tìm và chọn API Gateway.
   2. Tại trang API Gateway, kéo xuống và tìm REST API, sau đó nhấp vào nút Build để bắt đầu.
![Find API Gateway](/images/3/1.png)


2. Tạo mới REST API:
   1. Trong trang Create REST API, chọn New API để tạo một API mới.
   2. Đặt tên cho API của bạn, ví dụ: PowerOfMathAPI.
   3. Sau khi đặt tên, nhấp vào nút Create API để hoàn tất bước tạo API.

![Find API Gateway](/images/3/2.png)

3. Tạo Resource và Method cho API:
   1. Ở trang API Gateway vừa tạo, tại thanh bên trái, nhấn chọn Resources.
   2. Trong phần Resources, chọn "/" (root resource), sau đó nhấp vào Create Method.
   3. Tại trang Create Method, chọn loại method là POST.
   4. Trong mục Lambda Function, chọn khu vực (region) là us-east-1 (hoặc khu vực bạn đã tạo Lambda function trước đó).
   5. Nhập tên của Lambda function đã tạo trước đó, sau đó nhấn Create Method.
![Find API Gateway](/images/3/3.png)
![Find API Gateway](/images/3/5.png)
![Find API Gateway](/images/3/6.png)

4. Cấu hình CORS cho API:
   1. Quay lại trang API Gateway, trong phần Resources, chọn "/" (root resource) một lần nữa.
   2. Nhấp vào nút Enable CORS để bật tính năng CORS (Cross-Origin Resource Sharing).
   3. Trong trang Enable CORS, chọn method POST và sau đó nhấn Save để lưu lại cấu hình.
![Find API Gateway](/images/3/7.png)
![Find API Gateway](/images/3/8.png)
![Find API Gateway](/images/3/9.png)

5. Deploy API:
   1. Quay trở lại trang API Gateway, chọn Deploy API.
   2. Trong phần Stage name, nhập tên của stage mà bạn muốn, ví dụ: staging.
   3. Nhấn vào nút Deploy để triển khai API.
![Find API Gateway](/images/3/10.png)
![Find API Gateway](/images/3/11.png)

6. Lấy URL của API đã triển khai:
   1. Sau khi deploy, truy cập vào phần Stages trong API Gateway.  
   2. Tại đây, bạn sẽ thấy stage name vừa tạo, nhấp vào đó.
   3. Trong phần Invoke URL, sao chép URL của API để sử dụng sau này.
![Find API Gateway](/images/3/12.png)






