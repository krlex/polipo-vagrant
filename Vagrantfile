# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "debian/buster64"
  config.vm.network "forwarded_port", guest: 80, host: 5678, ip: "192.168.33.11"
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provision/site.yml"
  end
end
