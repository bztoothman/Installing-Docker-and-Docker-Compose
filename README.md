# Installing-Docker-and-Docker-Compose
Installing Docker and Docker-Compose

<p align="center">
<img src="![download](https://github.com/user-attachments/assets/edfd2184-fdb7-4063-9808-9b9c49b6abf2)"/>
</p>

<h1>Guide to Installing Docker and Docker-Compose on Ubuntu LTS Versions</h1>
This guide provides step-by-step instructions for uninstalling old versions of Docker, setting up the Docker APT repository, and installing the latest versions of Docker and Docker-Compose on Ubuntu LTS systems. <br />

<h2>Environments and Technologies Used</h2>

- Ubuntu 24.04 LTS Server (Virtual Machines/Compute)
- Docker
- Docker-Compose

<h2>Operating Systems Used </h2>

- Ubuntu 24.04 LTS Server (terminal only): Ubuntu Server 24.04 LTS.

<h2>Prerequisites</h2>

Supported Operating Systems:
 -Ubuntu 24.04 LTS (Noble Numbat)
 -Ubuntu 22.04.4 LTS (Jammy Jellyfish)
 -Ubuntu 20.04.6 LTS (Focal Fossa)
This guide uses Ubuntu 24.04 LTS Server (terminal only): [Ubuntu Server 24.04 LTS](https://ubuntu.com/download/server).
For a desktop environment, it is recommended to use Ubuntu 24.04 LTS Desktop: [Ubuntu Desktop 24.04 LTS](https://ubuntu.com/download/desktop).


<h2>Uninstalling Previous Versions of Docker</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To remove any existing Docker installations and conflicting packages, execute the following command:

 ```bash
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
```
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h2>Setting Up Docker's APT Repository/h2>
<p>
To install and update Docker from the official repository, follow these steps:
</p>
<h1>Add Docker's Official GPG Key:</h1>
<p>
 ```bash
 sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
 ```
</p>
<h1>Add the Docker Repository to APT Sources:</h1>
<p>
 ```bash
 echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
 ```
</p>

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
