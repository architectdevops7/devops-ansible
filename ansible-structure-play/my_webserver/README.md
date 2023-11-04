### Configure ansible roles
ansible-galaxy init /etc/ansible/roles/apache --offline

### Steps
1. Create the role from above command
2. Update the main playbook in root directory

`---
- name: Deploy Web Servers
  hosts: webservers
  roles:
    - apache`

`/etc/ansible`

3. Update the relevant files to configure ansible

apache/
├── defaults
│   └── main.yml
├── files
│   └── custom.html
├── handlers
│   └── main.yml
├── meta
│   └── main.yml
├── README.md
├── tasks
│   └── main.yml
├── templates
├── tests
│   ├── inventory
│   └── test.yml
└── vars
    └── main.yml

4. Play the playbook from below command
`ansible-playbook deploy_web.yml --syntax-check`
`ansible-playbook deploy_web.yml`