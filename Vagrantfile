# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.network :forwarded_port, guest: 80, host: 1234

  config.vm.network "public_network"

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y nginx
    apt-get install -y postgresql
    apt-get install -y nodejs monit
  SHELL
end
