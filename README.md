# README

Vagrant example for a simple LAMP-Stack (http://en.wikipedia.org/wiki/LAMP_%28software_bundle%29).
To get more information about vagrant visit http://vagrantup.com/

Please install the following requirements for your operating system:
 * VirtualBox 4.3.28+  (http://virtualbox.org) 
 * Vagrant 1.7.2+ (http://vagrantup.com) 
 * Windows: git-scm (http://git-scm.com/)

The example contains:
 * Ubuntu 14.04 Server
 * PHP
 * Java, Tomcat, mod_jk
 * Python, mod_wsgi

Getting started: 
 * Start VM: 
```
cd PATH/TO/THIS/DIR
vagrant up
```
   Note: the first run of this command downloads a basic virtual box (VB) and installs within VB all dependencies you need to run your project ("provisionising"). It can take long in the first run.
 * Open Browser in your host: http://localhost:8080

Customization
 * Customize install script (THISDIR/config/shell/custom.sh)
 * Add your application source in source folder 
 * Customize apache config (THISDIR/config/files/apache/)
 * Destroy and start VM
```
cd PATH/TO/THIS/DIR
vagrant destroy
vagrant up
```
 - To turn off the VB: ```vagrant halt```
 - To navigate into VB (via ssh): ```vagrant ssh```
