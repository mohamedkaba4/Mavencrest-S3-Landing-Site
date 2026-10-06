# Mavencrest Static Site

Personal cloud and Infrastructure engineering portfolio hosted on AWS using Amazon S3 and CloudFront. The site uses a lightweight static frontend (S3) for fast, reliable global delivery, with a GitHub Actions CI/CD pipeline that allows quick production updates directly from local dev through a simple Git push.

## Architecture

```text
Local Development
  |
  v
Git Push
  |
  v
GitHub Actions
  |
  v
AWS OIDC / IAM Role
  |
  v
Private S3 Bucket
  |
  v
CloudFront
  |
  v
Route 53 + HTTPS
```

CloudFront is the public entry point and serves cached content globally. The S3 bucket remains private and is accessed only through Origin Access Control (OAC).

## Stack

- HTML, CSS, JavaScript
- Amazon S3
- Amazon CloudFront
- Route 53
- AWS Certificate Manager
- AWS IAM
- GitHub Actions
- OpenID Connect (OIDC)

## CI/CD

Pushes to the `main` branch automatically authenticate to AWS using OIDC, deploy updated site files to S3, and invalidate the CloudFront cache.

## Highlights

- Private S3 origin
- CloudFront global content delivery
- HTTPS custom domain
- Automated deployments from local Git pushes
- OIDC-based AWS authentication
- Automated CloudFront cache invalidation

## Purpose

This project serves as the central portfolio for my cloud, infrastructure, security, and DevOps work while demonstrating practical experience with AWS hosting, IAM, DNS, TLS, CDN architecture, and CI/CD automation.
