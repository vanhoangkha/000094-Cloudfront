+++
title = "CloudFront với S3"
date = 2021
weight = 1
chapter = false
+++

# CLOUDFRONT VỚI S3

#### Giới thiệu

Bài lab này sẽ hướng dẫn bạn các bước để lưu trữ nội dung web tĩnh trong [Amazon S3 bucket](https://aws.amazon.com/s3/) , được bảo vệ và tăng tốc bởi [Amazon CloudFront](https://aws.amazon.com/cloudfront/) . Các kỹ năng học được sẽ giúp bạn đảm bảo khối lượng công việc của mình phù hợp với [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc).

![example](/images/2/s3_user.png?width=50pc)

#### Điều kiện cần thiết

- Tài khoản [AWS account](https://portal.aws.amazon.com/gp/aws/developer/registration/index.html) mà bạn sử dụng cho bài Lab.

- Tạo quyền IAM với Amazon S3 và Amazon CloudFront.

#### Chi phí

- Thường ít hơn $ 1 mỗi tháng (tùy thuộc vào số lượng yêu cầu)
- [Giá Amazon S3](https://aws.amazon.com/s3/pricing/)
- [Giá Amazon CloudFront](https://aws.amazon.com/cloudfront/pricing/)
- [Giá Amazon](https://aws.amazon.com/pricing/)

#### Steps:

- [Tạo nhóm S3](1.-cloud-front-với-s3/1.1-tạo-nhóm-s3/)
- [Tải lên tệp index.html](1.-cloud-front-với-s3/1.2-tải-lên-tệp-index.html/)
- [Cấu hình Amazon CloudFront](1.-cloud-front-với-s3/1.3-cấu-hình-amazon-cloudfront/)
- [Dọn dẹp tài nguyên](1.-cloud-front-với-s3/1.4-dọn-dẹp-tài-nguyên/)

#### Tài liệu tham khảo

[Amazon S3 & Amazon CloudFront ](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)
