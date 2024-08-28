+++
title = "Khởi tạo AWS Amplify"
date = 2020
weight = 1
chapter = false
pre = "<b>1 </b>"
+++




AWS Amplify là một nền tảng phát triển và triển khai ứng dụng toàn diện từ AWS, giúp các nhà phát triển xây dựng và triển khai ứng dụng web và di động một cách nhanh chóng và dễ dàng. Dưới đây là các bước cơ bản để triển khai ứng dụng với AWS Amplify:

#### Deploy with Amplify

1. Đăng nhập vào tài khoản AWS của bạn. Trên thanh tìm kiếm ở phần trên cùng của trang, gõ **Amplify** và chọn AMPLIFY từ danh sách các dịch vụ. **AWS Amplify Console** là nơi bạn quản lý toàn bộ quá trình triển khai và quản lý ứng dụng của mình.


![Find Amplify](/images/1/find.png?width=90pc)

2. Tại giao diện AWS Amplify, nhấp vào nút **Create a new app** để bắt đầu quá trình tạo ứng dụng mới. AWS Amplify hỗ trợ nhiều cách triển khai, từ việc sử dụng Git repository đến tải trực tiếp tệp nén (zip) chứa mã nguồn.

![Find Amplify](/images/1/3.png?width=90pc)

3. Trong trang **Create a new app**, chọn **Deploy without Git** nếu bạn muốn tải trực tiếp mã nguồn mà không cần kết nối với hệ thống quản lý phiên bản như Git. Đây là cách triển khai phù hợp khi bạn đã có sẵn mã nguồn và không cần sử dụng Git để quản lý.



![Find Amplify](/images/1/2.png?width=90pc)

4. Cấu hình ứng dụng và triển khai:
   1. **Đặt tên cho ứng dụng:** Trong bước này, bạn cần đặt tên cho ứng dụng của mình. Ví dụ, bạn có thể đặt tên là **"MathOfMath"**.
   2. **Đặt tên cho branch:** Tiếp theo, đặt tên cho branch (nhánh) mà bạn sẽ triển khai, ví dụ **"main"** hoặc **"production"**.
   3. **Tải lên tệp nén:** Tiếp theo, bạn cần tải lên tệp zip chứa toàn bộ mã nguồn ứng dụng. AWS Amplify sẽ tự động giải nén và xử lý các tệp cần thiết để triển khai ứng dụng.
   4. Sau khi hoàn tất, nhấp vào nút **Save and Deploy** để bắt đầu quá trình triển khai. AWS Amplify sẽ tự động xử lý và triển khai ứng dụng lên hạ tầng AWS.

{{%attachments style="orange" title="index.zip" pattern="index.zip"/%}}

![Find Amplify](/images/1/1.png?width=90pc)

