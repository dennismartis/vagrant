Vagrant.configure("2") do |config|

  config.ssh.insert_key = false

  (1..3).each do |i|
    config.vm.define "node-#{i}" do |node|
      node.vm.network "private_network", ip: "172.17.177.#{20 + i}"
      node.vm.box = "geerlingguy/centos7"
      node.vbguest.auto_update = false
      node.vm.hostname = "node#{i}"
      node.vm.provider "virtualbox" do |v|
        v.name = "node-#{i}"
      end
    end
  end
end