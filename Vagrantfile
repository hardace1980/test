Vagrant.configure(2) do |config|

  config.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory=256
      vb.cpus=1
      vb.check_guest_additions=false
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false
  end

  config.vm.define "web" do |web|
      web.vm.network  "private_network", ip: "10.10.0.2"
      web.vm.hostname = "web"
	  web.vm.boot_time = 600
	  end

 config.vm.define "db" do |db|
     db.vm.network "private_network", ip: "10.10.0.3"
     db.vm.hostname = "db"
	 db.vm.boot_time = 600
 end
end
