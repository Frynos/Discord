# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
    config.vm.box = "ubuntu/xenial64"
    config.vm.provision :shell, path: "scripts/vagrant-bootstrap.sh"
    config.vm.provision :shell, inline: "echo 'ignore \"Inappropriate ioctl for device\"'; systemctl restart nginx", run: "always"
    # config.vm.network "forwarded_port", guest: 80, host: 3000
    config.vm.network "forwarded_port", guest: 443, host: 8443
end
