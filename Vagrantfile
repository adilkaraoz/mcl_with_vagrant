# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.require_version ">= 2.0.0"
### configuration parameters
BOX_BASE = "adilkaraoz/mcl_requirements"
BOX_VERSION = "0.0.2"
BOX_CPU_COUNT = 2
BOX_RAM_MB = "4096"

### worker nodes configuration(s)
WORKER_IP_PATTERN = "192.168.2.10"
WORKER_COUNT = 1
WORKER_PREFIX = "worker0"

$script = <<-SCRIPT
echo enabling firewall...
sudo apt-get update && sudo apt-get install ufw ssh libgomp1 -y
echo y | sudo ufw enable
sudo ufw allow "OpenSSH" && sudo ufw allow 33824
echo creating swap...
sudo fallocate -l 4G /swapfile && sudo chmod 600 /swapfile
sudo mkswap /swapfile && sudo swapon /swapfile
echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
echo 'vm.swappiness=10' | sudo tee -a /etc/sysctl.conf
echo getting bootstrapfile to get some blocks...
cd /tmp
wget https://eu.bootstrap.dexstats.info/MCL-bootstrap.tar.gz
mkdir -p /home/vagrant/.komodo/MCL
sudo chown vagrant: /home/vagrant/.komodo
sudo chown vagrant: /home/vagrant/.komodo/MCL
rm -f /home/vagrant/.komodo/MCL/*
tar xf MCL-bootstrap.tar.gz -C /home/vagrant/.komodo/MCL
rm MCL-bootstrap.tar.gz
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vb|
    vb.cpus = BOX_CPU_COUNT
    vb.memory = BOX_RAM_MB
  end

  (1..WORKER_COUNT).each do |i|
    config.vm.define "#{WORKER_PREFIX}#{i}" do |node|
     node.vm.box = BOX_BASE
     node.vm.box_version = BOX_VERSION
      node.vm.box_check_update = false
      node.vm.hostname = "#{WORKER_PREFIX}#{i}"
      node.vm.network "private_network", ip: "#{WORKER_IP_PATTERN}#{i}", netmask: "255.255.255.0"
      node.vm.provision "shell", inline: "echo 'cd /vagrant' >> ~/.bashrc && exit", privileged: false
      node.vm.provider "virtualbox" do |v|
        v.customize ["modifyvm", :id, "--memory", BOX_RAM_MB]
      end
      node.vm.provision "shell" do |s|
        s.inline = $script
      end
    end
  end
end
