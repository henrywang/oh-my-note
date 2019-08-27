By default, Ansible will always use /usr/bin/python on the remote system.
You set ansible_python_interpreter to provide a path to something that isn't
/usr/bin/python if you want it to use that instead. Sure, you can create a
symlink instead, but:

How is that any easier than setting an inventory variable?
1. On many distributions, /usr/bin/python already exists and is Python 2 and is
required by system tools. Replacing it will break things.
1. Even on systems that don't ship with Python 2 by default, by creating a
symlink from /usr/bin/python to /usr/bin/python3 you have potentially broken
anything that expects /usr/bin/python to be Python 2. That might not bite
you now but it might surprise you in the future.

### ansible as test framework
https://github.com/projectatomic/atomic-host-tests/blob/master/callback_plugins/default.py

### download file from http/s, ftp
https://docs.ansible.com/ansible/latest/modules/get_url_module.html

### copy and extract iso
https://docs.ansible.com/ansible/latest/modules/list_of_files_modules.html

### checksum file
https://docs.ansible.com/ansible/latest/modules/stat_module.html

### mktemp like ansible module
https://docs.ansible.com/ansible/latest/modules/tempfile_module.html

### kickstart with ansible
https://github.com/rembik/ansible-role-kickstart-iso
https://medium.com/@jackprice/pushing-kickstarts-with-ansible-122b2cd9c1e
https://devopsmates.com/make-custom-centos-7-rhel-7-cd-kicktart-file/
