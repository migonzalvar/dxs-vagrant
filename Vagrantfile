# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "fedora18"

  #config.vm.box = "opscode_centos-6.4-i386_provisionerless"
  #config.vm.box_url = "https://opscode-vm.s3.amazonaws.com/vagrant/opscode_centos-6.4-i386_provisionerless.box"

  config.vm.network :public_network

  config.ssh.forward_agent = true

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.inventory_file = "ansible_hosts"
  end

end
