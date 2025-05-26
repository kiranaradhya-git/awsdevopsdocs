# awsdevopsdocs

## Installing Pre-Requisites

### Installing Docker on Ubuntu

```
sudo apt install docker.io
sudo apt install podman-docker
```

### Installing AWS CLI on Ubuntu


```
sudo apt install unzip
```

```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install --bin-dir /usr/local/bin --install-dir /usr/local/aws-cli --update
```

Ref: [Installing or updating to the latest version of the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

### Installing Kubectl on Ubuntu (Linux AMD64)

```
curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.33.0/2025-05-01/bin/linux/amd64/kubectl
```

```
chmod +x ./kubectl
```

```
mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$HOME/bin:$PATH
```

```
echo 'export PATH=$HOME/bin:$PATH' >> ~/.bash_profile
```

https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html

### Installing EKSCTL on Ubuntu (Linux AMD64)

Configure AWS CLI with Access Key and Secure Key

```
aws configure
```

```
# for ARM systems, set ARCH to: `arm64`, `armv6` or `armv7`
ARCH=amd64
PLATFORM=$(uname -s)_$ARCH

curl -sLO "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz"

# (Optional) Verify checksum
curl -sL "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_checksums.txt" | grep $PLATFORM | sha256sum --check

tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp && rm eksctl_$PLATFORM.tar.gz

sudo mv /tmp/eksctl /usr/local/bin
```


[Set up kubectl and eksctl](https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html)
[EKSCTL Installation](https://eksctl.io/installation/)

### Installing Java on Ubuntu

```
sudo apt install default-jre
```

Testing Java Installation
```
java -version
```

Ref
[Ubuntu Website - Install the Java Runtime Environment](https://ubuntu.com/tutorials/install-jre#2-installing-openjdk-jre)

### Installing Node on Ubuntu

```
sudo apt update
```

```
sudo apt install nodejs
```

Testing Installation

```
node -v
```

[NodeJS](https://nodejs.org/en)

### Installing Python

```
sudo apt install
sudo apt upgrade
```


```
python3 --version
```
https://discuss.python.org/t/install-python-3-11-9-on-ubuntu/51093

### How to install ReactJS

```
sudo apt install npm
```

```
sudo npm -g install create-react-app
```
  




