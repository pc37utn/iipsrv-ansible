# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "centos/7"
  config.vm.network "private_network", ip: "192.168.33.12"
  config.vm.hostname = "iipsrv-vagrant"
  #config.vm.synced_folder "data/", "/vagrant/data", create: true

  config.vm.provider "virtualbox" do |vb|
    vb.name = "iipsrv-vagrant"
    vb.memory = "2048"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "iipsrv.yml"
    ansible.inventory_path = "hosts"
    ansible.limit = "iipsrv-vagrant"
    ansible.verbose = 'v'

    ansible.extra_vars = { ansible_ssh_user: 'vagrant'}
  end

end
