# -*- mode: ruby -*-
# vi: set ft=ruby :

# Database Configuration
mysql_root_password   = "root"   # We'll assume user "root"

Vagrant.configure("2") do |config|

  config.vm.box = "scotch/box"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.hostname = "scotchbox"
  config.vm.synced_folder "churchinfo", "/var/www/public", :mount_options => ["dmode=777", "fmode=666"]

   config.vm.provision :shell, :path => "bootstrap.sh"
end