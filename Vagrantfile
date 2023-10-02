Vagrant.configure("2") do |config|
    config.vm.define "main-server" do |h|
        h.vm.box = "ubuntu/trusty64"
        h.vm.hostname = "main-server"
        h.vm.network "private_network", ip: "192.168.56.50"
        h.vm.provider "virtualbox" do |vb|
          vb.name = "main-sv"
          vb.memory = "4192"
          vb.cpus = 2
        end  
    end 
end