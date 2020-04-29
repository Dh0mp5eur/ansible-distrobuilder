Role Name
=========

Build RootFS/LXC/LXD FS with Distrobuilder

Requirements
------------

Install distrobuilder before

Role Variables
--------------

distrobuilder_cmd: distrobuilder
distrobuilder_builder: build-lxc
distrobuilder_image: debian
distrobuilder_image_tpl: "images/{{ distrobuilder_image }}.yaml"
distrobuilder_image_release: buster
distrobuilder_meta_clean: True
distrobuilder_rootfs_clean: True
tpl_dir: "./"
meta_name: meta.tar.xz
rootfs_name: rootfs.tar.xz
tpl_name: "{{ distrobuilder_image }}_{{ distrobuilder_image_release }}.tar.xz"

Dependencies
------------

n/a

Example Playbook
----------------

---

- hosts: localhost

  roles:
    - distrobuilder

License
-------

BSD

Author Information
------------------

DHOMPS Florian
