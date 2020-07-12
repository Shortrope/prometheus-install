# prometheus-install
## Install in an LXC CentOS 7.1
```
yum update
yum install wget vim tmux which
```
Install git
```
yum groupinstall "Development Tools"
yum install gettext-devel openssl-devel perl-CPAN perl-devel zlib-devel
yum install https://centos7.iuscommunity.org/ius-release.rpm
yum install git2u-all
git --version
```
Clone this repo and run the install
```
git clone https://github.com/Shortrope/prometheus-install.git
./prometheus-install/prom-install <options>
```
## Usage
### prom-install:
```
prom-install <ver> <ipaddr> <mask> <gateway>
prom-install 2.13.1 192.168.1.15 255.255.255.0 192.168.1.1
```
The script does the following:
- configures eth1 with the ip address info and bring the interface up
- downloads, extracts and installs the prometheus files - with the version specified
- creates the prometheus.service file and starts the service  

### prom-checks:  
displays checks to make sure everything was installed properly  

### prom-uninstall:  
removes everything done by prom-install  
