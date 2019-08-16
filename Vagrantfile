Vagrant.configure("2") do |config|
  config.vm.box = "debian/stretch64"

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end

  config.vm.provision "docker"
end
