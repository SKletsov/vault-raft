# vault-raft 


inventory 

```
[all]
node1  
node2  
node3  


[vault_raft_servers]
node1
node2
node3

[all:vars]
ansible_user='root'
ansible_become=true

```

```
- hosts: all
  gather_facts: True
  become: true
  vars:
    vault_backend: raft 
    vault_cluster_name: infra
    vault_ui: true 
  roles:
    - ansible-vault
```



Links - https://vmik.net/2022/02/01/hc-vault-install-raft/
