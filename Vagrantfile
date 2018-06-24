# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"

  config.vm.network "private_network", ip: "192.168.3.33"

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook/gremlinserver.yml"
    ansible.limit = "all"
    ansible.verbose        = true
    ansible.install        = true
    ansible.inventory_path = "playbook/local"
    ansible.raw_arguments  = [ "--connection=local" ]
  end
end
