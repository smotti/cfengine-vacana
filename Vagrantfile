# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "cargomedia/debian-7-amd64-plain"
  config.vm.provision "ansible" do |a|
    a.playbook = "provision/common.yml"
    a.sudo = true
  end

  config.vm.define :hub do |hub|
    hub.vm.network "private_network", ip: "192.168.100.3"
    hub.vm.synced_folder "./var/cfengine/masterfiles/", "/var/cfengine/masterfiles",
      owner: "root", group: "root"
    hub.vm.synced_folder "./var/cfengine/modules/", "/var/cfengine/modules",
      owner: "root", group: "root"
    hub.vm.synced_folder "./var/cfengine/prototypes/", "/var/cfengine/prototypes",
      owner: "root", group: "root"
    hub.vm.provision "ansible" do |a|
      a.playbook = "provision/hub.yml"
      a.sudo = true
    end
#    hub.vm.provision "cfengine" do |cf|
#      cf.am_policy_hub = true
#    end
    hub.vm.provider "virtualbox" do |v|
      v.name = "vacana_hub"
      v.cpus = 1
      v.memory = 256
    end
  end

  config.vm.define :node do |node|
    node.vm.network "private_network", ip: "192.168.100.4"
    node.vm.provision "ansible" do |a|
      a.playbook = "provision/node.yml"
      a.sudo = true
    end
#    node.vm.provision "cfengine" do |cf|
#      cf.policy_server_address = "192.168.123.3"
#    end
    node.vm.provider "virtualbox" do |v|
      v.name = "vacana_node"
      v.cpus = 1
      v.memory = 256
    end
  end
end
