# Static Website Hosting with Amazon S3 + CloudFront

A hands-on AWS project where I deployed a static website using **Amazon S3**
for storage and **Amazon CloudFront** as a global content delivery network
(CDN), secured with **Origin Access Control (OAC)**.

## What I built

- Created an **S3 bucket** to store the website's static files (HTML/CSS)
- Set up a **CloudFront distribution** to serve the site globally with
  low latency
- Configured **Origin Access Control (OAC)** so the S3 bucket stays
  **private** — visitors can only reach the website through CloudFront,
  not by accessing the S3 bucket directly. This is a real-world AWS
  security best practice.

## Architecture

```
Visitor Browser
      |
      v
Amazon CloudFront (CDN)
      |  (Origin Access Control)
      v
Amazon S3 Bucket (private, static files)
```

## Why this setup matters

- **S3** provides durable, cheap storage for static website files
- **CloudFront** caches and serves content from edge locations closer to
  users, making the site load faster worldwide
- **OAC** prevents anyone from bypassing CloudFront and accessing the S3
  bucket directly, closing off a common misconfiguration/security gap in
  real-world cloud deployments

## Live Demo

The site is live and publicly accessible via the CloudFront URL:
`<add your CloudFront URL here>`

## What I learned

- How to create and configure an S3 bucket for static website content
- How to set up a CloudFront distribution pointing to an S3 origin
- Why direct public access to S3 buckets is a security risk, and how
  Origin Access Control (OAC) solves it
- The basics of how CDNs improve website performance and reliability
