Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "private_network", ip: "192.168.21.120"
  config.vm.network "forwarded_port", guest: 80, host: 8083
  config.vm.network "forwarded_port", guest: 443, host: 8447

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "6144"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]   
  end  

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "vvv"
    ansible.playbook = "centos7-vagrant.yml"
  end

end
