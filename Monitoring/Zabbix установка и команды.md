## Установка через VM 
Начинаем с установки Apache2
```javascript
sudo apt install apache2
sudo apt install php php-{cgi,common,mbstring,net-socket,gd,xml-util,mysql,bcmath,imap,snmp}
sudo apt install libapache2-mod-php
```
После приступаем к установке самого Zabbix

У меня возникали проблемы и вот их решения
```javascript 
sudo apt install libldap-2.4-2
sudo apt install zabbix-server-mysql zabbix-frontend-php zabbix-apache-conf zabbix-agent
```

После не мог зайти на mysql, пришлось установить его отдельно 
```javascript
sudo apt update
sudo apt install mysql-server
sudo systemctl start mysql
```
