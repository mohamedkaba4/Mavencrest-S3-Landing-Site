# Mavencrest Static Site

Personal cloud and security engineering portfolio hosted on AWS using Amazon S3 and CloudFront.

The site showcases cloud infrastructure, systems engineering, security, DevOps, and enterprise architecture projects using a liglhtweight static frontend that allows for fast and reliable global delivery.

## Architecture

```text
User
  |
  v
CloudFront
  |
  v
Private Amazon S3 Bucket
  |
  +-- HTML
  +-- CSS
  +-- JavaScript
  +-- Static Assets (images, media, etc)

Amazon CloudFront serves the site publicly and handles caching, while the S3 bucket remains private and is only accessible through CloudFront.

# Stack
- HTML, CSS, JavaScript
- Amazon S3
- Amazon CloudFront
- Route 53
- AWS Certificate Manager
- Origin Access Control (OAC)

# Highlights
- Secure static website hosting
- Private S3 origin
- CloudFront content delivery and caching
- HTTPS with custom domain
- Responsive portfolio design
- Project and certification showcase

# Purpose
This project serves as the central portfolio for my cloud, infrastructure, security, and DevOps work while demonstrating a simple production-style static hosting architecture on AWS.

