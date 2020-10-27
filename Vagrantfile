Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"
  
# добавляем машину для использования в качестве веб-сервера с установленным apache 2.4
  config.vm.define "web" do |machine|
    machine.vm.network "private_network", ip: "10.10.0.10"
  end
  
# добавляем машину для использования в качестве сервера базы данных с установленным MySQL
  config.vm.define "db" do |machine|
    machine.vm.network "private_network", ip: "10.10.0.11"
  end
  
# добавляем машину для использования в качестве сервера управления Ansible
  config.vm.define 'controller' do |machine|
    machine.vm.network "private_network", ip: "10.10.0.12"

    machine.vm.provision :ansible_local do |ansible|
      ansible.playbook       = "playbook.yml"
      ansible.verbose        = true
      ansible.install        = true
      ansible.limit          = "all"
      ansible.inventory_path = "hosts"
    end
  end

end
