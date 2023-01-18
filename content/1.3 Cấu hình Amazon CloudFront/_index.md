+++
title = "Configure Amazon CloudFront"
date = 2021
weight = 3
chapter = false
pre = "<b> 3. </b>"
+++

Using the AWS Management Console, we will create a CloudFront distribution, and configure it to serve the S3 bucket we previously created.

1. Open the Amazon CloudFront console at https://console.aws.amazon.com/cloudfront/home .
2. From the console dashboard, click **Create distribution**.

![example](/images/2/3/3-create-cf.png?width=90pc)

3. Specify the following settings for the distribution:

- In the **Origin domain** field Select the S3 bucket you created previously.
- In the **Origin access**, choose **Legacy access identities**
- In the **Bucket policy**, choose **Yes, update the bucket policy**
- Choose **Create new OAI**

![example](/images/2/3/3.0-choose-s3.png?width=90pc)

- Choose **Create**

![example](/images/2/3/3.1-OAI.png?width=90pc)

- Another field, let it default

4. In the **Settings**

- Choose **Use North America, Europe, Asia, Middle East, and Africa** because, Vietnam in **Asia**
- In the **Default root object - optional**, input file already upload on S3 (Fx: index.html)
- Scroll down last page, choose **Create distribution**

![example](/images/2/3/3.2-asia.png?width=90pc)

- To return to the main CloudFront page click **Distributions** from the left navigation menu.

- For more information on the other configuration options, see [Values That You Specify When You Create or Update a Web Distribution](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html) in the CloudFront documentation.

5. After CloudFront creates your distribution which may take approximately a few minutes

- Column Status & Column Last modified has infomation like below.
- Lick on **ID** to get **Distribution domain name**

![example](/images/2/3/3.3-status.png?width=90pc)

6. When your distribution is deployed, confirm that you can access your content using your new CloudFront **Distribution domain name** which you can see in the console. Copy the Domain Name into a web browser to test.

![example](/images/2/3/3.4-get-name.png?width=90pc)

Result like below

![example](/images/2/3/3.5-test.png?width=90pc)

For more information, [see Testing a Web Distribution](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-testing.html) in the CloudFront documentation.

7. Check the period of time for brower loading index.html by **Distribution domain name** of CloudFront

- Lick rightmost button , choose **Inspect**
- On the right, choose **>>** and choose **Network**
- Lick the icon reload page

![example](/images/2/3/3.6'-check-cf.png?width=90pc)

- Time from **110** milliseconds (when viewing html files via S3-Object URL) has been reduced to **9** milliseconds by to access via CloudFront! Imagine: your static web is hosted in **Region US** & has end user in **Asian**, the time to return results after 1 mouse click can be up to a few seconds or tens of seconds, that - will affect the user experience! But with CloudFront speed will always be optimal.

8. Check the location of CloudFront **Pop**([Points of Presence](https://aws.amazon.com/about-aws/global-infrastructure/))

- Click one time in **domain name** central page
- Check POP - Cloudfront, i request from Ho Chi Minh - so POP is: SGN50-P1 (with SGN is [Saigon](https://en.wikipedia.org/wiki/Tan_Son_Nhat_International_Airport#:~:text=The%20airport's%20IATA%20code%2C%20SGN,Qu%E1%BB%91c%20t%E1%BA%BF%20T%C3%A2n%20S%C6%A1n%20Nh%E1%BA%A5t))

![example](/images/2/3/3.7-pop.png?width=90pc)

9. You now have content in a private S3 bucket, that only CloudFront has secure access to. CloudFront then serves the requests, effectively becoming a secure, reliable static hosting service with additional features available such as [custom certificates](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-https.html) and alternate [domain names](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/CNAMEs.html) .

For more information on configuring CloudFront, see [Viewing and Updating CloudFront Distributions](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/HowToUpdateDistribution.html) in the CloudFront documentation.
