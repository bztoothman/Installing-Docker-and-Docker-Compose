<p align="center">
<img src="https://i.imgur.com/b89vVVF.png"/>
</p>

<h1>Guide to Installing Docker and Docker-Compose on Ubuntu LTS Versions</h1>
This guide provides step-by-step instructions for uninstalling old versions of Docker, setting up the Docker APT repository, and installing the latest versions of Docker and Docker-Compose on Ubuntu LTS systems. <br />

<h2>Environments and Technologies Used</h2>

- Ubuntu 24.04 LTS Server (Virtual Machines/Compute)
- Docker
- Docker-Compose

<h2>Operating Systems Used </h2>

- Ubuntu 24.04 LTS Server (terminal only): <a href="https://ubuntu.com/download/server">Ubuntu Server 24.04 LTS</a>.

<h2>Prerequisites</h2>

Supported Operating Systems:
 - Ubuntu 24.04 LTS (Noble Numbat)
 - Ubuntu 22.04.4 LTS (Jammy Jellyfish)
 - Ubuntu 20.04.6 LTS (Focal Fossa)
<p>This guide uses Ubuntu 24.04 LTS Server (terminal only): <a href="https://ubuntu.com/download/server">Ubuntu Server 24.04 LTS</a>.
For a desktop environment, it is recommended to use Ubuntu 24.04 LTS Desktop: <a href="https://ubuntu.com/download/desktop">Ubuntu Desktop 24.04 LTS</a>.</p>


<h2>Uninstalling Previous Versions of Docker</h2>

<p>
</p>
<p>
To remove any existing Docker installations and conflicting packages, execute the following command:

 ```bash
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
```
</p>
<br />

<p>
<img src="https://i.imgur.com/VMTZmYU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h2>Setting Up Docker's APT Repository</h2>
 
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
<p>
<img src="https://i.imgur.com/6VBDcOA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

During this process, you may be prompted with "Do you want to continue? [Y/n]". Type y and press Enter to proceed.

<p>
<img src="https://i.imgur.com/57mjhUZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
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
<img src="https://i.imgur.com/aXMOIs4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h1>Installing the Latest Version of Docker</h1>
<h2>To install Docker, run the following command:</h2>
<p>

 ```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
During this process, you may be prompted with "Do you want to continue? [Y/n]". Type y and press Enter to proceed.
</p>
<br />

<p>
<img src="https://i.imgur.com/YF37FVQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h1>Verify Docker Installation</h1>
<h2>To confirm Docker is installed correctly, check the version:</h2>
<p>

 ```bash
docker --version
```
</p>
<br />

<p>
<img src="https://i.imgur.com/8eUX64W.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h1>Installing Docker-Compose</h1>
<h2>To install Docker-Compose, use the following command:</h2>
<p>

 ```bash
curl -SL https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose
```
</p>
<br />

<p>
<img src="https://i.imgur.com/LnfobDF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h1>Verify Docker-Compose Installation</h1>
<h2>Check the installed version of Docker-Compose with:</h2>
<p>

 ```bash
docker compose version
```
</p>
<p>
<img src="https://i.imgur.com/crZWJak.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
