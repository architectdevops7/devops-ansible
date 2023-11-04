### Installing ansible in Amazaon Linux 2 AMI
amazon-linux-extras install ansible2

### Steps to configure master & client machines  
1. Install ansible on master machine  
2. Install python on both master and client machines  
3. Create the ssh-key on ansible master machine then update id_rsa.pub key to all client machines  
4. Update the hosts file in ansible configuration `vi /etc/ansible/hosts`  
5. Check the syntaz issue from `ansible-playbook --syntax-check webserver.yml`  
6. Execute the playbook from master machine    