+++
title = "Tải lên file INDEX.HTML"
date = 2021
weight = 2
chapter = false
pre = "<b> 2. </b>"
+++

1. Tạo một tệp index.html đơn giản, bạn có thể tạo bằng cách sao chép đoạn code dưới đây vào **Notepad** và lưu lại dưới dạng **html**

```
<!DOCTYPE html>
<html>
  <head>
    <title>Example</title>
  </head>
  <body>
    <h1>THE FIRST CLOUD JOURNEY</h1>
    <p>FCJ.</p>
  </body>
</html>

```

2. Mở bảng điều khiển Amazon S3 tại https://console.aws.amazon.com/s3/.
3. Tại console, hãy nhấp vào tên của Bucket mà bạn vừa tạo.

![example](/images/2/2/2.0-choose-s3.png?width=90pc)

4. Chọn **Upload**

![example](/images/2/2/2.1-upload.png?width=90pc)

5. Bắt đầu **Add files**

- Chọn **Add files**, chọn tệp **index.html** tại nơi mà bạn đang chứa file.
- Sau đó chọn **Upload**.

![example](/images/2/2/2.2-add-file.png?width=90pc)

![example](/images/2/2/2.3-upload-file.png?width=90pc)

6. Tệp index.html của bạn bây giờ sẽ xuất hiện trong S3 Bucket

![example](/images/2/2/2.4-success.png?width=90pc)

7. Bấm chọn vào file vừa upload thành công chọn **Open**

![example](/images/2/2/2.5-open.png?width=90pc)

8. Kiểm tra thời gian browser loading **index.html**

- Kiểm tra trên thanh browser, xuất hiện đúng region **Singapore** (ap-southeast-1)
- Nhấp chuột phải, chọn **kiểm tra**
- Bên phải trang, chọn **Mạng**
- Nhấn ký hiệu tải lại trang
- Take note thời gian tải trang html (sẽ dùng để so sánh khi triển khai với Cloudfront)

![example](/images/2/2/2.6-check-url.png?width=90pc)
