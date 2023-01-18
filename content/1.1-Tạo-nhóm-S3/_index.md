+++
title = "Create S3 bucket"
date = 2021
weight = 1
chapter = false
pre = "<b> 1. </b>"
+++

Create an Amazon S3 bucket to host static content using the Amazon S3 console. For more information about Amazon S3, see [Introduction to Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html) .

1. Open the Amazon S3 console at https://console.aws.amazon.com/s3/ .
2. From the console dashboard, choose **Create bucket**.

![example](/images/2/1/1.0-create-s3-new.png?width=90pc)
- In the Bucket name: input ```doc-example-bucket-111```

- In the AWS Region: choose **Asia Pacific (Singapore)ap-southeast-1**
![example](/images/2/1/1.1-create-s3-bucket.png?width=90pc)

3. Enter a **Bucket name** for your bucket, type a unique DNS-compliant name for your new bucket. Follow these naming guidelines:

- The name must be unique across all existing bucket names in Amazon S3.
- The name must not contain uppercase characters.
- The name must start with a lowercase letter or number.
- The name must be between 3 and 63 characters long.

4. Choose an AWS Region where you want the bucket to reside. Choose a Region close to you to minimize latency and costs, or to address regulatory requirements. Note that for this example we will accept the default settings and this bucket is secure by default. Consider enabling additional security options such as logging and encryption, the S3 documentation has additional information such as [Protecting Data in Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/DataDurability.html) .

5. In this lab, 
- Keep default **Block all public access** 

![example](/images/2/1/1.3-block.png?width=90pc)

6. In the **bicket versioning** 
- **Enable** [bucket versioning](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Versioning.html) , to keep multiple versions of an object so you can recover an object if you unintentionally modify or delete it.
- Click **Create bucket**.

![example](/images/2/1/1.4-version-s3.png?width=90pc)