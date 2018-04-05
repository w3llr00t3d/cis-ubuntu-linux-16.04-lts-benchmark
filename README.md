# CIS-Ubuntu-Linux-16.04-LTS-Benchmark
Ansible role that configures Ubuntu Linux 16.04 LTS to CIS Benchmark

## Install Ansible
```
sudo apt-get update && sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update && sudo apt-get install ansible
```

## Download Role From GitHub
```
git clone https://github.com/PaxDominicus/CIS-Ubuntu-Linux-16.04-LTS-Benchmark.git roles/cis
```

## Create Playbook
```
cat >>  playbook.yml << 'EOF'
---
- hosts: all
  roles:
    - cis
EOF
```

## Configure Playbook
defaults/main.yml

## Run Playbook
```
sudo ansible-playbook -b -i "localhost," -c local playbook.yml
```
