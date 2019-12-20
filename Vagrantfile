# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/bionic64"
  config.ssh.insert_key = false

  config.vm.provision "pipsetup", type:'ansible' do |ansible|
    ansible.playbook = "provisioning/tasks/setup_pip.yml"
  end
  
  config.vm.provision "mongosetup", type:'ansible' do |ansible|
    ansible.playbook = "provisioning/tasks/install_mongodb.yml"
  end
  
  config.vm.provision "dbconfig", type:'ansible' do |ansible|
    ansible.playbook = "provisioning/tasks/config_db.yml"
  end

  config.vm.provision "replset", type:'ansible' do |ansible|
    ansible.playbook = "provisioning/tasks/replica_set.yml"
  end
  
end
