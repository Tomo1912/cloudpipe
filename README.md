# 🚀 CloudPipe - Automated CI/CD Pipeline

Automated deployment pipeline using GitHub Actions + AWS S3. Push code → Auto deploy!

## 🎯 What It Does

- ✅ Push to GitHub → Automatically deploys to AWS S3
- ✅ No manual uploads
- ✅ Fast & reliable deployments
- ✅ 100% FREE (using free tiers)

## 🛠️ Tech Stack

- GitHub Actions (CI/CD)
- AWS S3 (Hosting)
- HTML/CSS/JavaScript

## ⚡ Quick Setup

### 1. Create S3 Bucket
```bash
# AWS Console → S3 → Create bucket
# Name: cloudpipe-demo-yourname
# Region: us-east-1
# Uncheck "Block all public access"
# Enable "Static website hosting"
```

### 2. Bucket Policy
```json
{
    "Version": "2012-10-17",
    "Statement": [{
        "Effect": "Allow",
        "Principal": "*",
        "Action": "s3:GetObject",
        "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }]
}
```

### 3. Create IAM User
- IAM → Users → Create user
- Attach: `AmazonS3FullAccess`
- Create access key → Save credentials

### 4. GitHub Secrets
Add in Settings → Secrets:
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `S3_BUCKET_NAME`

### 5. Deploy!
```bash
git push origin main
```

## 📊 Results

**Before:** 15-20 min manual deployment  
**After:** 20 seconds automated ⚡

**Cost:** $0.00 💰

---

Built to demonstrate modern DevOps practices 🚀

