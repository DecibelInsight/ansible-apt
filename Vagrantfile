# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.provision "shell",inline: <<-SHELL
      apt-get update && apt-get install -y python2.7
      update-alternatives --install /usr/bin/python python /usr/bin/python2.7 2
  SHELL
  config.vm.provision 'ansible'do |ansible|
      ansible.playbook = "./apt.yml"
      ansible.sudo = true
      ansible.groups = {
        'all' => ['default'],
        'all:vars' => {
            'apt_region' => ENV.fetch('APT_REGION', 'default'),
        }
      }
  end

end
