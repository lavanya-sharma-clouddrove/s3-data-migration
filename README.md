# Terraform AWS Deployment

This repository contains Terraform code to deploy AWS s3 data migration code , cross account

# Prerequisites
- Terraform >= 1.0.0
- AWS CLI configured with appropriate credentials
- Create a terraform.tfvars files and define variables in that.
```hcl
region = "<region>"
bucket_names = [
  "<bucket1-name>",
  "<bucket1-name>",
 ....
]
principal_arn = "<arn of your main account iam>"
```
# Usage
Follow these steps to deploy the infrastructure:

## Initialize Terraform
```bash
terraform init
```
This command initializes Terraform, downloads providers, and prepares your working directory.

## Plan the Deployment
```bash
terraform plan -out=tfplan
```
This creates an execution plan and saves it to the tfplan file. Review the plan carefully to ensure it matches your expectations.

## Apply the Configuration
```bash
terraform apply tfplan
```
This applies the changes required to reach the desired state of the configuration.

🛠️Happy Terraform, Happy Deploying🚀
