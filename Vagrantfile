# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

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
