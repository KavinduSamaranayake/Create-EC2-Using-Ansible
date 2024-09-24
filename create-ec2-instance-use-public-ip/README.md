# Setup EC2 Collection and Authentication


## Install boto3

#### * use this command ->  pip install boto3

# 
## Install AWS Collection

#### * use this command ->  ansible-galaxy collection install amazon.aws

#
# Setup Vault

##  1. Create a password for vault

#### * use this command ->  openssl rand -base64 2048 > vault.pass

#
##  2. Add your AWS credentials using the below vault command

#### * use this command ->  ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass

#
## Create Ansible Role  

#### * use this command ->  ansible-galaxy role init ec2_role

#
##  Run 

#### * use this command ->  ansible-playbook -i inventory.ini create_ec2.yml --vault-password-file vault.pass
