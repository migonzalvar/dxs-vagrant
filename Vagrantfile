# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "fedora-18-i386"

  config.vm.network :public_network, :mac => "080027CAFECA"

  config.ssh.forward_agent = true

	config.vm.synced_folder ".", "/vagrant", :disabled => true

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
  end

end
