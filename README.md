# FRP--fast-reverse-proxy

# EXPOSING LOCAL APACHE WEBSITE USING FRP

# INTRODUCTION TO FRP

 It is the server component of a fast reverse proxy (FRP) system that exposes local services behind a firewall or NAT to the internet. It runs on a publicly accessible machine and waits for connections from FRP clients, which run on the local machines.

 # 1. LAUNCH INSTANCE







<img width="1912" height="904" alt="image" src="https://github.com/user-attachments/assets/5142e662-5f46-4025-a9a4-bcbdc27051e0" />



# 2. DOWNLOAD FRP SERVER ON CREATED AWS UBUNTU SERVER
wget https://github.com/fatedier/frp/releases/download/v0.58.1/frp_0.58.1_linux_amd64.tar.gz
tar -xvzf frp_0.58.1_linux_amd64.tar.gz
cd frp_0.58.1_linux_amd64




FRP IS RUNNING.


# 3. CREATE FRP SERVER CONFIGURATION
Create frps.ini:
[common]
bind_port = 7000
dashboard_port = 7500
dashboard_user = admin
dashboard_pwd = admin


Start the server:
./frps -c frps.ini






