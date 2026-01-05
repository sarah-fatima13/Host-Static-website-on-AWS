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

<img width="1675" height="991" alt="Image" src="https://github.com/user-attachments/assets/ada5698d-4e4d-415a-8fa0-dabcd6f19e83" />

  # 3. Configure S3 for Static Website Hosting
I enabled static website hosting on the S3 bucket. By specifying the index document, the bucket was configured to behave like a web server and serve the website content without running any servers.
<img width="1410" height="272" alt="Image" src="https://github.com/user-attachments/assets/030f4562-a904-40cf-b4cc-193b4c0e9bb1" />

  # 4. Set Public Read Permissions
I configured the bucket policy to allow public read access. This step ensures that website files can be accessed by users through a browser and by CloudFront for content delivery.
<img width="1514" height="713" alt="Image" src="https://github.com/user-attachments/assets/79ab6ad3-a9ed-4339-a333-712979e6249b" />

  # 5. Set Up DNS with Route 53
I configured Amazon Route 53 to manage DNS for the domain. Although the domain was registered with GoDaddy, Route 53 was used to control how the domain routes traffic to AWS resources.
<img width="1655" height="996" alt="Image" src="https://github.com/user-attachments/assets/37ee4ea5-c45e-4f6e-b389-7559e47b81e3" />

  # 6. Request an SSL Certificate (ACM)
I requested an SSL/TLS certificate using AWS Certificate Manager (ACM).This enables HTTPS encryption, ensuring secure communication between users and the website.
<img width="1649" height="912" alt="Image" src="https://github.com/user-attachments/assets/e8d7977c-92a2-4651-a67a-2858a4ff1e8d" />

  # 7. Create a CloudFront Distribution
I created an Amazon CloudFront distribution with the S3 bucket as the origin. CloudFront improves performance by caching and delivering content from edge locations closer to users worldwide.
<img width="1758" height="915" alt="Image" src="https://github.com/user-attachments/assets/4ea70fbe-83c1-495b-a485-b1a132604cd0" />

  # 8. Connect DNS to CloudFront
I linked the custom domain to the CloudFront distribution using Route 53.This ensures that when users enter the domain name, the request is routed to CloudFront, which serves the website securely.
<img width="1811" height="916" alt="Image" src="https://github.com/user-attachments/assets/fb51ce0c-7aee-4b81-9c4a-246bae22dbca" />

  # 9. Test the Website
Finally, I tested the website using the custom domain. This confirmed that S3 hosting, CloudFront delivery, HTTPS security, and DNS configuration were all working correctly.
 <img width="1884" height="1037" alt="Image" src="https://github.com/user-attachments/assets/54212226-0cf0-44f4-97ef-083b273999ff" /> 

 <img width="948" height="932" alt="Image" src="https://github.com/user-attachments/assets/28822ea2-0c76-46a4-ac6e-88d47c4229b3" />
 # Note:
All AWS resources used for this project were deleted after completion to avoid any unintended charges, as the project was created using the AWS Free Tier.
  

