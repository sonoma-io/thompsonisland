# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"

  config.vm.hostname = "wp-box"

  config.vm.network :private_network, ip: "192.168.50.4"

  # If true, then any SSH connections made will enable agent forwarding.
  # Default value: false
  # config.ssh.forward_agent = true

  # Drive mapping
  config.vm.synced_folder "db/data/", "/var/lib/mysql", :mount_options => [ "dmode=777", "fmode=777" ]

  # Provisioning
  #config.vm.provision :shell, :path => "config/vagrant/provision.sh"
end
