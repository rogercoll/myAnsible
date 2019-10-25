## Commands examples
ansible all -i inventory -m ping
ansible all -i inventory -m setup | less
ansible all -i inventory -a "apt list --installed"

With `-f` creates x parallel forks, useful if you have more than one host
ansilbe all -i inventory -a "man 2 write" -f 1

With `-a` flag enables to pass parameters to module and `-b` to become root
ansible all -i inventory -b -m apt -a "name=tree update_cache=yes"
ansible all -i inventory -a "tree /home/roger_coll_aumatell"

###Playbooks
ansible-playbook -i inventory playBooks/webServer.yml
