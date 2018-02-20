Vagrant.configure("2") do |config|

  Vagrant::DEFAULT_SERVER_URL.replace('https://vagrantcloud.com')

  config.vm.provider :virtualbox do |vb, override|
    override.vm.box = "bento/ubuntu-16.04"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "setup.yaml"
    ansible.inventory_path = "local.yaml"
    ansible.limit = "all"
  end

  config.vm.network "private_network", ip: "10.20.30.40"

end
