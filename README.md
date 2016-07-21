Introduction
=======

 Ansible-NGINX is a Complete ansible playbook (more than roles) for nginx.

 This playbook will separate the steps to operate a whole nginx into many roles, and now allow users to install/reload nginx services with combined tags and seleted roles.




Get Involved
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

> You should related your environment includes:

	* hosts: defined in file like "env/dev/host_vars/dev"

	* env: defined with directory name like "dev" in env/

	* remote_user: defined in file like "env/dev/group_vars/variables.yml" or cmd, used to connect with SSH



how to install
-------


> in CentOS 7.0

	# ansible-playbook -i env/dev/host_vars/dev main.yml -e '{"hosts": "default", "env": "dev", "remote_user": "root"}' -t "centos,install"


> in Ubuntu 14.04

	# ansible-playbook -i env/dev/host_vars/dev main.yml -e '{"hosts": "default", "env": "dev", "remote_user": "dev"}' -t "ubuntu,install" --ask-sudo-pass



how to reload
-------

> in CentOS 7.0

	# ansible-playbook -i env/dev/host_vars/dev main.yml -e '{"hosts": "default", "env": "dev", "remote_user": "root"}' -t "reload"

> in Ubuntu 14.04

	# ansible-playbook -i env/dev/host_vars/dev main.yml -e '{"hosts": "default", "env": "dev", "remote_user": "dev"}' -t "reload" --ask-sudo-pass




Documentation
=======

You can add your own variables in files like

> "env/dev/group_vars/variables.yml"

or define variables just in files like

> "roles/configure/defaults/main.yml"

to customize your own nginx service.




Testing
=======

* CentOS 7.0     - successful

* Ubuntu 14.04   - successful




Any problem or PR
=======


Are [welcome](https://github.com/hongxiaolong/ansible-nginx/issues)!