Firewall role
=========

Данная роль настраивает iptables используя набор стандартных правил, подходящих для большинства хостов

Role Variables
--------------
**fw_accept_rules** - стандартные разрешающие правила (разрешаем ssh, prometheus, zabbix), применимые для многих хостов, можно переопределить в случае нестандартных хостов  
**extra_fw_accept_rules** - пустой массив, можно задать свое значение, если нужно дополнить стандартный набор правил  

Example Playbook
----------------
  - name: Firewall setup  
    hosts: all  
    become: yes  
    roles:  
      - firewall  



