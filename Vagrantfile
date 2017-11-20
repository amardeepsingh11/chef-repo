Vagrant.configure("2") do |config|

config.berkshelf.enabled = true

 config.vm.define "web" do |web|
  web.vm.box = "bento/ubuntu-16.04"
  web.vm.box_url = "https://vagrantcloud.com/bento/boxes/ubuntu-16.04/versions/201710.25.0/providers/virtualbox.box"
  web.omnibus.chef_version = :latest
  web.vm.provision :chef_client do |chef|
    chef.provisioning_path = "/etc/chef"
    chef.chef_server_url = "https://api.chef.io/organizations/devops11"
    chef.validation_key_path = "devops11-validator.pem"
    chef.validation_client_name = "devops11-validator"
    chef.node_name = "server"
  end
 end

 config.vm.define "db" do |db|
  db.vm.box = "bento/ubuntu-16.04"
  db.vm.box_url = "https://vagrantcloud.com/bento/boxes/ubuntu-16.04/versions/201710.25.0/providers/virtualbox.box"
  db.omnibus.chef_version = :latest
  db.vm.provision :chef_client do |chef|
    chef.provisioning_path = "/etc/chef"
    chef.chef_server_url = "https://api.chef.io/organizations/devops11"
    chef.validation_key_path = "devops11-validator.pem"
    chef.validation_client_name = "devops11-validator"
    chef.node_name = "server_db"
  end
 end

end
