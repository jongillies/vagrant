# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.ssh.username = 'ubuntu'
  config.vm.box = 'ubuntu/xenial64'
  config.vm.hostname = 'devops'
  config.vm.network :private_network, ip: '172.28.128.10'

  config.vbguest.auto_update = false

  config.vm.provider :virtualbox do |vb|
    vb.memory = 2048
    vb.cpus = 2
  end

  # Make sure python is installed for Ansible the provisioner
  config.vm.provision 'shell', inline: 'apt-get install -y python-minimal'

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'playbook.yml'
    ansible.sudo = true
    # ansible.verbose = 'vvv'
    # ansible.extra_vars =
  end

end
