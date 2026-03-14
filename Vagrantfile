Vagrant.configure("2") do |config|
  config.vbguest.auto_update = false
  config.vm.synced_folder "./BashScript", "/Bash"

  # Master Node
  config.vm.define "master" do |master|
    master.vm.box = "ubuntu/jammy64"
    master.vm.hostname = "k8s-master" # Set automatically
    master.vm.network "private_network", ip: "192.168.56.10"
    master.vm.provision "shell", path: "./BashScript/bootstrap.sh"
    master.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
  end

  # Worker Nodes
  [1, 2].each do |i|
    config.vm.define "web0#{i}" do |node|
      node.vm.box = "ubuntu/jammy64"
      node.vm.hostname = "k8s-worker-0#{i}" # Set automatically
      node.vm.network "private_network", ip: "192.168.56.#{30+i}"
      node.vm.provision "shell", path: "./BashScript/bootstrap.sh"
      node.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
        vb.cpus = 2
      end
    end
  end
end