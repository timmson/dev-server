# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

    config.vm.box = "ubuntu/bionic64"
    
    config.vm.network "forwarded_port", host:10000, guest:10000
    config.vm.network "forwarded_port", host:12000, guest:12000
    config.vm.network "forwarded_port", host:8100, guest:8100
    config.vm.network "forwarded_port", host:8180, guest:8180
    config.vm.network "forwarded_port", host:8182, guest:8182
    config.vm.network "forwarded_port", host:8280, guest:8280
    config.vm.network "forwarded_port", host:8380, guest:8380
    config.vm.network "forwarded_port", host:8480, guest:8480
    config.vm.network "forwarded_port", host:8500, guest:8500

    config.vm.provider "virtualbox" do |v|
      v.memory = 4096
      v.cpus = 4
    end

    config.vm.provision "shell", inline: <<-SHELL
        apt-add-repository -y ppa:ansible/ansible
        apt update
        apt -y install ansible git
    SHELL

    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "site.yml"
        ansible.raw_arguments = ["-c local"]
    end

end
