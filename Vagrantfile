# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  shared_host_folder = "./shared"

  config.vm.define "machine1" do |machine1|
    machine1.vm.box = "generic/debian12"
    machine1.vm.box_version = "4.3.12"

    machine1.vm.hostname = "machine1"
    machine1.vm.network "private_network", ip: "192.168.56.10"
  end

  config.vm.define "machine2" do |machine2|
    machine2.vm.box = "generic/debian12"
    machine2.vm.box_version = "4.3.12"

    machine2.vm.hostname = "machine2"
    machine2.vm.network "private_network", ip: "192.168.56.11"
  end

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "1024"
    vb.cpus = 2
  end

end