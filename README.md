# 🔍🧠 AWS Rekognition Image Analyzer with Google Colab

This project demonstrates how to securely authenticate with **AWS IAM**, analyze an image using **AWS Rekognition**, and extract meaningful labels such as objects and categories .

---

## 📁 Project Overview

- 🔐 Securely input AWS credentials using `getpass` (hidden input).
- ✅ Validate IAM session with AWS STS to confirm authorized access.
- 🖼️ Load an image from a direct URL.
- 🔄 Convert the image into byte format for Rekognition.
- 🧠 Analyze the image using AWS Rekognition's **Label Detection API**.
- 📝 Extract and print the top labels with confidence scores.

---

## ✅ Requirements

- AWS account with **Rekognition** enabled.
- IAM user with permissions to use Rekognition and STS.
- Your **Access Key ID** and **Secret Access Key**.
- A **direct** URL to an image (must return an image file, not a webpage).

---

## 🔧 Installation

Install `boto3` in your Colab notebook:

```bash
%pip install boto3
```

---

## ⚠️ Important Notes

- The image URL **must be direct** to an image file, **not** a webpage or redirect.
- Rekognition supports images via:
  - Raw bytes (as shown).
  - Images stored in S3 (using `'S3Object': {Bucket, Name}`).
- Avoid hardcoding AWS credentials; always use secure input methods.
- Use least privilege IAM policies for security.
- AWS Rekognition costs apply beyond free tier limits. Monitor usage accordingly.

---

## 📚 References & Resources

- [AWS Rekognition Documentation](https://docs.aws.amazon.com/rekognition/latest/dg/what-is.html)
- [Boto3 Rekognition Client](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/rekognition.html)
- [AWS IAM Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
- [Google Colab](https://colab.research.google.com/)

---
