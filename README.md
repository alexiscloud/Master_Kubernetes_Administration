# Master_Kubernetes_Administration
## Module 1 : Step-by-step guide to install Docker on an AWS EC2 instance running Ubuntu 22.04

## Launch an instance
> EC2 >Instances >Launch an instance

<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (60).png?raw=true" width ="80%">
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (61).png?raw=true" width ="80%">
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (62).png?raw=true" width ="80%">

## Allocate Elastic IP address
> EC2>Elastic IP addresses>Allocate Elastic IP address

<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (63).png?raw=true" width ="80%">
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (64).png?raw=true" width ="80%">
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (65).png?raw=true" width ="80%">
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (66).png?raw=true" width ="80%">
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (67).png?raw=true" width ="80%">
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (68).png?raw=true" width ="80%">

## Login with Putty
> login user and host name ip adding
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (69).png?raw=true" width ="80%">

> auth section add credential
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (70).png?raw=true" width ="80%">

> accept key and login
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (71).png?raw=true" width ="80%">

> view ubuntu instance terminal
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (72).png?raw=true" width ="80%">

> check OS status
```
cat /etc/os-release
```
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot (73).png?raw=true" width ="80%">

# Module 2 : Introduction to Containers and Docker
## Setting up Docker on a Linux host
> Linux

#### Set up the repository
```
sudo apt-get update
```

```
sudo apt-get install ca-certificates curl gnupg
```
```
sudo mkdir -m 0755 -p /etc/apt/keyrings
```
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
```
echo "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | sudo tee /etc/apt/sources.list.d/docker.list /dev/null
```
#### Install Docker Engine
```
sudo apt-get update
```
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
```
sudo docker ps
```
#### Manage Docker as a non-root user
```
sudo groupadd docker
```
```
sudo usermod -aG docker $USER
```
```
newgrp docker
```
```
docker ps
```
#### Configure Docker to start on boot with systemd
```
sudo systemctl enable docker.service
sudo systemctl enable containerd.service
```
#### To stop this behavior, use disable instead
```
sudo systemctl disable docker.service
sudo systemctl disable containerd.service
```
> Mac 

[Download docker desktop for mac here](https://docs.docker.com/desktop/install/mac-install/)

> Windows

[Download docker desktop for windows here](https://docs.docker.com/desktop/install/windows-install/)
