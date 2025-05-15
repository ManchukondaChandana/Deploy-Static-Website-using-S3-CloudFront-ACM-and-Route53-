#Deploy-Static-Website-using-S3-CloudFront-ACM-and-Route53

This project showcases how to deploy a static website securely using Amazon S3, CloudFront, ACM, and Route 53, all mapped to a custom domain: youtubeclone-p1.tk.

**Services**
<li>Amazon S3 – Static file storage
CloudFront – CDN with HTTPS
AWS Certificate Manager (ACM) – SSL certificate
Route 53 – DNS and domain mapping
Custom Domain – youtubeclone-p1.tk</li>

**Workflow:**
##Step1: Create an index.html file. I wrote a code for youtube clone with basic html and css, in which I used to host that website using cloud.

##Step2: S3 Bucket Creation:
    **1. Create a New Bucket:**
        - Click on the "Create bucket" button.
        - Enter a unique name for your bucket.
        - Choose a region for your bucket. Choosing a region closest to your target audience is             recommended   for better performance.
        - Click on "Create bucket" to create your S3 bucket.
    **2. Configure Bucket Settings:**
        - Once the bucket is created, click on its name to open its settings.
        - Configure the bucket for static website hosting:
        - Go to the "Properties" tab of your bucket.
        - Scroll down to "Static website hosting" and click on "Edit".
        - Choose "Use this bucket to host a website" and enter the index document (e.g., 
          index.html).
        - Click "Save changes" to save the configuration.
    **3.  Set Bucket Policy for Public Access:**
         - In the bucket settings, go to the "permissions" tab.
         - Scroll down to "Bucket policy" and clik on "Edit"
         - Add a bucket policy for public read access.
 ##Step3: SSL Certificate with ACM

          - Region: us-east-1 (Northern Virginia)
          - Validation: DNS (via Route 53)

 ##Step4: Route 53 Setup

          -Created Public Hosted Zone for youtubeclone-p1.tk
          -Configured name servers in the domain registrar
          -Validated ACM SSL
          -Added A Record with alias to CloudFront distribution

 ##Step5:  CoudFront Distribution

          -Set origin domain as the private S3 bucket
          -Enabled OAC to restrict direct access
          -Redirected HTTP to HTTPS
          -Added youtubeclone-p1.tk as CNAME
          -Selected the validated SSL cert from ACM
          -Enabled caching (optimized for static content)
          -Default object: index.html

From this project I have learned
-Domain and DNS mapping via Route 53
-HTTPS setup using ACM
-Using S3 and cloudfront Securely
-Practical static site deployment using AWS services

  

