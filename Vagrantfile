# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "generic/ubuntu1804"

  config.vm.network "private_network", ip: "192.168.33.100"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "nodejs-box"
    vb.memory = "512"
  end

  config.vm.synced_folder ".", "/home/vagrant/temp-e-commerce-node-course"

  config.vm.provision "install-node", type: "shell", privileged: false do |s|
    s.path = "./install-node.sh"
  end

end