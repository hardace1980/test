Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false

  config.vm.define "web" do |web|
      web.vm.network  "public_network", ip: "10.10.0.2"
      web.vm.hostname = "web"  
      web.vm.provider "virtualbox" do |vb|
         vb.memory = "1024"
      end
  end

 config.vm.define "db" do |db|
     db.vm.network "public_network", ip: "10.10.0.3"
     db.vm.hostname = "db"  
     db.vm.provider "virtualbox" do |vb|
         vb.memory = "1024"
     end
 end


end
