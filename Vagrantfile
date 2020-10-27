Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false

  config.vm.define "web" do |web|
      web.vm.network  "public_network", ip: "192.168.88.50"
      web.vm.hostname = "web"  
      web.vm.provider "virtualbox" do |vb|
         vb.memory = "1024"
      end
  end

 config.vm.define "db" do |db|
     db.vm.network "public_network", ip: "192.168.88.51"
     db.vm.hostname = "db"  
     db.vm.provider "virtualbox" do |vb|
         vb.memory = "1024"
     end
 end

 config.vm.define "controller" do |controller|
     controller.vm.network "public_network", ip: "192.168.88.52"
     controller.vm.hostname = "controller"  
     controller.vm.provider "virtualbox" do |vb|
         vb.memory = "1024"
     end
 end

end
