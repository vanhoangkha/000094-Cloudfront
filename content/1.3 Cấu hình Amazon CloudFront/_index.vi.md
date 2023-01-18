+++
title = "Cấu hình Amazon CloudFront"
date = 2021
weight = 3
chapter = false
pre = "<b> 3. </b>"
+++

Sử dụng Bảng điều khiển quản lý AWS, để tạo **CloudFront distribution** và cấu hình nó để phục vụ **s3 Bucket** mà chúng ta đã tạo trước đó.

1. Mở bảng điều khiển Amazon CloudFront tại https://console.aws.amazon.com/cloudfront/home.
2. Từ bảng điều khiển, nhấn vào **Create distribution**.

![example](/images/2/3/3-create-cf.png?width=90pc)

3. Chỉ định các cài đặt sau đây cho bản distribution:

- Trong trường **Origin domain**, chọn S3 bucket mà bạn đã tạo trước đó.
- Trong trường **Origin access**, chọn **Legacy access identities**
- Trong trường **Bucket policy**, chọn **Yes, update the bucket policy**
- Chọn **Create new OAI**

![example](/images/2/3/3.0-choose-s3.png?width=90pc)

- Chọn **Create**

![example](/images/2/3/3.1-OAI.png?width=90pc)

- Các phần còn lại, để mặc định.

4. Trong phần **Settings**

- Chọn **Use North America, Europe, Asia, Middle East, and Africa** vì Việt Nam trong khu vực **Asia**
- Trọng mục **Default root object - optional**, điền tên file đã upload lên S3 - vào ô trống (VD: index.html)
- Cuộn xuống cuối trang, chọn **Create distribution**

![example](/images/2/3/3.2-asia.png?width=90pc)

- Để quay lại trang CloudFront chọn **Distributions** từ menu điều hướng bên trái.

- Để biết thêm thông tin về các tùy chọn cấu hình khác, xem thêm [CloudFront Web Distribution](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html).

5. Sau khi CloudFront tạo bản phân phối của bạn, có thể mất khoảng vài phút.

- Cột Status & cột Last modified sẽ có thông tin như bên dưới hình.
- Nhấp vào **ID** để lấy **Distribution domain name**

![example](/images/2/3/3.3-status.png?width=90pc)

6. Khi bản phân phối của bạn được triển khai, hãy kiểm tra nội dung tĩnh (index.html) của mình bằng CloudFront **Distribution domain name** mà bạn có thể thấy trong console. Sao chép **domain name** vào browser để kiểm tra.

![example](/images/2/3/3.4-get-name.png?width=90pc)

Kết quả được như hình bên dưới

![example](/images/2/3/3.5-test.png?width=90pc)

Để biết thêm thông tin, xem thêm [Testing Web Distribution](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-testing.html).

7. Kiểm tra thời gian browser tải index.html bằng **Distribution domain name** của CloudFront
- Nhấp chuột phải, chọn **kiểm tra**
- Bên phải trang, chọn **Mạng**
- Nhấn ký hiệu tải lại trang

![example](/images/2/3/3.6-check-cf.png?width=90pc)

- Thời gian từ **389** mili second (khi xem file html qua S3-Object URL) đã giảm còn **8** mili second nhờ truy cập qua CloudFront! Hãy thử tưởng tưởng: web tĩnh của bạn được host tại các **Region US** & có end user tại khu vực **Asian**, thì thời gian trả về kết quả sau 1 cú lích chuột có thể lên tới vài giây hoặc chục giây, điều đó -  sẽ làm ảnh hưởng đến trãi nghiệm người dùng! Nhưng với CloudFront tốc độ sẽ luôn được tối ưu. 

8. Kiểm tra địa điểm của CloudFront **Pop** ([Points of Presence](https://aws.amazon.com/about-aws/global-infrastructure/))
- Nhấp 1 lần vào **domain name** ở giữa trang
- Kiểm tra POP của Cloudfront, vì mình đang truy cập ở Hồ Chi Minh - nên POP là: SGN50-P1 (với SGN là [Saigon](https://en.wikipedia.org/wiki/Tan_Son_Nhat_International_Airport#:~:text=The%20airport's%20IATA%20code%2C%20SGN,Qu%E1%BB%91c%20t%E1%BA%BF%20T%C3%A2n%20S%C6%A1n%20Nh%E1%BA%A5t))

![example](/images/2/3/3.7'-pop.png?width=90pc)

9. Giờ đây, bạn có nội dung trong S3 bucket private mà chỉ CloudFront mới có quyền truy cập an toàn. Sau đó, CloudFront phục vụ các yêu cầu, trở thành một dịch vụ lưu trữ tĩnh an toàn, đáng tin cậy một cách hiệu quả với các tính năng như [custom certificates](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-https.html) và [alternate domain names](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/CNAMEs.html) .

Để biết thêm thông tin về cách cấu hình CloudFront, [update CloudFront Distribution ](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/HowToUpdateDistribution.html).
