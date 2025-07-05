# Install-Ubuntu-on-Windows-using-WSL
In this guide, I will walk you through step-by-step instructions on how to easily install Ubuntu on your Windows PC using WSL (Windows Subsystem for Linux) commands.

## Requirements:
- Windows 10 (Version 2004 or later with Build 19041+)
- Windows 11 (Fully supported)

---

## Step 1:

Open Windows PowerShell

![image alt](https://github.com/CryptoGurujiOG/Install-Ubuntu-on-Windows-using-WSL/blob/c1062e2232490323d907b3fc2aa65af413ce9fb9/Screenshot%201.png)

## Step 2:

Run the WSL Installation Command

```
wsl --install
```
Like this 👇

![image alt](https://github.com/CryptoGurujiOG/Install-Ubuntu-on-Windows-using-WSL/blob/324d30708e6d69259b9af26ac4a9a022e1109fc7/Screenshot%202.png)

- It may take some time to download and install WSL.
- Restart your PC after the installation is complete.

## Step 3:

- Open Ubuntu
- Create your Username and Password

![image alt](https://github.com/CryptoGurujiOG/Install-Ubuntu-on-Windows-using-WSL/blob/ba51783d39a640b6b5b37ef6ea688f9fdd25e1cb/Screenshot%203.png)

## Step 4:

- Install and Update Packages

Run these commands 👇

```
sudo apt update

sudo apt upgrade
```

```
sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
```

Install Docker:

```
sudo apt update -y && sudo apt upgrade -y

for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do 
  sudo apt-get remove -y $pkg 
done

sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg

sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
  sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
https://download.docker.com/linux/ubuntu \
$(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update -y && sudo apt upgrade -y

sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

docker --version
```

---

✅ Now you are ready to run Nodes on your Pc

## Watch my Step by Step Video Guide 👇

[![Watch on YouTube](https://img.youtube.com/vi/mpdwAlRyOrE/hqdefault.jpg)](https://youtu.be/mpdwAlRyOrE)


