# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "sajibasm"

  config.vm.network "forwarded_port", guest: 80, host: 80
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  config.ssh.forward_agent = true
  config.vm.synced_folder "./code", "/home/vagrant/code"
  
  config.vm.provider "virtualbox" do |v|
  v.memory = 1024
  end
  
  config.vm.provision "shell", path: "vm_provision/ubuntu14.sh"
end