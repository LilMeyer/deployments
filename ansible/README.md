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

Elastic search
--------------
```sh
wget https://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-1.6.0.deb
```


References
----------
 - [ansible tutorial](https://serversforhackers.com/an-ansible-tutorial)
 - [packetbeat-deploy](https://github.com/packetbeat/packetbeat-deploy)
