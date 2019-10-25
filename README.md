# myAnsible
Configurations and learings for my own usage

## Learning info
By deault ansible gets the hosts from /ets/ansible/hosts But we can also provide an inventory(hosts) file to ansible.

Varialbes= can be passed in via command line using the `-e` flags
Facts=are simply various properties regarding a given remote system. The `setup` module can retrive facts. Later on, can be used as ansible_varialbes
Handlers=mechanism that allows an action to be flagged for execution when a task performs a change. Be only executing certain tasks during a task CHANGE, pays are more efficient. Notify system.

###Roles
Roles provide a framework for fully independent, or interdependent collections of variables, tasks, files, templates, and modules.
The directory structure for roles is essential to create a new role.
Each role is a directory tree in itself. The role name is the directory name within the /roles directory.
Create a new role=ansible-galaxy init personalpc
Run a role=ansible-playbook -i inventory site.yml
