# Agritracer Setup #

Getting Started :
===============
To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

Minimum server request :
```info
[CPU Intel] -> [X86_64] [2 Core]
[Ram] -> [4GB]
[Disk] -> [50GB] 
[OS] -> [Debian Distro Core 64Bit]
```

Linux Envroment :
=====================

Github Config Account :
```bash
git config --global user.name "FIRST_NAME LAST_NAME"
```
```bash
git config --global user.email "MY_NAME@example.com"
```

Setup Run Directory :
```bash
mkdir -p ~/Agritracer
```
```bash
cd Agritracer
```

Setup Repo and bin PATH
```bash
mkdir -p ./bin
```
```bash
curl https://storage.googleapis.com/git-repo-downloads/repo > ./bin/repo
```
```bash
chmod a+x ./bin/repo
```
```bash
PATH=./bin:$PATH # or echo 'PATH=./bin:$PATH' > ~/.bashrc
```

Setup Docker Compose :
```bash
sudo apt-get update -yq
```
```bash
sudo apt-get install ca-certificates curl gnupg lsb-release -yq
```
```bash
export DISTRO="debian"
curl -fsSL https://download.docker.com/linux/$DISTRO/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/$DISTRO \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
```bash
sudo apt-get update -yq
```
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -yq
```
```bash
sudo systemctl enable docker.service
```
