+++
title = "Test Lambda với DynamoDb"
date = 2024
weight = 3
chapter = false
pre = "<b>4.3. </b>"
+++


#### Hoàn tất tích hợp và kiểm tra kết quả với AWS Lambda và DynamoDB

**1. Cập nhật code cho AWS Lambda:**
   1. Quay lại trang **AWS Lambda**.
   2. Chọn phần **Code** trong bảng điều khiển của Lambda.
   3. Nhập đoạn code cần thiết để tương tác với DynamoDB. 
```python
# import the AWS SDK (for Python the package name is boto3)
import boto3
# import two packages to help us with dates and date formatting
from time import gmtime, strftime

# create a DynamoDB object using the AWS SDK
dynamodb = boto3.resource('dynamodb')
# use the DynamoDB object to select our table
table = dynamodb.Table('PowerOfMathDatabase')
# store the current time in a human readable format in a variable
now = strftime("%a, %d %b %Y %H:%M:%S +0000", gmtime())

# define the handler function that the Lambda service will use an entry point
def lambda_handler(event, context):

# extract the two numbers from the Lambda service's event object
    mathResult = math.pow(int(event['base']), int(event['exponent']))

# write result and time to the DynamoDB table using the object we instantiated and save response in a variable
    response = table.put_item(
        Item={
            'ID': str(mathResult),
            'LatestGreetingTime':now
            })

# return a properly formatted JSON object
    return {
    'statusCode': 200,
    'body': json.dumps('Your result is ' + str(mathResult))
    }
```
  {{% notice info %}}
  Ở dòng table nhớ thay đổi thành tên Table mà bạn đã tạo trước đó
  {{% /notice %}}
![DynamoDB](/images/4/12.png)

**2. Triển khai code và kiểm tra Lambda function:**
   1. Sau khi nhập code, nhấp vào **Deploy** để triển khai code lên Lambda function.
   2. Sau đó, nhấp vào nút **Test** để kiểm tra hoạt động của Lambda function.
   3. Nếu kiểm tra thành công, bạn sẽ thấy **status code 200**, báo hiệu rằng Lambda function đã thực hiện đúng chức năng.
![DynamoDB](/images/4/13.png)

**3. Kiểm tra dữ liệu trong DynamoDB:**
   1. Quay lại trang **DynamoDB**.
   2. Chọn bảng dữ liệu (database) mà bạn đã sử dụng (ví dụ: **PowerOfMathDatabase**).
   3. Nhấp vào **Explore items** để xem các mục (items) đã được lưu trữ trong bảng.
   4. Bạn sẽ thấy kết quả mà Lambda function đã trả về thông qua API Gateway ở các bước trước.
![DynamoDB](/images/4/14.png)
![DynamoDB](/images/4/15.png)

4.  Kiểm tra trang web đã được triển khai:

    1. Truy cập vào AWS Amplify và mở giao diện quản lý ứng dụng của bạn.
    2. Tại đây, bạn sẽ thấy một liên kết dẫn đến trang web đã được deploy.
    3.  Nhấp vào liên kết này để mở trang web và kiểm tra xem ứng dụng của bạn đã được triển khai thành công hay chưa.


![DynamoDB](/images/4/16.png)


