# Dynamic and automatic validation process based Cisco Family

The process developed here are related with different modules of Ansible and using functions like NAPALM and other library developed by community in order to help get correct information from devices.

##Requirements

Follow the process to use this deploy

1) Install **nelsnmp** - ```pip install nelsnmp --upgrade```
2) Install **ansible-snmp** - Access this code done by [networklore](https://github.com/networklore/ansible-snmp)
3) Refer in `ansible.cfg` the library installed before via folder you make download through `git clone`
4) Validate inside correct version of Ansible using `network-cli` as connection.
```
ansible 2.6.2
  config file = /etc/ansible/ansible.cfg
  configured module search path = [u'/root/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python2.7/dist-packages/ansible
  executable location = /usr/bin/ansible
  python version = 2.7.12 (default, Dec  4 2017, 14:50:18) [GCC 5.4.0 20160609]
```

##Comments

This project has idea to collect automatically in Cisco device your module/family via `snmp ` and `get_facts` and you can compare which best for you because NAPALM has other status can be used after to go through in your deployment. We could create and developed your scripts based in some rules using a static inventory built in csv file and organize those script creating different tasks.

For this example none module were execute to access device and implement scripts, however this action is only add module `ios_config` or `nxos_config`

If you have more idea fell free to contact to build this developed.
