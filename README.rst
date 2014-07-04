Ansible Scripts for Minecraft
===============================

Setup
---------
Edit `/etc/ansible/hosts` to create a Minecraft group::

    [minecraft]
    my.minecraft.server.net

Tasks
---------

Restart Minecraft on a remote server.::

    ansible-playbook restart-minecraft.yml

Installing Minecraft
------------------------------------

Disclaimer: I used this once, and it worked, but it is not even remotely robust yet.
It also doesn't even setup your Minecraft as a service, for compatability with the restart-minecraft.yml script.

Download a Java RPM for use with CentOS, into the same diectory as Vagrantfile::

    >ls
    Vagrantfile
    jre-7u25-linux-x64.rpm

Edit install-minecraft.yml so that it knows the name of the Java RPM.

Install Minecraft on a remote server.::
    
    ansible-playbook install-minecraft.yml
