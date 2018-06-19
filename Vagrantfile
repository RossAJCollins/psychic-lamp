# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  
  config.vm.define "host1" do |host1|
    host1.vm.network "private_network", ip: "192.168.33.20"
    host1.vm.hostname = "Vagrant-box1"
    host1.vm.provider "virtualbox" do |vb1|
      vb1.memory = 1024
      vb1.name = "Box1"
     end
   end

  config.vm.define "host2" do |host2|
    host2.vm.network "private_network", ip: "192.168.33.21"
    host2.vm.hostname = "Vagrant-box2"
    host2.vm.provider "virtualbox" do |vb2|
     vb2.memory = 1024
     vb2.name = "Box2"
    end
  end

 # config.vm.provider "virutalbox" do |vb|
  #  vb.mmemory = 1024
 # end  

  config.vm.provision "ansible" do |ansible| 
    ansible.playbook="provisioning/playbook.yml"
   end
 end


