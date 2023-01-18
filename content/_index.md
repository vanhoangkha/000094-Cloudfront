+++
title = "CLOUDFRONT WITH S3 BUCKET ORIGIN"
date = 2021
weight = 1
chapter = false
+++

# CLOUDFRONT WITH S3 BUCKET ORIGIN

#### Introduction

This hands-on lab will guide you through the steps to host static web content in an [Amazon S3 bucket](https://aws.amazon.com/s3/) , protected and accelerated by [Amazon CloudFront](https://aws.amazon.com/cloudfront/) . Skills learned will help you secure your workloads in alignment with the [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc).

![example](/images/2/s3_user.png?width=50pc)

#### Prerequisites

- An [AWS account](https://portal.aws.amazon.com/gp/aws/developer/registration/index.html) that you are able to use for testing.

- Permissions to Amazon S3 and Amazon CloudFront.

#### Costs

- Typically less than $1 per month (depending on the number of requests) if the account is only used for personal testing or training, and the tear down is not performed.
- [Amazon S3 pricing](https://aws.amazon.com/s3/pricing/)
- [Amazon CloudFront pricing](https://aws.amazon.com/cloudfront/pricing/)
- [AWS Pricing](https://aws.amazon.com/pricing/)

#### Steps:

- [Create S3 bucket](1.-cloud-front-với-s3/1.1-tạo-nhóm-s3/)
- [Upload example index.html file](1.-cloud-front-với-s3/1.2-tải-lên-tệp-index.html/)
- [Configure Amazon CloudFront](1.-cloud-front-với-s3/1.3-cấu-hình-amazon-cloudfront/)
- [Tear down](1.-cloud-front-với-s3/1.4-dọn-dẹp-tài-nguyên/)

#### References & useful resources

[Amazon S3 Developer Guide Amazon CloudFront Developer Guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)
