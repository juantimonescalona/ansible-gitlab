Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = ".yml"
  end
end
