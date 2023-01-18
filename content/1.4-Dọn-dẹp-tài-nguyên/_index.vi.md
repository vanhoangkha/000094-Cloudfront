+++
title = "Dọn dẹp tài nguyên"
date = 2021
weight = 4
chapter = false
pre = "<b> 4. </b>"
+++

Các hướng dẫn sau, sẽ xóa CloudFront distribution và S3 bucket được tạo trong bài Lab này.

#### Xóa CloudFront distribution:

1. Mở bảng điều khiển Amazon CloudFront tại (https://console.aws.amazon.com/cloudfront/home).
2. Từ bảng điều khiển bảng điều khiển, chọn distribution mà bạn đã tạo trước đó, chọn **Disable**. Để xác nhận, chọn **Disable**.
3. Sau khoảng 15 phút khi trạng thái **Disabled**, chọn distribution và chọn **Delete**,và để xác nhận chọn **Delete**.

#### Xóa S3 Bucket:

1. Mở bảng điều khiển Amazon S3 tại https://console.aws.amazon.com/s3/.
2. Chọn Bucket bạn đã tạo trước đó, sau đó nhấp vào **Empty** từ thanh menu.
3. Xác nhận bucket của bạn đã empty.
4. Khi Bucket trống, sau đó nhấp vào **Delete** từ thanh menu.
5. Xác nhận Bucket bạn đã xóa.
