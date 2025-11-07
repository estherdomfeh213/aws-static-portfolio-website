# Project Showcase: Static S3 Portfolio

## Business Impact
- **Cost Reduction:** ~90% cheaper than traditional hosting
- **Availability:** 99.9% AWS SLA guarantee  
- **Scalability:** Handles traffic spikes automatically
- **Global Reach:** Can be enhanced with CloudFront CDN

## Technical Decisions & Justifications

| Decision | Why I Chose This | Alternative Considered |
|----------|------------------|------------------------|
| **S3 Static Hosting** | Cost-effective for static sites | EC2 (overkill, expensive) |
| **af-south-1 Region** | Demonstrate regional awareness | us-east-1 (default) |
| **Bucket Versioning** | Data protection & recovery | No versioning (risky) |
| **Public Bucket Policy** | Required for web access | Keeping private (won't work) |

## Lessons Learned
1. **S3 website endpoints don't support HTTPS** - need CloudFront for SSL
2. **Bucket names must be globally unique** - learned to include randomness
3. **Public access requires explicit bucket policies** - security learning
4. **Versioning protects against accidental deletions** - best practice

## Interview Talking Points
- "I reduced hosting costs by 90% using S3 static hosting vs traditional VPS"
- "Implemented proper security through S3 bucket policies and versioning"
- "Designed for high availability leveraging AWS's global infrastructure"
- "Can easily scale this architecture to millions of users with CloudFront"