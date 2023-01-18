+++
title = "Tạo S3 bucket"
date = 2021
weight = 1
chapter = false
pre = "<b> 1. </b>"
+++

Tạo Amazon S3 để lưu trữ nội dung tĩnh bằng bảng điều khiển Amazon S3. Để biết thêm thông tin về [Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html) .

1. Mở trang Amazon S3 console at https://console.aws.amazon.com/s3/.
2. Từ console , chọn nút **Create bucket**.

![example](/images/2/1/1.0-create-s3-new.png?width=90pc)

- Tại mục Bucket name: điền ```doc-example-bucket-111```

- Tại mục AWS Region: chọn **Asia Pacific (Singapore)ap-southeast-1**

![example](/images/2/1/1.1-create-s3-bucket.png?width=90pc)


3. Đặt tên cho  **Bucket name** của bạn, nhập tên và tuân thủ quy định dưới dây cho Bucket. Thực hiện theo các nguyên tắc đặt tên sau:

- Tên phải là duy nhất trên tất cả các Bucket hiện có trong **Amazon S3**.
- Tên không được chứa các ký tự viết hoa.
- Tên phải bắt đầu bằng chữ thường hoặc số.
- Tên phải dài từ 3 đến 63 ký tự.

4. Chọn **Region** gần bạn để giảm thiểu độ trễ và chi phí, hoặc để giải quyết các yêu cầu quy định. Lưu ý rằng đối với ví dụ này, chúng ta sẽ chấp nhận cài đặt mặc định và Bucket này được bảo mật theo mặc định. Xem xét bật các tùy chọn bảo mật bổ sung như ghi nhật ký và mã hóa, [Bảo vệ dữ liệu trong Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/DataDurability.html) .

5. Ở ví dụ này, 
- Chúng ta giữ nguyên mặc định **Block all public access** 

![example](/images/2/1/1.3-block.png?width=90pc)

6. Tại mục **bucket versioning** 
- **Enable** [bucket versioning](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Versioning.html) , để giữ nhiều phiên bản của objects để bạn có thể khôi phục object nếu bạn vô tình sửa đổi hoặc xóa nó.
- Chọn **Create bucket**

![example](/images/2/1/1.4-version-s3.png?width=90pc)






