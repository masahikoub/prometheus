# prometheus / node_exporter / alertmanager 

## build virtual machines
```
git clone https://github.com/masahikoub/prometheus
cd prometheus
vagrant up
```

## setup ssh
```
# ssh login to client server
vagrant ssh client
sudo vi /ets/ssh/sshd_config
systemctl restart sshd

# ssh login to prometheus server
vagrant ssh server
sudo vi /etc/ssh/sshd_config
sudo ssh-keygen
sudo ssh-copy-id 192.168.100.10
sudo ssh-copy-id 192.168.100.20
```

## ansible
```
sudo yum install -y git ansible
git clone https://github.com/masahikoub/prometheus
cd prometheus/ansible
ansible-playbook -i inventory/hosts master.yml
```
