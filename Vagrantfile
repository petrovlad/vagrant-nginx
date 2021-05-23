NETWORK_BASE = "192.168.56."
WORKSTATION_IP_HOST = 1
VM_IP_HOST = 10
Vagrant.configure("2") do |config|

  config.vm.box = "sbeliakou/centos"

  config.vm.network "private_network", ip: "#{NETWORK_BASE}#{VM_IP_HOST}"
  config.vm.hostname = "nginx-server"
  config.vm.provision "shell", path: "provision.sh", args: "#{NETWORK_BASE}#{WORKSTATION_IP_HOST}"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "Vagrant-NGINX-VM"
    vb.memory = "1024"
  end
  
  
end
