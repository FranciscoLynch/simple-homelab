## 1. Install

- Vagrant: https://www.vagrantup.com/docs/installation
- Oracle Virtualbox: https://www.vagrantup.com/docs/providers/virtualbox

### Clone the repository

```
git clone https://github.com/FranciscoLynch/simple-homelab.git
```

### Enter the lab

```
cd simple-homelab 
```

Check if the cpu and memory is ok for your setup.

```
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
```
Once it's ready

```
vagrant up
```

Once it's done

```
vagrant ssh
```

## Break a leg!