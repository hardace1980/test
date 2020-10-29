# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false

   config.vm.provider "virtualbox" do |vb|
       vb.gui = false
       vb.memory=2048
       vb.cpus=2
   end

   config.vm.define "web" do |web|
      web.vm.network "public_network", use_dhcp_assigned_default_route: true
      web.vm.hostname = "web"
   end

   config.vm.define "db" do |db|
      db.vm.network "public_network", use_dhcp_assigned_default_route: true
      db.vm.hostname = "db"
   end

end