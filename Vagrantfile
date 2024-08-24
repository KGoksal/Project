# Specify Vagrant version and configure settings
Vagrant.configure("2") do |config|

  # Enable Vagrant Hostmanager plugin to manage host entries
  config.hostmanager.enabled = true 
  config.hostmanager.manage_host = true
  
  ### DB VM ###
  config.vm.define "db01" do |db01|
    db01.vm.box = "eurolinux-vagrant/centos-stream-9"  # Base box image
    db01.vm.hostname = "db01"  # Hostname of the VM
    db01.vm.network "private_network", ip: "192.168.56.55"  # Private network IP
    db01.vm.provider "virtualbox" do |vb|  # VirtualBox specific settings
      vb.memory = "600"  # Memory allocation for the VM
    end
  end
  
  ### Memcache VM ###
  config.vm.define "mc01" do |mc01|
    mc01.vm.box = "eurolinux-vagrant/centos-stream-9"
    mc01.vm.hostname = "mc01"
    mc01.vm.network "private_network", ip: "192.168.56.54"
    mc01.vm.provider "virtualbox" do |vb|
      vb.memory = "600"
    end
  end 
  
  ### RabbitMQ VM ###
  config.vm.define "rmq01" do |rmq01|
    rmq01.vm.box = "eurolinux-vagrant/centos-stream-9"
    rmq01.vm.hostname = "rmq01"
    rmq01.vm.network "private_network", ip: "192.168.56.53"
    rmq01.vm.provider "virtualbox" do |vb|
      vb.memory = "600"
    end
  end
  
  ### Tomcat VM ###
  config.vm.define "app01" do |app01|
    app01.vm.box = "eurolinux-vagrant/centos-stream-9"
    app01.vm.hostname = "app01"
    app01.vm.network "private_network", ip: "192.168.56.52"
    app01.vm.provider "virtualbox" do |vb|
      vb.memory = "800"
    end
  end
  
  ### Nginx VM ###
  config.vm.define "web01" do |web01|
    web01.vm.box = "ubuntu/jammy64"
    web01.vm.hostname = "web01"
    web01.vm.network "private_network", ip: "192.168.56.51"
    web01.vm.provider "virtualbox" do |vb|
      vb.gui = true  # Enable GUI mode
      vb.memory = "800"  # Memory allocation for the VM
    end
  end
  
end
