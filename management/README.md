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
