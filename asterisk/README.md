1. Добавить пользователю zabbix возможность запускать /usr/bin/asterisk
~~~
    |-- /etc/sudoers
    |----   zabbix       ALL=(ALL)       NOPASSWD:/usr/sbin/asterisk
~~~
2. Проверить что в конфигурации zabbix агента есть строка
~~~
    |--/etc/zabbix/zabbix_agentd.conf
    |----   Include=/etc/zabbix/zabbix_agentd.d
~~~
3. Скопировать Asterisk.conf в /etc/zabbix/zabbix_agentd.d
4. Импортировать шаблон в zabbix
