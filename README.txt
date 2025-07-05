Cloud Storage Setup using AWS S3

## ✅ Deliverables
- S3 bucket: `my-cloud-bucket-storage`
- Public access configured using bucket policy
- Example files uploaded: `image.jpg`, `doc.pdf`, `notes.txt`
- Encryption enabled: **SSE-S3** (Amazon managed keys)
- Object Ownership: **Bucket owner enforced**

## 🔓 Public Access Example
URL: https://my-cloud-bucket-storage.s3.amazonaws.com/image.jpg

## 🛡️ Access Policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-cloud-bucket-storage/*"
    }
  ]
}
yaml
Copy
Edit

---

### 4. ⬆️ Push the Project to GitHub (if not done yet)

If your folder has:
- `README.md`
- Screenshot of S3 Console or example files
- Optional `bucket-policy.json`

You can push it with:

```bash
git init
git remote add origin https://github.com/yourusername/cloud-storage-s3.git
git add .
git commit -m "Initial commit: S3 Cloud Storage setup"
git push -u origin main