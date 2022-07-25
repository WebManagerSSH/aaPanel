![logo](https://user-images.githubusercontent.com/32661918/180830925-6fcbc315-c2ae-4ef4-9087-9bda563ea45f.png)

## Information Important
Repository was not made for financial purposes. (Student end)

## More information in
* Feature - https://www.aapanel.com/new/feature.html
* Pricing - https://www.aapanel.com/new/pricing.html
* Forum - https://forum.aapanel.com/

**  *Plan Free (Basic - Forever):* 

    ✓ Unlimited number of domains, 
    ✓ Unlimited SSL certificate, 
    ✓ Basic security protection, 
    ✓ Full-featured file manager, 
    ✓ File online editor, 
    ✓ Use all free plugins.
    

## :book: Installation 
aaPanel is developed based on Centos, we recommend using Centos to install it

* Centos:
```
yum install -y wget && wget -O install.sh https://raw.githubusercontent.com/WebManagerSSH/aaPanel/main/script/install_6.0_en.sh && bash install.sh github
```

* The experimental Centos/Ubuntu/Debian/Fedora installation command supports ipv6. Note that this command is executed with root privileges (Centos8 is supported)
```
curl -sSO http://www.aapanel.com/script/new_install_en.sh && bash new_install_en.sh github
```

* Ubuntu/Deepin:
```
wget -O install.sh https://raw.githubusercontent.com/WebManagerSSH/aaPanel/main/script/install-ubuntu_6.0_en.sh && bash install.sh github
```

* Debian:
```
wget -O install.sh https://raw.githubusercontent.com/WebManagerSSH/aaPanel/main/script/install-ubuntu_6.0_en.sh && bash install.sh github
```

** Note: You must install aaPanel for a new system that has not installed other environments such as Apache/Nginx/php/MySQL. It is recommended to use centos 7.X

## :scroll: CHANGE LOGS
**VERSION: 6.8.26**
* File management adds video playback
* File sharing adds directory sharing and video playback functions
* Optimize file sharing UI
* Publish system firewall plugin
* Release Amazon storage plugin
* Other details adjustment

## :heavy_exclamation_mark: Requirements
* Memory: 512M or more, 768M or more is recommended (Pure panel for about 60M of system memory)
* Hard disk: More than 100M available hard disk space (Pure panel for about 20M disk space)
* System: CentOS 7.1+ (Ubuntu20, Debian10), to ensure that it is a clean operating system, there is no other environment with Apache/Nginx/php/MySQL installed (the existing environment can not be installed)

## :octocat: CREDITS
1. @aaPanel - Criar Script
2. @k7Brasil - Custom Script
