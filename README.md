## Ansible 

![Ansible image](./img/Untitled.png)

## Links Refs

[Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

[PIPX](https://pipx.pypa.io/stable/)

### Install and Configure

    $ sudo apt-get install python3-pip
    $ python3 -m pip install --user pipenv
    $ python3 -m pip install --user pipx
    $ sudo apt install python3.8-venv
    $ python3 -m pipx ensurepath
    $ source ~/.bashrc
    $ pipx install --include-deps ansible
    $ pipx install ansible-core
    $ apt-get install sshpass

### Validate

    $ ansible localhost -m ping

ex:
````log
[WARNING]: No inventory was parsed, only implicit localhost is available
localhost | SUCCESS => {
    "changed": false,
    "ping": "pong"
}
````

### Using ad-hoc 


    $  ansible -i inventario all -m ping -u root -k

    ou 

    $  ansible -i inventario -m ping -u root --  private-key ~/.ssh/id_rsa.pub 

### Using playbooks


    $  ansible-playbook -i inventario install-kubectl.yaml


### Using Ansible-vault 

Using with password interactively

    $  ansible-vault encrypt inventario
    $  ansible-vault edit inventario
    $  ansible-vault decrypt inventario


### Modules

[Ansilbe modules](https://docs.ansible.com/ansible/2.9/modules/list_of_all_modules.html)


