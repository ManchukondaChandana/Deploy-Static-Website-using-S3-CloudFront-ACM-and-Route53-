** Deploy-Static-Website-using-S3-CloudFront-ACM-and-Route53 **
This project showcases how to deploy a static website securely using Amazon S3, CloudFront, ACM, and Route 53, all mapped to a custom domain: youtubeclone-p1.tk.
Step 1: Create an index.html file. I wrote a code for youtube clone with basic html and css, in which I used to host that website using cloud.


**Services:**
<li>Amazon S3 – Static file storage
CloudFront – CDN with HTTPS
AWS Certificate Manager (ACM) – SSL certificate
Route 53 – DNS and domain mapping
Custom Domain – youtubeclone-p1.tk</li>


**Workflow:**
1) S3 Bucket Creation:
    Create a New Bucket:
  Click on the "Create bucket" button.
  Enter a unique name for your bucket.
  Choose a region for your bucket. Choosing a region closest to your target audience is recommended   for better performance.
  Click on "Create bucket" to create your S3 bucket.
2) Configure Bucket Settings:
Once the bucket is created, click on its name to open its settings.
Configure the bucket for static website hosting:
Go to the "Properties" tab of your bucket.
Scroll down to "Static website hosting" and click on "Edit".
Choose "Use this bucket to host a website" and enter the index document (e.g., index.html).
Click "Save changes" to save the configuration.
  

3) SSL Certificate with ACM

  <li>Region: us-east-1 (Northern Virginia)
  Validation: DNS (via Route 53)</li>

3)Route 53 Setup

  <li>Created Public Hosted Zone for youtubeclone-p1.tk
  Configured name servers in the domain registrar
  Validated ACM SSL
  Added A Record with alias to CloudFront distribution</li>

  

