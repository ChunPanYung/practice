### Command Types

`$ ansible`: ad-hoc command

`$ ansible-playbook`: runs predefined commands, will read `ansible.cfg` if exists in current directory

`$ ansible-playbook --list_tags FILE.yml`: list all tags in FILE.yml
`$ ansible-playbook --tags "TAG1, TAG2" FILE.yml`: run ansible only on task with tags TAG1, or TAG2

### Ad-hoc Commands

baisc command:

`$ ansible [all|host_name|ip] --key-file ~/.ssh/[secret_key] --inventory INVENTORY_PATH --module_path MODULE_PATH --args MODULE_ARGS`

List all the hosts:

`$ ansible HOSTS --list-hosts`

Print out all information on all server:

`$ ansible HOSTS -m gather_facts`

Limit to one host:

`$ ansible all -m gather_facts --limit IP_ADDRESS`

### Modules & Options

apt Update package repositories:

`$ ansible [hosts] -m apt -a update_cache=true`

* `$ apt update`

`$ ansible HOSTS -m apt -a name=vim-nox`

* `$ apt install vim-nox`

`$ ansible HOSTS -m apt -a "name=vim-nox state=absent"`

* Remove `vim-nox` using apt

`$ ansible HOSTS -m apt -a "name=snapd state=latest"`

* Install and Update `snapd` to the latest version

`$ ansible HOSTS -m apt -a "upgrade=dist"`

* `$ apt dist-upgrade`

### Options

`$ ansible HOSTS <command> --become --ask-become-pass`

* Become root and ask to enter password

* It only works if all hosts have same password

### File Structure

`ansible.cfg`: ansible configuration settings, environment variables, command-line options, playbook keywords, and varaibles.

* Use `;` for comment

* variation of `.ini` format

`inventory.yml | inventory.ini`: for hostname, connection type, user name
