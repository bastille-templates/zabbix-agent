## Now apply template to container
```sh
bastille create zabbix-agent 14.1-RELEASE YourIP_Address

bastille bootstrap https://github.com/bastille-templates/zabbix-agent
bastille template zabbix-agent bastille-templates/zabbix-agent
```

## License
This project is licensed under the BSD-3-Clause license.

## Start and login Agents container
```sh

# IP to IP Server Zabbix
sed -i '' 's%Server=127.0.0.1%Server=10.0.0.1%g' /usr/local/etc/zabbix7/zabbix_agentd.conf
# IP to IP Server Zabbix
sed -i '' 's%ServerActive=127.0.0.1%ServerActive=10.0.0.1%g' /usr/local/etc/zabbix7/zabbix_agentd.conf
# Hostname
sed -i '' 's%Hostname=Zabbix server%Hostname=famp%g' /usr/local/etc/zabbix7/zabbix_agentd.conf

# restart service
service zabbix_agentd restart