# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

Vagrant.configure(2) do |config|

  config.vm.box = "wcs-centos-6.6"
  config.vm.box_url = "https://s3.eu-central-1.amazonaws.com/wcs-vms/wcs-centos-6.6.virtualbox.box"

  # Application server.
  config.vm.define "wcs-server" do |app|
    app.vm.hostname = "wcs.192.168.60.5.xip.io"
    app.vm.network :private_network, ip: "192.168.60.5"
    app.vm.network "forwarded_port", guest: 8080, host: 8080, auto_correct: true
    app.vm.network "forwarded_port", guest: 1521, host: 1521, auto_correct: true      
    app.vm.network "forwarded_port", guest: 9090, host: 9090, auto_correct: true
  end  
end

