# 🌐 Static Portfolio Website Hosted on AWS S3

## 📖 Project Overview
A professional portfolio website hosted on **Amazon S3**, demonstrating cost-effective, highly available, and scalable cloud hosting solutions.

## 🎯 Live Demo
**Visit my live portfolio:** [http://estherdomfeh-portfolio-423.s3-website.af-south-1.amazonaws.com](http://yourname-portfolio-123.s3-website-af-south-1.amazonaws.com)

## 🏗️ Architecture
![Architecture Diagram](images/architecture.png)

**Technical Stack:**
- **Frontend:** HTML5, CSS3, JavaScript
- **Cloud:** Amazon S3 (Static Website Hosting)
- **Security:** IAM Bucket Policies, S3 Versioning
- **Region:** af-south-1 (Africa Cape Town)

## 📊 AWS Services & Features Used

| Service | Feature | Purpose |
|---------|---------|---------|
| **Amazon S3** | Static Website Hosting | Primary website hosting |
| **Amazon S3** | Bucket Policies | Public read access control |
| **Amazon S3** | Versioning | Data protection & recovery |
| **AWS IAM** | Resource Policies | Security permissions |

## 🚀 Deployment Status
✅ **Website Successfully Deployed**  
✅ **Public Access Configured**  
✅ **Versioning Enabled**  
✅ **Cost Optimization Active**  

## 💰 Cost Analysis
- **S3 Storage:** ~$0.023/GB per month
- **Data Transfer:** ~$0.09/GB for first 10TB
- **Requests:** ~$0.005 per 10,000 requests
- **Estimated Monthly Cost:** **<$1.00**

## 🔧 Technical Implementation

### Deployment Commands (AWS CLI)
```bash
# Create bucket with versioning
aws s3 mb s3://yourname-portfolio-123 --region af-south-1

# Configure static website hosting
aws s3 website s3://yourname-portfolio-123 --index-document index.html --error-document index.html

# Upload files with public read access
aws s3 sync . s3://yourname-portfolio-123 --acl public-read

# Verify deployment
aws s3 ls s3://yourname-portfolio-123 --recursive