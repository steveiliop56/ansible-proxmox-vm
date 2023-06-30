# ansible-proxmox-vmcreation
Some simple ansible playbooks for creating, starting, stopping, deleting proxmox virtual machines...

### Installing

In order to use these playbooks you will need to install the proxmoxer module on your proxmox server. In order to so this run this command:
```Shellscript
pip3 install proxmoxer --break-system-packages
```

**Note:** The *--break-system-packages* will not break something is just a required flag for the installation to happen.

### Running

You firstly have to add the required configuration variables in the ``vars.yml`` file and in the ``inventory``. It is very easy, you only need to addyour virtual machine name the template* to clone from and your proxmox credentials.
After you do this you will be able to run each of the playbooks with this command:
```Shellscript
ansible-playbook -i inventory nameofplaybook.yml
```

***Note:** These playbooks do not create a vm (although the module that I use supports it) but just clone an existing template, for faster creation. If you don't know or don't have a template you can create 
one yourself with [this guide](https://youtu.be/MJgIm03Jxdo) from Learn Linux TV.
