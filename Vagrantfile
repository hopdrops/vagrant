Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.provision "docker"

  config.vm.provision "shell", inline: "sudo apt-get -qq remove unattended-upgrades"

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--uartmode1", "disconnected"]
  end
end
