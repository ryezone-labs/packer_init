ryezone-labs/packer_init
=========

This role contains many of the initialization steps necessary for my vagrant box
builds with packer.


Role Variables
--------------

| Variable Name | Type | Default Value | Description |
| ------------- | ---- | ------------- | ----------- |
| `packer_init_vagrant_key_uri` | string | `https://raw.githubusercontent.com/hashicorp/vagrant/master/keys/vagrant.pub` | URI to vagrant public insecure key. |
| `packer_init_desktop` | bool | `false` | Flag to toggle logic specific to Ubuntu Desktop vagrant boxes. |


Example Playbook
----------------

    ```yaml
    ---
    - hosts: 127.0.0.1
      connection: local
      vars:
        packer_init_desktop: false
      roles:
        - rz.packer_init
        - rz.packer_complete
    ```

License
-------

BSD
