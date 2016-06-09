# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure(2) do |config|
  config.vm.box = "cloudimg-trusty64"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  # config.vm.network "forwarded_port", guest: 80, host: 8880
  # config.vm.network "private_network", ip: "192.168.88.88"
  config.vm.network "public_network"
  # config.vm.synced_folder "~/vboxshare", "/mnt/vboxshare"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "Sandbox"
    # vb.gui = false
    vb.memory = "1024"
  end

  # Ansible provisioning
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yaml"
    # ansible.host_key_checking = false
    # ansible.verbose = "vvvv"
  end

end
