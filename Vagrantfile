Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false
  
  config.vm.provider "virtualbox" do |vb|
       vb.gui = true
       vb.memory=2048
       vb.cpus=2
   end

  config.vm.define "web" do |machine|
    machine.vm.network "public_network", ip: "192.168.88.50"
  end

  config.vm.define "db" do |machine|
    machine.vm.network "public_network", ip: "192.168.88.51"
  end

  config.vm.define 'controller' do |machine|
    machine.vm.network "public_network", ip: "192.168.88.52"

    machine.vm.provision :ansible_local do |ansible|
      ansible.playbook       = "playbook.yml"
      ansible.verbose        = true
      ansible.install        = true
      ansible.limit          = "all"
      ansible.inventory_path = "hosts"
    end
  end

end