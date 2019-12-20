# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/bionic64"
  config.ssh.insert_key = false

  config.vm.provision "replset", type:'ansible' do |ansible|
    ansible.playbook = "provisioning/main.yml"
  end
  
end
