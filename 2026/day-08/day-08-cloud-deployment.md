# Update system packages

sudo apt update && sudo apt upgrade -y

# Install Nginx

sudo apt install nginx -y

# Start and enable Nginx service

sudo systemctl start nginx
sudo systemctl enable nginx

# Check Nginx status

systemctl status nginx

# View Nginx logs

sudo tail -n 50 /var/log/nginx/access.log
sudo tail -n 50 /var/log/nginx/error.log

# Save logs to a file

sudo cat /var/log/nginx/access.log /var/log/nginx/error.log > nginx-logs.txt

# Download logs to local machine (AWS)

scp -i your-key.pem ubuntu@<your-instance-ip>:~/nginx-logs.txt .

# Download logs to local machine (Utho)

scp root@<your-instance-ip>:~/nginx-logs.txt .

# Security Group Challenges Faced

Nginx page not opening in browser
→ Fixed by allowing port 80 (HTTP) in the cloud security group/firewall.

Permission denied while accessing Nginx logs
→ Solved using sudo to read files inside /var/log/nginx.

Service not starting automatically after reboot
→ Resolved by enabling Nginx using systemctl enable nginx.

# What I Learned

→ How to launch and access a cloud server using SSH

→ Installing and managing services with systemctl

→ Importance of security group rules for web access

→ How to access and store Nginx access and error logs

→ Transferring files securely using scp
