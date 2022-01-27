# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/bionic64"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end

  config.vm.provision "shell", inline: "curl -sfL https://get.k3s.io | sh -"
end

# https://learn.hashicorp.com/tutorials/vagrant/getting-started-index
