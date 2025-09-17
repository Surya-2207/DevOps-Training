# Task 4: Infrastructure Automation and Configuration Management

## Overview
This task demonstrates the use of Terraform for infrastructure provisioning and Ansible for configuration management. It includes files for managing cloud resources, automating server setup, and deploying a simple web application.

## Screenshots

<img width="867" height="621" alt="Screenshot 2025-09-17 134623" src="https://github.com/user-attachments/assets/36d39049-d53f-42c2-b32f-0b60959b1f03" />

---

<img width="1366" height="724" alt="Screenshot 2025-09-17 134506" src="https://github.com/user-attachments/assets/502fd8a0-9c18-4c5a-b468-5f5da0806a8d" />


## Contents
- `index.html`: Sample web page to be deployed.
- `inventory`: Ansible inventory file listing target hosts.
- `main.tf`: Terraform configuration for provisioning infrastructure.
- `site.yml`: Ansible playbook for configuring servers and deploying the web application.
- `surya.pem`: Private key for SSH access to provisioned servers.
- `terraform-key.pub`: Public key for server authentication.
- `terraform.tfstate`, `terraform.tfstate.backup`: Terraform state files tracking infrastructure resources.

## Usage
### 1. Provision Infrastructure with Terraform
1. Ensure you have Terraform installed.
2. Initialize Terraform:
   ```powershell
   terraform init
   ```
3. Apply the configuration to create resources:
   ```powershell
   terraform apply
   ```

### 2. Configure Servers with Ansible
1. Ensure you have Ansible installed (use WSL or a compatible environment).
2. Run the playbook:
   ```bash
   ansible-playbook -i inventory --private-key surya.pem site.yml
   ```

### 3. Access the Web Application
- After successful deployment, access the web application using the public IP of the provisioned server.

## Notes
- Update the `inventory` file with the correct IP addresses of your servers.
- Keep your private key (`surya.pem`) secure.
- Review and customize `main.tf` and `site.yml` as needed for your environment.



