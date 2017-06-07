# Vagrant Example: LampX-Stack

Vagrant example for a simple LAMP-Stack (http://en.wikipedia.org/wiki/LAMP_%28software_bundle%29).
To get more information about vagrant visit http://vagrantup.com/

The example contains:

 * Ubuntu 16.04 Server
 * PHP
 * Java, Tomcat, mod_jk

## Requirements 

Please install the following requirements for your operating system:

 * VirtualBox 5.1.22+  (http://virtualbox.org) 
 * Vagrant 1.9.5+ (http://vagrantup.com) 
 * Windows: git-scm (http://git-scm.com/)

## Getting started guide

see [GettingStarted.md](https://github.com/kwies/vagrant-examples/blob/master/GettingStarted.md)

## Customization
 * Customize install script (THISDIR/config/shell/custom.sh)
 * Add your application source in source folder 
 * Customize apache config (THISDIR/config/files/apache/)
 * Destroy and start VM
```
cd PATH/TO/THIS/DIR
vagrant destroy
vagrant up
```
 * To turn off the VB: ```vagrant halt```
 * To navigate into VB (via ssh): ```vagrant ssh```

