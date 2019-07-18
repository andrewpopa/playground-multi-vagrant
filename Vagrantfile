Vagrant.configure("2") do |config|
    (1..2).each do |i|
      config.vm.define vm_name="web#{i}" do |node|
        node.vm.box = "apopa/nginx"
        node.vm.hostname = vm_name
      end
    end
    config.vm.define vm_name="mysql" do |node|
        node.vm.box = "psysdev/basebox-ubuntu-14.04-java8-mysql"
        node.vm.hostname = vm_name
    end
  end