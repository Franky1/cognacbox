# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = "reddingwebpro/cognacbox"
    config.vm.hostname = "cognacbox"
    config.vm.boot_timeout = 600  # increased from default 300
    # config.vm.network "forwarded_port", guest: 80, host: 8080
    config.vm.network "private_network", ip: "192.168.33.10"
    config.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=777"]

    config.vm.provider "virtualbox" do |virtualbox|
        virtualbox.name = "Cognac Box"
        virtualbox.gui = true
        virtualbox.memory = 4096
        virtualbox.cpus = 2
        # virtualbox.customize [ "modifyvm", :id, "--uartmode1", "disconnected" ]
    end
end
