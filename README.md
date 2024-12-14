## Now apply template to container
```sh
bastille create zabbix-agent 14.1-RELEASE YourIP_Address

bastille bootstrap https://github.com/bastille-templates/zabbix-agent
bastille template zabbix-agent bastille-templates/zabbix-agent
```

## License
This project is licensed under the BSD-3-Clause license.