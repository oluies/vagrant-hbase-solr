

=================================
Vagrant on Mac w Virtualbox
=================================

The Goal:
=========
Install Brew, VirtualBox, Vagrant and  Vagrant-Manager, on a Macintosh 10.12.x system.

Assumptions:
============
You are running a computer with Mac OS X 10.12.x installed.
 
Overview:
=========
1 Install Brew.
2 Brew Vagrant.
3 “Hello World” Vagrant.


1. Install Prerequisite Software (Homebrew from Command Line):
==============================================================

Using the terminal, download and install Homebrew with this command::

    $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    
    
Run this command from the terminal to update and confirm install of Homebrew::

    $ brew doctor 

2. Install Vagrant and Virtualbox via Homebrew:
===============================================

Download, verify, and install VirtualBox::

    $ brew install Caskroom/cask/virtualbox
    
Download, verify, and install VirtualBox extension pack for your version of virtualbox::

    $ brew install Caskroom/cask/virtualbox-extension-pack

Download, verify, and install Vagrant::

    $ brew install Caskroom/cask/vagrant

Download, verify, and install Vagrant-Manager::

    $ brew install Caskroom/cask/vagrant-manager
    
Download, verify, and install Vagrant-ghost:
   
    $ vagrant plugin install vagrant-ghost

 
3. Start a Virtual Ubuntu Server:
=================================
Now that we have it all installed, let's spin up an Ubuntu server, log in to it, play, log out, and then destroy it.

From Command line enter the following to make a sandbox directory, cd into it, and then download the Ubuntu::

    $ mkdir sandbox && cd sandbox 
    $ vagrant box add precise64 http://files.vagrantup.com/precise64.box
    
Initialize the installation inside the sandbox folder (aka make the Vagrantfile). (You can modify the Vagrantfile and look at it after this step.)::

    $ vagrant init precise64 
    
Start the Ubuntu server via Vagrant by typing this at command line::

    $ vagrant up
    
To login to the new server via ssh, enter the following via command line::

    $ vagrant ssh
    
Change what you like. Mess it up if you care to. Once done poking around logout::

    $ exit
    
To destroy the Ubuntu virtual server installation::

    $ vagrant destroy
    
To rebuild from the OS again::

    $ vagrant up


vagrant-hbase-solr
==================

WIP



```
 λ  vagrant provision
==> default: Running provisioner: shell...
==> default: Setting javahome to /usr/lib/jvm/java-7-oracle/
==> default: stdin: is not a tty
==> default: Screen with namenode already running
==> default: Screen with datanode already running
==> default: Screen with resourcemanager already running
==> default: Screen with nodemanager already running
==> default: Screen with hbasemaster already running
==> default: Screen with solr already running
==> default: Done
==> default:
==> default: hbasemaster: http://172.16.64.151:60010/
==> default: namenode: http://172.16.64.151:50070/
==> default: datanode: http://172.16.64.151:50075/
==> default: resource manager: http://172.16.64.151:8088/
==> default: nodemanager: http://172.16.64.151:8042/
==> default: solr: http://172.16.64.151:8983/solr/
==> default:
==> default: to attach to screen run:
==> default:   sudo screen -x solr-vagrant
==> default:
```

puppet-todo
-----------

zk
==
standalone zookeeper: http://apache.miloslavbrada.cz/zookeeper/zookeeper-3.4.6/zookeeper-3.4.6.tar.gz
zkCli in path




