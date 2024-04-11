Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"

  config.vm.network "private_network", ip: "192.168.56.10"

  # Installation d'apache2 via un script shell (provisioning)
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y apache2
  SHELL

  # Il existe une autre syntaxe pour ajouter un script shell :
  # config.vm.provision "shell", path: "monScript.sh"
  # Ensuite, traper la commande : vagrant provision
end