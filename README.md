IntelliJ IDEA Ultimate Installer
================================

Installs IntelliJ IDEA Ultimate on Ubuntu. You can specify a version and it will install or upgrade to that version.
It will remove any old versions that *this role* has installed.

I'm planning to add the Community Edition as well. Should be quite easy.

Based on: [jdauphant/ansible-role-intellij](https://github.com/jdauphant/ansible-role-intellij).

Requirements
------------
This role does not handle Java installation. IDEA requires that of course. I use [williamyeh.oracle-java](https://github.com/William-Yeh/ansible-oracle-java).

Role Variables
--------------

    intellij_version: 2016.2.2
 
 Which version to install.

    intellij_download_dir: /home/{{ ansible_env.HOME }}/Downloads

Where the tar.gz will be downloaded.

    intellij_install_dir: /opt/intellij

Where IDEA will be installed


Dependencies
------------

None.

Example Playbook
----------------

    - hosts: mylaptop
      roles:
        - { role: rdeknijf.intellij, intellij_version: 2016.1 }         

License
-------
MIT / BSD

Author Information
------------------
Rutger de Knijf
<rutger@deknijf.com>
