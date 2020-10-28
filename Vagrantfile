# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.boot_timeout = 600
  config.vm.box_check_update = false

  config.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory=1024
      vb.cpus=2
      vb.check_guest_additions=false
  end

  config.vm.define "web" do |web|
      web.vm.network  "private_network", ip: "192.168.0.100"
      web.vm.hostname = "web"
	  end

 config.vm.define "db" do |db|
     db.vm.network "private_network", ip: "192.168.0.101"
     db.vm.hostname = "db"
 end
end
