Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "forwarded_port", guest: 80, host: 7845
# Provisioning configuration for Ansible.
  config.vm.provision "ansible" do |ansible|
    ansible.galaxy_role_file = "requirements.yml"
    ansible.playbook = "deploy.yml"
#    ansible.inventory_path = "environments/inventory.yml"
     ansible.sudo = true
  end

end
