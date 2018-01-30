# es-aws-ansible


## Setup
Get ansible installed

```bash
sudo easy_install pip
sudo pip install ansible
```

## Configure
Add your hosts to `config/hosts`
If you want to copy keys add your key to `files/key.pub`
Elasticsearch configuration can be modified at `files/elasticsearch.yml`

## Running

Installing elasticsearch:
```bash
ansible-playbook --key-file=~/yourkey.pem -i config/hosts provision_es.yml
```

Restarting elasticsearch
```bash
ansible-playbook --key-file=~/yourkey.pem -i config/hosts restart.yml
```

Copy new ssh key to cluster
```bash
ansible-playbook --key-file=~/yourkey.pem -i config/hosts copy_key.yml
```
