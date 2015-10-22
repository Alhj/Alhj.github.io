Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty32"

  config.vm.network "forwarded_port", guest: 3000, host: 8080

  # Jekyll github-pages port
  config.vm.network "forwarded_port", guest: 4000, host: 4000
  
  config.vm.network "forwarded_port", guest: 5858, host: 5858

  config.vm.provision :shell, :path => "provision.sh"
  config.vm.provision :shell, :path => "install-node.sh", privileged: false
  config.vm.provision :shell, path: "install-rvm.sh", args: "stable", privileged: false
  config.vm.provision :shell, path: "install-ruby.sh", args: "2.2.1 bundler", privileged: false
  
end

