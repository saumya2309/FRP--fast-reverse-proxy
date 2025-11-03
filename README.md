# FRP--fast-reverse-proxy

# EXPOSING LOCAL APACHE WEBSITE USING FRP

# INTRODUCTION TO FRP

 It is the server component of a fast reverse proxy (FRP) system that exposes local services behind a firewall or NAT to the internet. It runs on a publicly accessible machine and waits for connections from FRP clients, which run on the local machines.

 


## 1. LAUNCH INSTANCE
- Log into AWS Console
- Navigate to EC2 Dashboard
- Click "Launch Instance"
- 
## 2. - Connect to your EC2 instance
 Use putty to connect to the EC2 instance


 
## 3. - Install FRP server
<img width="782" height="141" alt="Screenshot 2025-11-03 205318" src="https://github.com/user-attachments/assets/d00732f7-a339-468d-a89f-98106f99fb86" />

# Update system
sudo apt update && sudo apt upgrade -y

# Download FRP 

wget https://github.com/fatedier/frp/releases/download/v0.52.3/frp_0.52.3_linux_amd64.tar.gz

# Extract
tar -xzf frp_0.52.3_linux_amd64.tar.gz
cd frp_0.52.3_linux_amd64


## 4. - Configure FRP client
Create a client configuration file `frpc.toml`:
```bash
sudo rm usr/local/frp/frpc.toml
sudo vim usr/local/frp/frpc.toml
```
Add the following content:
```toml

serverAddr = "3.7.253.188" # REPLACE YOUR OWN IP
serverPort = 7000
token = "eth4" 

[[proxies]]
name = "web"
type = "http" 
localPort = 80
remotePort = 8080
```

## 5. - Run the FRP client
```bash
sudo /usr/local/frp/frpc -c /usr/local/frp/frpc.toml
```

## 6. RUN FRP CLIENT

<img width="974" height="251" alt="Screenshot 2025-11-03 210111" src="https://github.com/user-attachments/assets/1c86678f-0069-4cee-9f88-39d0e594fcf7" />


## 7 . CHECKING WEBSITE IS ACCESSED ON PORT 8080

<img width="1283" height="846" alt="image" src="https://github.com/user-attachments/assets/cefb5c24-6241-45bc-830b-1ae0edb5a555" />



