# DevOps in AWS

## Setup in AWS EC2 with Ubuntu Server

### Server
```bash
sudo su
apt-get update && apt-get upgrade && apt-get autoremove && apt-get clean && apt-get autoclean 
```

### Node.js
```bash
sudo apt-get install curl
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
source ~/.bashrc
nvm list-remote
nvm install [version] #Example: nvm install v16.13.2
```

### Python

Find the python version you need here: [Python version](https://www.python.org/ftp/python)

```bash
sudo apt update

# Install the dependencies
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev

# Download the package. Example:
# wget https://www.python.org/ftp/python/3.9.5/Python-3.9.5.tg
# tar -xf Python-3.9.5.tgz

wget https://www.python.org/ftp/python/[version]/*.tgz 
tar -xf Python-[version].tgz 

# Enter into your folder. Example: 
# cd Python-3.9.5
cd Python-[version]

# Install python 
./configure --enable-optimizations
make -j 12
sudo make altinstall
```

### Install CodeDeploy Agent
Run this on your current user. Example: /home/ubuntu
```bash
sudo apt update
sudo apt install install ruby
wget https://aws-codedeploy-us-east-1.s3.amazonaws.com/latest/install
sudo chmod +x ./install
sudo ./install auto
```
