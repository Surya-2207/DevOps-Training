# Task 7: XOps Microchallenge #4 – Infrastructure as Code + Configuration Management Combo

## Objective
Provision an AWS EC2 instance using Terraform and configure it with Ansible to deploy a simple web app (NGINX + custom index.html).

---

## Files
- `main.tf`: Terraform configuration for AWS EC2
- `inventory`: Ansible inventory file
- `site.yml`: Ansible playbook to install NGINX and deploy web page
- `index.html`: Custom web page

---

## Prerequisites
- AWS account and credentials configured
- Terraform installed
- Ansible installed
- SSH key pair for EC2 access

---

## Steps

### 1. Provision EC2 with Terraform
1. Update `main.tf` with your key pair and public key path.
2. Run:
   ```powershell
   terraform init
   terraform apply
   ```
3. Note the EC2 public IP from Terraform output.

### 2. Configure EC2 with Ansible
1. Update `inventory` file with EC2 public IP:
   ```
   [web]
   <EC2_PUBLIC_IP> ansible_user=ec2-user ansible_ssh_private_key_file=~/.ssh/<your-key>.pem
   ```
2. Run the playbook:
   ```powershell
   ansible-playbook -i inventory site.yml
   ```

### 3. Test Deployment
- Open browser and visit `http://<EC2_PUBLIC_IP>`
- You should see the custom web page served by NGINX

---

## Screenshots to Include
- EC2 instance running in AWS Console
- NGINX serving the custom page in browser
- Ansible playbook run output

---

## Notes
- Security group allows SSH (22) and HTTP (80)
- User data installs Python3 for Ansible
- Playbook installs and starts NGINX, copies `index.html`

---

## Troubleshooting
- Ensure your key pair permissions are correct (`chmod 400` on Linux/macOS)
- If Ansible fails to connect, check security group and SSH key
- For Amazon Linux 2, use `ec2-user` as the SSH user

---

Happy Automating!
