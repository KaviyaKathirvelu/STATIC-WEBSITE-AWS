# Building a Static Website with Terraform: Step-by-Step Guide

Creating and hosting a static website has never been easier with the power of Infrastructure as Code (IaC) and cloud services. In this guide, we'll walk you through setting up a static website using Terraform to manage AWS resources. You'll learn how to automate the creation of an S3 bucket, configure it for static website hosting, deploy your website files, and some additional considerations.

# Prerequisites

Before we start, ensure you have the following:
• An AWS account.
• AWS CLI installed and configured with appropriate permissions.
• Terraform installed.

Step 1: Initialize Your Project:

Create a new directory for your Terraform project and navigate to it:
> mkdir my-static-website
> cd my-static-website

Step 2: Define Your Terraform Configuration:

Create a file named terraform.tf and define your provider configuration. This configuration sets up Terraform to use the AWS provider, specifying your AWS profile and region.

Step 3: Create the S3 Bucket:

Create a file named bucket.tf to define your S3 bucket and its configuration. This defines an S3 bucket and uploads an index.html file to it, configuring the bucket for static website hosting.

Step 4: Set Bucket Policies:

Create a file named policy.tf to define your S3 bucket policies for public access. This ensures your bucket's objects are publicly accessible.

Step 5: Output the Website URL:

Create a file named output.tf to output your website's URL. This outputs the URL of your hosted static website after deployment.

Step 6: Deploy Your Static Website:

   1. Initialize Terraform:
      >  terraform init
      This command prepares your working directory for other Terraform commands.

   2. Apply the Configuration:
      > terraform apply
      Review the changes and confirm with yes.

  3. Access Your Website:

     After the apply process completes, Terraform will output your website's URL. Visit this URL to see your static website live.

# Additional Considerations

• Custom Domain: To use a custom domain for your static website, you can set up Route 53 for DNS management and CloudFront for CDN and SSL/TLS termination.

• Versioning and Backup: Enable versioning on your S3 bucket to maintain backups of your files. This helps in case of accidental deletion or modification.

• Security: Review and implement appropriate security measures, such as bucket policies and IAM roles, to restrict access and protect your resources.

• Monitoring and Logging: Set up S3 access logging and CloudWatch alarms to monitor and manage your static website's performance and availability.

# Conclusion

Congratulations! You've successfully deployed a static website using Terraform on AWS. By leveraging Infrastructure as Code, you can manage your resources efficiently and ensure consistency across deployments. This approach not only saves time but also enhances scalability and maintainability for your projects.

Feel free to explore thr results in my blog (https://dev.to/kaviya_kathirvelu_0505/building-a-static-website-with-terraform-step-by-step-guide-38c6).







