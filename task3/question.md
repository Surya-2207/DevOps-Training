XOps Microchallenge #3 – "CI/CD Pipeline in Action!"
Dear Learners,
 
Ready to take your DevOps skills to the next level?
This time, you're building a real CI/CD pipeline using GitHub Actions that automatically deploys your web app on AWS EC2!
 
Title:
🛠️ Build a CI/CD Pipeline That Automatically Deploys a Web App on EC2
 
Objective:
Create a fully working CI/CD pipeline using GitHub Actions that:
Builds a simple web app (HTML or Node.js or Python Flask — your choice)
Pushes the code to GitHub
Automatically connects to an EC2 instance (via SSH)
Deploys the code and restarts the web server
What You’ll Learn:
Basics of CI/CD automation with GitHub Actions
SSH-based deployment (no cloud-native complexity yet)
GitHub secrets & secure credential management
Script-based deployment practices (real-world stuff!)
EC2 setup, web server hosting, and service restart automation
Fundamentals of continuous delivery mindset
Step-by-Step Challenge Guide
1. Prepare Your EC2 Web Server
Launch an EC2 instance (Amazon Linux 2 or Ubuntu)
Install a basic web server (e.g., NGINX or Apache)
Add a placeholder file at /var/www/html/index.html or in /opt/app/
Make sure port 80 is open in the Security Group
Create a .pem key OR username/password to SSH (use GitHub Secrets securely)
2. Build a Simple Web App
Create a small app folder with 1–2 files:
index.html or app.py (Flask) or server.js (Node.js)
Add a README.md explaining the setup
Push the project to a GitHub repo
3. Create a GitHub Actions Workflow
On code push to main:
SSH into the EC2 instance
Copy the latest code using scp or rsync
Replace existing app folder
Restart the web server if needed (e.g., sudo systemctl restart nginx)
Use GitHub Secrets to store:
EC2_PUBLIC_IP
SSH_USERNAME
SSH_PRIVATE_KEY (secure string format)
4. Deliverables
Working GitHub Actions YAML file
Deployed web page visible via EC2 public IP
Screenshots of:
Web app output
GitHub Actions pipeline success
GitHub repo structure
All pushed to your GitHub repo
Share your repo link in Teams with ✅ once done
Prerequisites
EC2 instance (Free Tier)
GitHub account with Actions enabled
Basic understanding of shell scripting
Comfort using GitHub Secrets