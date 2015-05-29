# -*- mode: ruby -*-
# vi: set ft=ruby :


## vagrant documentation: http://docs.vagrantup.com


VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  ## 32 bit 
  config.vm.box = "ubuntu/trusty32"
  config.vm.provider :virtualbox do |vb|
    vb.customize [ "modifyvm", :id, "--hwvirtex", "off"]
  end
  ##
  ## 64 bit 
  #config.vm.box = "ubuntu/trusty64"
  ##

  ## cpu, ram
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 1
  end

  ## shared folder (default is mounted the folder of this Vagrantfile on the host under /vagrant on the guest)
  config.vm.synced_folder "src/", "/vagrant_data/"

  ## forwarded ports
  config.vm.network "forwarded_port", guest: 80, host: 8080  

  ## hostname
  config.vm.hostname = "dev.local"

  ## assign IP address
#  config.vm.network "private_network", ip: "192.168.50.4"

  ## NOTE: 
  ## to activate DNS, add the following entry to your local hosts file (http://en.wikipedia.org/wiki/Hosts_%28file%29)
  ## (FORMAT: <IPADRESS> <HOSTNAME>)
  ##
  ## 192.168.50.4 dev.local

  ## provision
  config.vm.provision :shell, :path => "config/shell/lamp_base.sh"
  config.vm.provision :shell, :path => "config/shell/custom.sh"
  ##
end
