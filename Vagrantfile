Vagrant.configure("2") do |config|
  config.vm.box = "jumperfly/centos-7-ansible"
  config.vm.network "forwarded_port", guest: 80, host: 8080
# Provisioning configuration for Ansible.
  config.vm.provision "ansible" do |ansible|
    ansible.galaxy_role_file = "requirements.yml"
    ansible.playbook = "deploy.yml"
     ansible.sudo = true
   end
 
end
