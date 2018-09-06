# Dynamic and automatic validation process based Cisco Family

The process developed here used different modules of Ansible and projects like NAPALM and other libraries developed by the community in order to access and get correct information from Cisco network devices.

## Requirements

Follow these steps

1. Install **nelsnmp** - ```pip install nelsnmp --upgrade```
2. Install **ansible-snmp** - Access this code done by [networklore](https://github.com/networklore/ansible-snmp)
3. Refer in `ansible.cfg` the library installed before via folder you make download through `git clone`
4. Validate inside correct version of Ansible using `network-cli` as connection.
```
ansible 2.6.2
  config file = /etc/ansible/ansible.cfg
  configured module search path = [u'/root/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python2.7/dist-packages/ansible
  executable location = /usr/bin/ansible
  python version = 2.7.12 (default, Dec  4 2017, 14:50:18) [GCC 5.4.0 20160609]
```

## Comments

This project has idea to collect automatically in Cisco device your module/family via `snmp ` and `get_facts` and you can compare which is best for you because NAPALM has other status that can be used after to go through in your deployment. We could create and developed your scripts based on some rules using a static inventory built in a .csv file and organize those script creating different tasks.

For this example non modules were executed to access device and implement scripts, however this action requires only that you add module `ios_config` or `nxos_config`

If you have other ideas, feel free to contact (e.g. create a new issue) to help this be developed.
