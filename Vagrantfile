$global = <<SCRIPT
# install mysql
DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server
SCRIPT

Vagrant.configure("2") do |config|

    (1..2).each do |i|
      config.vm.define vm_name="web#{i}" do |node|
        node.vm.box = "apopa/nginx"
        node.vm.hostname = vm_name
      end
    end
    config.vm.define vm_name="mysql" do |node|
        node.vm.box = "ubuntu/xenial64"
        node.vm.provision "shell", inline: $global
        node.vm.hostname = vm_name
    end
  
  end