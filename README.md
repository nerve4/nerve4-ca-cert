# cacert

An Ansible role that installs and generate ca-certs to Rhel and Ubuntu. More info about cacerts: [link](https://www.redhat.com/sysadmin/ca-certificates-cli/)


## Requirements

Make sure, you made your vars file with valid path to custom template or you can use Default vars.

You need `ansible 2.13.7` to run this module

The Role also use `community.general collection` module. To install it, use: `ansible-galaxy collection install community.general`. 


## Tasks descriptions

- main.yml - Run the OS check and run the relevant playbook
- configure-cacert.yml - Configure CA location and generate Certs
- rhel-install-cacert.yml - Deploy CA pkgs on Rhel
- ubuntu-install-cacert.yml - Deploy CA pkgs on Ubuntu


## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- hosts: servergroup
  become: true
  become_user: lee

  vars_files:
    - vars/main.yml
    
  roles:
    - nerve4-ca-cert
```


## Maintainer Information
Lee | 2023