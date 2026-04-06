

# CBDAS-Project: AWS S3 Management via CLI

This project demonstrates how to manage Amazon S3 resources using the AWS Command Line Interface (CLI), specifically focusing on bucket creation and object manipulation from a local environment.

---

## 📋 Prerequisites

1.  **AWS CLI Installed:** [Download here](https://aws.amazon.com/cli/).
2.  **IAM Credentials:** An AWS user with `AmazonS3FullAccess`.
3.  **Local Setup:** Configure your terminal by running:
    ```bash
    aws configure
    ```
    *Provide your Access Key, Secret Key, and preferred Region (e.g., `us-east-1`).*

---

## 🚀 Step-by-Step Operations

### 1. Create a Globally Unique Bucket
Replace `your-unique-bucket-name` with a name that hasn't been taken by anyone else in the world.

```bash
aws s3 mb s3://your-unique-bucket-name
```

###2. Upload a Local File to S3To upload a specific file (e.g., data.txt) to the root of your bucket:Bashaws s3 cp data.txt s3://your-unique-bucket-name/
###3. Sync a Local FolderTo upload multiple files and keep your bucket synchronized with a local directory:Bashaws s3 sync ./my-local-folder s3://your-unique-bucket-name/uploads/
##4. Verify UploadsList all files currently residing in your S3 bucket:Bashaws s3 ls s3://your-unique-bucket-name/ --recursive
🛠️ Command Cheat SheetTaskCommandMake Bucketaws s3 mb s3://[bucket-name]Upload Fileaws s3 cp [file] s3://[bucket-name]Download Fileaws s3 cp s3://[bucket-name]/[file] .List Contentsaws s3 ls s3://[bucket-name]Remove Fileaws s3 rm s3://[bucket-name]/[file]Delete Bucketaws s3 rb s3://[bucket-name] --force
