+++
title = "Upload example index.html file"
date = 2021
weight = 2
chapter = false
pre = "<b> 2. </b>"
+++

1. Create a simple index.html file, you can create by coping the following text into your favourite text editor.

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

2. Open the Amazon S3 console at https://console.aws.amazon.com/s3/ .
3. In the console click the name of your bucket you just created.

![example](/images/2/2/2.0-choose-s3.png?width=90pc)

4. Click the **Upload** button.

![example](/images/2/2/2.1-upload.png?width=90pc)

5. Star to **Add files**

- Click the **Add files** button, select your index.html file.
- then click the **Upload** button.

![example](/images/2/2/2.2-add-file.png?width=90pc)

![example](/images/2/2/2.3-upload-file.png?width=90pc)

6. Your index.html file should now appear in the list.

![example](/images/2/2/2.4-success.png?width=90pc)

7. Tick on the file already upload success, choose **Open**

![example](/images/2/2/2.5-open.png?width=90pc)

8. Check the period of time for brower loading **index.html**

- Check in the brower has correct **Singapore** (ap-southeast-1)
- Lick rightmost button , choose **Inspect**
- On the right, choose **>>** and choose **Network**
- Lick the icon reload page
- Take note the period of time to the reload page (will use to compare when deploy cloudfront)

![example](/images/2/2/2.6'-open.png?width=90pc)
