## Nodejs
* Distributions (<https://github.com/nodesource/distributions>)

#### NodeJS 13.x安装
```
# Using Ubuntu
curl -sL https://deb.nodesource.com/setup_13.x | sudo -E bash -
sudo apt-get install -y nodejs

# Using Debian, as root
curl -sL https://deb.nodesource.com/setup_13.x | bash -
apt-get install -y nodejs

# Run as root on RHEL, CentOS, CloudLinux or Fedora:
# As root
curl -sL https://rpm.nodesource.com/setup_13.x | bash -

# No root privileges 
curl -sL https://rpm.nodesource.com/setup_13.x | sudo bash -
```