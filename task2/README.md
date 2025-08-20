# AWS EC2 Web Server with Terraform

This project provisions an AWS EC2 instance running a web server using Terraform. It creates a VPC, subnet, internet gateway, route table, security group, and an EC2 instance with Apache HTTP server installed.

## Prerequisites

- [Terraform](https://www.terraform.io/downloads.html) v1.12.2 or later
- AWS account and credentials configured
- An existing EC2 key pair (update `key_name` in [`main.tf`](main.tf) as needed)

## Files

- [`main.tf`](main.tf): Main Terraform configuration
- [`output.tf`](output.tf): Output values (e.g., public IP)
- `.terraform.lock.hcl`: Provider dependency lock file
- `terraform.tfstate` / `terraform.tfstate.backup`: Terraform state files

## Usage

1. **Initialize Terraform:**
   ```sh
   terraform init
   ```

2. **Review the execution plan:**
   ```sh
   terraform plan
   ```

3. **Apply the configuration:**
   ```sh
   terraform apply
   ```
   Confirm when prompted.

4. **Get the public IP:**
   After apply, the public IP of the EC2 instance will be shown as output or can be found in the AWS console.



## Cleanup

To destroy all resources:
```sh
terraform destroy
```
