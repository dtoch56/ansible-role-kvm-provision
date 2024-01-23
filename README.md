ansible-role-kvm-provision
=========

[![CI](https://github.com/dtoch56/ansible-role-kvm-provision/workflows/CI/badge.svg?event=push)](https://github.com/dtoch56/ansible-role-kvm-provision/actions?query=workflow%3ACI)


Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml).

## Template

| Variable         | Description                  | Default                                                                                                   |
|------------------|:-----------------------------|:----------------------------------------------------------------------------------------------------------|
| base_image_name  | Base image file name         | Fedora-Cloud-Base-39-1.5.x86_64.qcow2                                                                     |
| base_image_url   | Base image url               | https://download.fedoraproject.org/pub/fedora/linux/releases/39/Cloud/x86_64/images/{{ base_image_name }} |
| base_image_sha   | Base image SHA               | ab5be5058c5c839528a7d6373934e0ce5ad6c8f80bd71ed3390032027da52f37                                          |
| libvirt_pool_dir | Libvirt image directory path | "/var/lib/libvirt/images"                                                                                 |
| vm_name          | VM name                      | f39-dev                                                                                                   |
| vm_vcpus         | VM CPU number                | 2                                                                                                         |
| vm_ram_mb        | VM RAM size in MB            | 2048                                                                                                      |
| vm_net           |                              | default                                                                                                   |
| vm_root_pass     |                              | developer                                                                                                 |
| cleanup_tmp      | Path to                      | false                                                                                                     |
| ssh_key          | Proxmox VM ID for template   | /root/.ssh/id_rsa.pub                                                                                     |

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: localhost
      roles:
        - { role: dtoch56.kvm_provision }

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2024 by DToch.

Development
------------------

    pip install pipenv
    pipenv install
