Vagrant.configure("2") do |config|
  config.vm.define "kube01" do |kube01|
    kube01.vm.box = "ubuntu/focal64"
    kube01.vm.network "public_network", bridge: "wlp2s0", ip:"192.168.15.121"
    kube01.vm.hostname = "kube01"
    kube01.vm.provision "shell",
      inline: "apt update && apt upgrade -y"
    config.vm.provider "virtualbox" do |v|
    v.memory = 4196
    v.cpus = 4
  end
end
  config.vm.define "kube02" do |kube02|
    kube02.vm.box = "ubuntu/focal64"
    kube02.vm.network "public_network", bridge: "wlp2s0", ip:"192.168.15.122"
    kube02.vm.hostname = "kube02"
    kube02.vm.provision "shell",
      inline: "apt update && apt upgrade -y"
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end
end
  config.vm.define "kube03" do |kube03|
    kube03.vm.box = "ubuntu/focal64"
    kube03.vm.network "public_network", bridge: "wlp2s0", ip:"192.168.15.123"
    kube03.vm.hostname = "kube03"
    kube03.vm.provision "shell",
      inline: "apt update && apt upgrade -y"
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end
end
end