# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Requisito: Box Debian Bookworm
  config.vm.box = "debian/bookworm64"
  config.vm.hostname = "hugo.anolivia"
  config.vm.network "private_network", ip: "192.168.56.154"
  # ------------------

  config.ssh.insert_key = false

  if Vagrant.has_plugin?("vagrant-vbguest")
    config.vbguest.auto_update = false
  end

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.name = "Projeto02-Hugo"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook_ansible.yml"
    ansible.become = true
  end
end
