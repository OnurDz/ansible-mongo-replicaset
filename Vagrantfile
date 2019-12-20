# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.ssh.insert_key = true

  config.vm.provision "replset", type:'ansible' do |ansible|
    ansible.playbook = "ansible/tasks/main.yml"
  end
  
end
