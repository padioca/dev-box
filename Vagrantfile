# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  config.vm.box      = 'ubuntu/trusty64'

  config.vm.network :forwarded_port, guest: 3000, host: 3000
  config.vm.network :forwarded_port, guest: 80, host: 8080

  config.vm.provision :shell, path: 'bootstrap.sh', keep_color: true

  config.vm.synced_folder '.', '/vagrant'
  config.vm.network 'private_network', ip: '192.168.50.5' # ensure this is available

  config.vm.provider "virtualbox" do |v|
  	v.memory = 4096
  	v.cpus = 2
  end
  
end
