# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.define :deb6 do |deb6_config|
    deb6_config.vm.box = "debian6-64-envpuppet-latest"
    deb6_config.vm.host_name = "testdeb.example.com"
    deb6_config.vm.box_url = "http://files.penumbra.be/vagrant/debian6-64-envpuppet-latest.box"
    deb6_config.vm.provision :puppet do |puppet|
        puppet.manifests_path = "puppet/manifests"
        puppet.module_path = "puppet/modules"
        puppet.manifest_file  = "site.pp"
    end
  end
  config.vm.define :el6 do |el6_config|
    el6_config.vm.box = "centos6-64-envpuppet-latest"
    el6_config.vm.boot_mode = :gui
    el6_config.vm.host_name = "testcentos.example.com"
    el6_config.vm.box_url = "http://files.penumbra.be/vagrant/centos6-64-envpuppet-latest.box"
    el6_config.vm.provision :puppet do |puppet|
        puppet.manifests_path = "puppet/manifests"
        puppet.module_path = "puppet/modules"
        puppet.manifest_file  = "site.pp"
    end
  end
end
