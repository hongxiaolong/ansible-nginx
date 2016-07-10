Introduction
=======

 Ansible-NGINX is a Complete ansible playbook (more than roles) for nginx.

 This playbook will separate the steps to operate a whole nginx into many roles, and allow users to install/reconfigure/reload nginx services with combined tags and seleted roles.



Related Introduction
=======

Ansible is a radically simple IT automation system. It handles configuration-management, application deployment, cloud provisioning, ad-hoc task-execution, and multinode orchestration - including trivializing things like zero downtime rolling updates with load balancers.

Read the documentation and more at http://ansible.com/

Here are a few NGINX Ansible Galaxy Roles

* https://galaxy.ansible.com/list#/roles/466

* https://galaxy.ansible.com/list#/roles/551

* https://galaxy.ansible.com/list#/roles/471

* https://galaxy.ansible.com/list#/roles/1580

Read the full post here:

* [Installing NGINX and NGINX Plus With Ansible](https://www.nginx.com/blog/installing-nginx-nginx-plus-ansible/)



How to Play
=======

install
-------


`$ ansible-playbook -i env/dev/host_vars/dev main.yml -e '{"hosts": "default", "env": "dev"}' -t "install,centos"`


or


`$ ansible-playbook -i env/dev/host_vars/dev main.yml -e '{"hosts": "uu", "env": "dev", "remote_user": "dev"}' -t "ubuntu,install" --ask-sudo-pass`


reconfigure
-------


`$ ansible-playbook -i env/dev/host_vars/dev main.yml -e '{"hosts": "default", "env": "dev"}' -t "reconfigure"`


reload
-------


`$ ansible-playbook -i env/dev/host_vars/dev main.yml -e '{"hosts": "default", "env": "dev"}' -t "reload"`
