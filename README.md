# FRP--fast-reverse-proxy

# EXPOSING LOCAL APACHE WEBSITE USING FRP

# INTRODUCTION TO FRP

 It is the server component of a fast reverse proxy (FRP) system that exposes local services behind a firewall or NAT to the internet. It runs on a publicly accessible machine and waits for connections from FRP clients, which run on the local machines.

 
## We'll need to accomplish:

- Set up an AWS EC2 instance (Ubuntu) to act as the FRP server
- Create a simple website locally (FRP client side)
- Configure FRP server on EC2
- Configure FRP client on your local machine
- Expose your local website through the FRP server



# 1. Set up an AWS EC2 instance (Ubuntu) 
## 1. LAUNCH INSTANCE
- Log into AWS Console
- Navigate to EC2 Dashboard
- Click "Launch Instance"
- 
## Step 2 - Connect to your EC2 instance
 Use putty to connect to the EC2 instance


 
## Step 3 - Install FRP server
<img width="782" height="141" alt="Screenshot 2025-11-03 205318" src="https://github.com/user-attachments/assets/d00732f7-a339-468d-a89f-98106f99fb86" />

# Update system
sudo apt update && sudo apt upgrade -y

# Download FRP 

wget https://github.com/fatedier/frp/releases/download/v0.52.3/frp_0.52.3_linux_amd64.tar.gz

# Extract
tar -xzf frp_0.52.3_linux_amd64.tar.gz
cd frp_0.52.3_linux_amd64
