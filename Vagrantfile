# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

    config.vm.box = "ubuntu/bionic64"

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
