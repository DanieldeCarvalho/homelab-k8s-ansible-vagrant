Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"

  nodes = {
    "k8s-master" => "192.168.56.10",
    "k8s-worker-1" => "192.168.56.11",
    "k8s-worker-2" => "192.168.56.12"
  }

  nodes.each do |name, ip|
    config.vm.define name do |node|
      node.vm.hostname = name
      node.vm.network "private_network", ip: ip
      node.vm.provider "virtualbox" do |vb|
        vb.memory = 1028
        vb.cpus = 1
      end
      node.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y curl wget net-tools gnupg
      SHELL
    end
  end
end
