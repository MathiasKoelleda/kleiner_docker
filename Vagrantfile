# -*- mode: ruby -*-

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.define "docker1" do |docker1|
    docker1.vm.hostname = "docker1"
    docker1.vm.network "private_network", ip: "192.168.100.100"
    docker1.vm.provider "virtualbox" do |vb|
      vb.name = "docker1"
      vb.cpus = "2"
      vb.memory = "4096"
      sudo apt-get update

      sudo apt-get install \
         apt-transport-https \
         ca-certificates \
         curl \
         gnupg \
         lsb-release
         sudo apt-get update

         sudo apt-get install docker-ce docker-ce-cli containerd.io
         sudo apt-get install docker-ce=<VERSION_STRING> docker-ce-cli=<VERSION_STRING> containerd.io        
    end
    docker1.vm.provision "shell" , path: "scripts/docker-provision.sh"
  end
end
    