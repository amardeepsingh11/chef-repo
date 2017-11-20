Vagrant.configure("2") do |config|
config.vm.box = "bento/ubuntu-16.04"
config.vm.box_url = "https://vagrantcloud.com/bento/boxes/ubuntu-16.04/versions/201710.25.0/providers/virtualbox.box"
config.omnibus.chef_version = :latest
config.berkshelf.enabled = true
config.vm.provision :chef_client do |chef|
    chef.provisioning_path = "/etc/chef"
    chef.chef_server_url = "https://api.chef.io/organizations/devops11"
    chef.validation_key_path = "devops11-validator.pem"
    chef.validation_client_name = "devops11-validator"
    chef.node_name = "server"
  end
end
