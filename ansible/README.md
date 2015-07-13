Ansible
=======
Ping all hosts
```sh
ansible all -m ping
```

```sh
ansible-playbook test.yml
```

Playbook on a specific host
```sh
ansible-playbook -i "debian," logstash.yml
```

References
----------
 - [ansible tutorial](https://serversforhackers.com/an-ansible-tutorial)
 - [packetbeat-deploy](https://github.com/packetbeat/packetbeat-deploy)
