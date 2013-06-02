Vagrant::Config.run do |config|
  config.vm.box = "squeeze193chef"
  #config.vm.box_url = "http://packages.diluvia.net/squeeze64-ruby193.box"
  config.vm.network :hostonly, "33.33.33.10"
  config.vm.share_folder "v-cookbooks", "/cookbooks", "."
  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = "."
    chef.add_recipe "apt"
    chef.add_recipe "nginx"
  end
end
