+++
title = "Khởi tạo AWS Lambda"
date = 2024
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

## Hướng dẫn tạo và triển khai AWS Lambda Function
AWS Lambda là một dịch vụ điện toán không cần máy chủ (serverless) của Amazon Web Services (AWS), cho phép bạn chạy mã mà không cần quản lý máy chủ. Lambda tự động mở rộng và chỉ tính phí dựa trên thời gian thực hiện của mã, làm cho nó trở thành lựa chọn lý tưởng cho nhiều tác vụ tự động hóa và xử lý dữ liệu. Dưới đây là các bước để tạo và triển khai một hàm (function) với AWS Lambda.


1. Đăng nhập vào tài khoản AWS của bạn và trong thanh tìm kiếm ở phần trên cùng, gõ "Lambda". Chọn Lambda từ danh sách các dịch vụ để mở AWS Lambda Console. Tại đây, bạn có thể tạo, quản lý và giám sát các hàm Lambda của mình.
![Diagram](../../../images/2/1.png?width=40pc)

2. Trong trang AWS Lambda Console, nhấp vào nút Create function để bắt đầu quá trình tạo mới một hàm. Đây là nơi bạn sẽ định nghĩa các thông tin cơ bản cho hàm Lambda của mình.


3. Cấu hình hàm Lambda:
   1. Trong trang Create function, chọn Author from scratch để bắt đầu từ đầu.
   2. Đặt tên cho function: Nhập tên cho hàm Lambda của bạn, ví dụ như "PowerOfMathFunction".
   3. Chọn runtime: Chọn phiên bản runtime mà mã của bạn sẽ chạy, ví dụ: Python 3.11.
   4. Chọn kiến trúc: Chọn kiến trúc phù hợp, ví dụ x86_64.
   5. Sau khi hoàn tất các bước trên, nhấp vào Create function để tạo hàm.
![Diagram](../../../images/2/2.png?width=40pc)

4. Viết và triển khai mã:
   1. Sau khi hàm được tạo thành công, bạn sẽ được chuyển đến trang cấu hình của hàm. Tại phần Code source, bạn có thể nhập mã Python của mình. Ví dụ, bạn có thể nhập mã sau:
    ``` python
    # import the JSON utility package
   import json
   # import the Python math library
   import math

   # define the handler function that the Lambda service will use an entry point
   def lambda_handler(event, context):

   # extract the two numbers from the Lambda service's event object
       mathResult = math.pow(int(event['base']), int(event['exponent']))

       # return a properly formatted JSON object
       return {
       'statusCode': 200,
       'body': json.dumps('Your result is ' + str(mathResult))
       }
    ```
   2. Nhấp vào Deploy để triển khai mã. Khi triển khai thành công, hàm của bạn đã sẵn sàng để được kích hoạt.
![Diagram](../../../images/2/3.png?width=40pc)

5. Cấu hình và chạy thử nghiệm:
   1. Sau khi triển khai, nhấp vào Test để cấu hình và chạy thử nghiệm.
   2. Chọn Create a new test event, đặt tên cho sự kiện, ví dụ như "TestEvent1".
   3. Cấu hình parameters: Đối với mã trên, bạn cần cung cấp hai tham số trong JSON như trong hình
   4. Nhấp vào Create để lưu sự kiện thử nghiệm. Sau đó, nhấp vào Test để chạy hàm với các tham số đã cấu hình và kiểm tra kết quả.
![Diagram](../../../images/2/4.png?width=40pc)



![Diagram](../../../images/2/5.png?width=40pc)
