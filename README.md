
## Files

- **s3.tf**: Defines the S3 bucket and related resources.
- **cloudfront.tf**: Defines the CloudFront distribution and related resources.
- **provider.tf**: Configures the AWS provider.
- **index.html**: HTML content.

## Prerequisites

- [Terraform](https://www.terraform.io/downloads.html) installed.
- AWS account with appropriate permissions.
- AWS CLI configured with your credentials.

## Setup

1. **Clone the repository**:
    ```sh
    git clone https://github.com/connectrajesh/aws-static-website.git
    cd aws-static-website
    ```

2. **Initialize Terraform**:
    ```sh
    terraform init
    ```
3. **Plan Terraform**:
    ```sh
    terraform plan
    ```   

4. **Apply the Terraform configuration**:
    ```sh
    terraform apply
    ```

    This will create the necessary AWS resources, including an S3 bucket, CloudFront distribution, and CloudWatch log group.

## AWS Resources

### S3 Bucket

The S3 bucket is configured to host the static website. The index.html file is uploaded to this bucket.

### CloudFront Distribution

CloudFront is used to serve the content from the S3 bucket. It provides caching and improves the performance of the website.

## Outputs

After applying the Terraform configuration, the CloudFront domain name will be output. You can use this domain name to access your static website.

## Clean Up

To destroy the infrastructure created by Terraform, run:

```sh
terraform destroy
