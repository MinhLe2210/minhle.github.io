+++
title = "Triển khai Ứng dụng toán với Amplify"
date = 2021
weight = 1
chapter = false
+++
## Sơ đồ tổng quan bài thực hành
![Diagram](images/AWS.png?width=40pc)

#### Tổng quan

Trong bài thực hành này, chúng ta sẽ triển khai một ứng dụng với **AWS Amplify** để quản lý toàn bộ quy trình triển khai và lưu trữ ứng dụng web, đồng thời sử dụng các dịch vụ khác như **IAM**, **Lambda**, **API Gateway**, và **DynamoDB** để xây dựng và bảo mật backend cho ứng dụng.

Trước khi bắt đầu, hãy đảm bảo rằng bạn đã quen thuộc với việc triển khai các dịch vụ cơ bản trên AWS. Các tài liệu và hướng dẫn về cách triển khai ứng dụng với các dịch vụ AWS sẽ rất hữu ích để bạn nắm rõ quy trình tổng thể.

#### AWS Amplify
**AWS Amplify** là một nền tảng dịch vụ giúp bạn dễ dàng phát triển, triển khai, và quản lý các ứng dụng web hoặc di động. Amplify cung cấp một bộ công cụ mạnh mẽ cho phép bạn xây dựng cả frontend và backend của ứng dụng một cách nhanh chóng. Với Amplify, bạn có thể tích hợp dễ dàng với các dịch vụ AWS như API Gateway, Lambda, và DynamoDB để xây dựng backend cho ứng dụng của mình.

#### IAM (Identity and Access Management)
**IAM** (*Quản lý danh tính và truy cập*) là một dịch vụ của AWS cho phép bạn kiểm soát quyền truy cập đến các tài nguyên AWS của mình một cách an toàn. Với IAM, bạn có thể tạo người dùng, nhóm người dùng, và gán các quyền truy cập cụ thể để kiểm soát ai có thể thực hiện hành động gì trong tài khoản AWS của bạn. Điều này rất quan trọng để bảo vệ các tài nguyên nhạy cảm, đặc biệt khi bạn triển khai các ứng dụng với Lambda, API Gateway, và DynamoDB.

#### AWS Lambda
**AWS Lambda** là một dịch vụ điện toán không cần quản lý máy chủ, cho phép bạn chạy mã mà không cần phải thiết lập hoặc quản lý các máy chủ. Lambda tự động mở rộng ứng dụng của bạn dựa trên lưu lượng và chỉ tính phí cho thời gian thực hiện mã. Trong bài thực hành này, Lambda sẽ được sử dụng để xử lý logic phía server cho ứng dụng, với các yêu cầu được kích hoạt qua API Gateway và dữ liệu được lưu trữ trong DynamoDB.

#### API Gateway
**API Gateway** là một dịch vụ của AWS giúp bạn tạo, triển khai và quản lý các API RESTful một cách an toàn và hiệu quả. API Gateway hoạt động như một "cửa ngõ" cho phép các ứng dụng frontend của bạn giao tiếp với các chức năng backend được thực thi trong Lambda hoặc DynamoDB. API Gateway cũng hỗ trợ các tính năng như bảo mật, kiểm soát lưu lượng, và giám sát API, giúp bạn quản lý các API một cách toàn diện.

#### DynamoDB
**Amazon DynamoDB** là một dịch vụ cơ sở dữ liệu NoSQL được quản lý toàn phần, cung cấp khả năng lưu trữ và truy xuất dữ liệu với độ trễ thấp và hiệu suất cao. DynamoDB được sử dụng để lưu trữ dữ liệu của ứng dụng mà bạn triển khai trên Amplify, với các tương tác dữ liệu được thực hiện thông qua các Lambda function và API Gateway. DynamoDB đảm bảo rằng dữ liệu của bạn được lưu trữ an toàn, có khả năng mở rộng cao, và luôn sẵn sàng để phục vụ các yêu cầu từ ứng dụng của bạn.



#### Nội dung:
1. [Khởi tạo Amplify](1-amplify)
2. [Khởi tạo Lambda](2-lambda)
3. [Khởi tạo API Gateway](3-api-gateway)
4. [Khởi tạo DynamoDB](4-DynamoDB)
5. [Dọn dẹp tài nguyên](5-cleanup) 