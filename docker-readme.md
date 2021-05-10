## Prerequisites install

This install has been tested on Ubuntu 20.04 running on a standard VPS. The distro needs docker fully running.

```
sudo apt-get update
sudo apt-get install git curl wget python3-pip
sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release
```

Download the GPG key from the APT docker repo

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

Add APT repository that matches your CPU architecture

```
echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Install docker & docker-compose

```
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
sudo apt-get install docker-compose
```
