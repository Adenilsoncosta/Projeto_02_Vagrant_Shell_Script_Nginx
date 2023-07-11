Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vb|
    vb.name = "Projeto_02_Vagrant_Shell_Script_Nginx"
    vb.memory = "1024"
    vb.cpus = "1"
  end

  config.vm.box = "hashicorp/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 8090   
  config.vm.network "public_network", ip: "192.168.0.40"
  config.vm.provision "shell", path: "script.sh"
  config.vm.synced_folder "site/", "/var/www/html"
end

