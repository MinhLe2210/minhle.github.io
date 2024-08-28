+++
title = "Test API Gateway"
date = 2021
weight = 3
chapter = false
pre = "<b>3.2 <b>"
+++

#### Hướng dẫn kiểm tra API trên API Gateway
1. Kiểm tra API vừa tạo:
   1. Ở trang API Gateway, trong phần Resources, chọn API mà bạn muốn kiểm tra.
   2. Nhấp vào mục Test để mở giao diện kiểm tra API.
2. Thực hiện kiểm tra API:
   1. Tại phần Request Body, nhập vào các tham số mà bạn muốn kiểm tra. Ví dụ, nếu API của bạn yêu cầu các tham số như base và exponent, bạn có thể nhập:
    ```json
    {
     "base": 3,
     "exponent": 4
   }
    ```
   2. Sau khi nhập các tham số, kéo xuống cuối trang và nhấn nút Test để thực hiện kiểm tra.
![Find API Gateway](/images/3/13.png)
3. Xem kết quả kiểm tra:
   1. Sau khi thực hiện kiểm tra, bạn sẽ thấy kết quả hiển thị bao gồm status code và response body.
   2. Nếu API hoạt động đúng, status code sẽ là 200. Nếu có lỗi, status code sẽ khác và sẽ có thông tin chi tiết về lỗi trong phần response body.

![Find API Gateway](/images/3/14.png)