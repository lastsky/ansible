VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos/7"
  config.vm.network "private_network", type: "dhcp"

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook-all.yml"
    ansible.vault_password_file = ".vault-pass"
    ansible.verbose = 'vvvvvvvv'
    ansible.groups = {
     "hardware" => ["default"]
    }
    end
end
