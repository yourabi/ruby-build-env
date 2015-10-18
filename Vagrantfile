# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true

    # Customize the amount of memory on the VM:
    vb.memory = "2048"

    vb.customize ["modifyvm", :id, "--vtxvpid", "on", "--vrde", "on"]
  end

  config.vm.box = "opscode_ubuntu-14.04"

  config.vm.provider "virtualbox" do |v, override|
    override.vm.box_url = "http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_ubuntu-14.04_chef-provisionerless.box"
  end

  config.vm.provider "vmware_fusion" do |v, override|
    override.vm.box_url = "http://opscode-vm-bento.s3.amazonaws.com/vagrant/vmware/opscode_ubuntu-14.04_chef-provisionerless.box"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/playbook.yml"
  end
end
