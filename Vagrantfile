Vagrant.configure("2") do |config|
  config.vm.define "mastery" do |subconfig|
    subconfig.vm.box = "sbeliakou/centos"
    subconfig.vm.hostname = "mastery"
    subconfig.vm.network :private_network, ip: "192.168.56.120"
    config.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--memory", 2048]
      v.name="mastery"
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
  end

  config.vm.define "workers" do |subconfig|
    subconfig.vm.box = "sbeliakou/centos"
    subconfig.vm.hostname = "workers"
    subconfig.vm.network :private_network, ip: "192.168.56.130"
    config.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--memory", 1512]
      v.name="workers"
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
  end
end  

