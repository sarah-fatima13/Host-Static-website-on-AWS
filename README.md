# Host-Static-website-on-AWS
# Project Overview:
The cloud is perfect for hosting static websites that require no server-side processing.This AWS project hosts a static HTML website on AWS using a secure and scalable cloud architecture. The website contains only HTML files and does not require any backend or server-side processing.
The website is stored in an Amazon S3 bucket configured for static website hosting. Amazon CloudFront is used to deliver content efficiently through a global content delivery network, ensuring low latency and high availability. A custom domain registered with GoDaddy is integrated using Amazon Route 53, and HTTPS security is enabled using AWS Certificate Manager (ACM). This architecture ensures fast content delivery, secure access, and reliable availability, making it suitable for hosting simple static websites on AWS.
# File Summary:
* **Sarah_Fatima_resume_2_.html** – Main HTML file of the website.
* **architecture diagram/** – Architectural diagram explaining the AWS setup.
* **bucket_policy.json** – S3 bucket policy used to configure public access and permissions.
* **demo_site_images/** – Working images of the project showing successful website deployment and functionality.
# Architectural diagram:
<img width="1238" height="313" alt="Image" src="https://github.com/user-attachments/assets/ad79f13d-7aac-419b-998b-8bf64453129d" />

# Project steps(working):
  # 1. Prepare Static Website Files
Created the static website content using HTML. Since the website does not require any backend or server-side processing, the HTML file serves as the complete website and forms the foundation of the project.
  # 2. Create an S3 Bucket & Upload Files
Created an Amazon S3 bucket to store the website files. The bucket acts as the storage layer for the website, and all static files were uploaded to this bucket so they can be served to users.
  # 3. Configure S3 for Static Website Hosting
I enabled static website hosting on the S3 bucket. By specifying the index document, the bucket was configured to behave like a web server and serve the website content without running any servers.
  # 4. Set Public Read Permissions
I configured the bucket policy to allow public read access. This step ensures that website files can be accessed by users through a browser and by CloudFront for content delivery.
  # 5. Set Up DNS with Route 53
I configured Amazon Route 53 to manage DNS for the domain. Although the domain was registered with GoDaddy, Route 53 was used to control how the domain routes traffic to AWS resources.
  # 6. Request an SSL Certificate (ACM)
I requested an SSL/TLS certificate using AWS Certificate Manager (ACM).This enables HTTPS encryption, ensuring secure communication between users and the website.
  # 7. Create a CloudFront Distribution
I created an Amazon CloudFront distribution with the S3 bucket as the origin. CloudFront improves performance by caching and delivering content from edge locations closer to users worldwide.
  # 8. Connect DNS to CloudFront
I linked the custom domain to the CloudFront distribution using Route 53.This ensures that when users enter the domain name, the request is routed to CloudFront, which serves the website securely.
  # 9. Test the Website
Finally, I tested the website using the custom domain. This confirmed that S3 hosting, CloudFront delivery, HTTPS security, and DNS configuration were all working correctly.
  
  

