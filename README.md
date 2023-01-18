# Kerio-Connect-Zabbix Mailbackup Check for Kerio Connect on Linux

Zabbix Template for Check Mailbackup works fine or not, you musst in Kerio Connect the Logfiles send to the Syslog Server, than the zabbix Agent must have acess to the syslog under /var/log/syslog 

In Kerio Connect under Logfile Section Error activated Log 

localhost:514
Typ: Mailsystem
Operting:  Kerio-Error

change on the Kerio Server Permission and add zabbix to the adm group
chmod 0660 /var/log/syslog
usermod -aG adm zabbix

