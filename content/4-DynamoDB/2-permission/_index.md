+++
title = "Khởi tạo Permistion"
date = 2024
weight = 2
chapter = false
pre = "<b>4.2. </b>"
+++




#### Hướng dẫn tích hợp DynamoDB với AWS Lambda và cấu hình IAM Policy

**1. Lấy Amazon Resource Name (ARN) của DynamoDB Table:**
   1. Sau khi bảng DynamoDB được khởi tạo thành công, truy cập vào trang **Table** của DynamoDB.
   2. Chọn bảng vừa tạo (ví dụ: **PowerOfMathDatabase**).
   3. Nhấp vào **Additional Info** để xem thông tin bổ sung, bao gồm **Amazon Resource Name (ARN)**.
   4. Sao chép ARN này để sử dụng trong các bước tiếp theo.
![DynamoDB](/images/4/6.png)

**2. Cấu hình quyền truy cập IAM cho Lambda:**
   1. Quay lại trang **AWS Lambda**.
   2. Trong phần **Configuration**, kéo xuống và chọn **Permissions**.
   3. Nhấp vào **Role name** để mở trang IAM liên quan đến role này.
![DynamoDB](/images/4/permision.png)

**3. Tạo Inline Policy cho IAM Role:**
   1. Trên trang IAM vừa mở, chọn tab **Permissions**.
   2. Nhấp vào **Add permissions** và chọn **Create inline policy**.
   3. Chuyển sang tab **JSON** trong phần **Create policy**.
   4. Dán đoạn mã JSON dưới đây vào **Policy editor**:
  ```json
  {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "dynamodb:PutItem",
                "dynamodb:DeleteItem",
                "dynamodb:GetItem",
                "dynamodb:Scan",
                "dynamodb:Query",
                "dynamodb:UpdateItem"
            ],
            "Resource": "YOUR-TABLE-ARN"
        }
        ]
    }
  ```
  {{% notice info %}}
  Ở phần "resource" nhớ thay đổi thành ARN của DynamoDB đã tạo trước đó
  {{% /notice %}}
   - Nhấp vào **Next** để tiếp tục.
  
![DynamoDB](/images/4/8.png)
![DynamoDB](/images/4/9.png)

**4. Đặt tên và tạo Policy:**
   1. Trong trang tiếp theo, đặt tên cho **Policy name** (ví dụ: **PowerOfMathPolicy**).
   2. Nhấp vào **Create policy** để hoàn tất quá trình tạo policy.

![DynamoDB](/images/4/10.png)

**5. Xác nhận tạo Policy thành công:**
   1. Quay lại trang IAM, bạn sẽ thấy policy mới vừa tạo đã được gán vào role của Lambda.

![DynamoDB](/images/4/11.png)


**6. Cập nhật code cho AWS Lambda:**
   1. Quay lại trang **AWS Lambda**.
   2. Chọn phần **Code** và nhập đoạn code cần thiết để tương tác với DynamoDB, sử dụng ARN đã sao chép ở bước 1.



