# Docker with ubuntu - Note

> Preparation
```sh
sudo apt-get update
```
```sh
sudo apt-get install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
```
```sh
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
```sh
sudo apt-key fingerprint 0EBFCD88
```
```sh
// x86_64
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

> Install
```sh
sudo apt-get install -y docker-ce
```

> Check
```sh
docker version
```

> Manage Docker as a non-root user
```sh
sudo groupadd docker
```
```sh
sudo usermod -aG docker $USER
```
```sh
newgrp docker
```

