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

## :grey_exclamation: Management script for commands
- [Management]
    - Stop
        ```
        service bt stop
        ```

    - Start
        ```
        service bt start
        ```
    - Restart
        ```
        service bt restart
        ```
    - Uninstall
        ```
        service bt stop && chkconfig --del bt && rm -f /etc/init.d/bt && rm -rf /www/server/panel
        ```
    - View current port of control panel
        ```
        cat /www/server/panel/data/port.pl
        ```
    - Change port of control panel，e.g. 8881（centos 6 Operation System）
        ```
        echo '8881' > /www/server/panel/data/port.pl && service bt restart iptables -I INPUT -p tcp -m state --state NEW -m tcp --dport 8881 -j ACCEPT service iptables save service iptables restart
        ```
    - Change port of control panel，e.g. 8881（centos 7 Operation System）
        ```
        echo '8881' > /www/server/panel/data/port.pl && service bt restart firewall-cmd --permanent --zone=public --add-port=8881/tcp firewall-cmd --reload
        ```
    - Force to change MySQL manager (root) Password，e.g. 123456
        ```
        cd /www/server/panel && python tools.py root 123456
        ```
    - Change control Panel login password，e.g. 123456
        ```
        cd /www/server/panel && python tools.py panel 123456
        ```
    - Site Configuration location
        ```
        /www/server/panel/vhost
        ```
    - Delete banding domain of control panel
        ```
        rm -f /www/server/panel/data/domain.conf
        ```
    - Clean login restriction
        ```
        rm -f /www/server/panel/data/*.login
        ```
    - View control panel authorization IP
        ```
        cat /www/server/panel/data/limitip.conf
        ```
    - Stop access restriction
        ```
        rm -f /www/server/panel/data/limitip.conf
        ```
    - View permission domain
        ```
        cat /www/server/panel/data/domain.conf
        ```
    - Turn off control panel SSL
        ```
        rm -f /www/server/panel/data/ssl.pl && /etc/init.d/bt restart
        ```
    - View control panel error logs
        ```
        cat /tmp/panelBoot
        ```
    - View database error log
        ```
        cat /www/server/data/*.err
        ```
    - Site Configuration directory(nginx)
        ```
        /www/server/panel/vhost/nginx
        ```
    - Site Configuration directory(apache)
        ```
        /www/server/panel/vhost/apache
        ```
    - Site default directory
        ```
        /www/wwwroot
        ```
    - Database backup directory
        ```
        /www/backup/database
        ```
    - Site backup directory
        ```
        /www/backup/site
        ```
    - Site logs
        ```
        /www/wwwlogs
        ```
- [Nginx]
    - One Cmd
        ```
        One Cmd
        ```
- [Apache]
    - One Cmd
        ```
        One Cmd
        ```
- [MySQL]
    - One Cmd
        ```
        One Cmd
        ```
- [FTP]
    - One Cmd
        ```
        One Cmd
        ```
- [PHP]
    - One Cmd
        ```
        One Cmd
        ```
- [Redis]
    - One Cmd
        ```
        One Cmd
        ```
- [Memcached]
    - One Cmd
        ```
        One Cmd
        ```

## :heavy_exclamation_mark: Requirements
* Memory: 512M or more, 768M or more is recommended (Pure panel for about 60M of system memory)
* Hard disk: More than 100M available hard disk space (Pure panel for about 20M disk space)
* System: CentOS 7.1+ (Ubuntu20, Debian10), to ensure that it is a clean operating system, there is no other environment with Apache/Nginx/php/MySQL installed (the existing environment can not be installed)

## :scroll: CHANGE LOGS
**VERSION: 6.8.26**
* File management adds video playback
* File sharing adds directory sharing and video playback functions
* Optimize file sharing UI
* Publish system firewall plugin
* Release Amazon storage plugin
* Other details adjustment

## :octocat: CREDITS
1. @aaPanel - Criar Script
2. @k7Brasil - Custom Script
