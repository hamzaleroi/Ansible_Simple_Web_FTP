
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.define "ftp-server" do |ftp|
    ftp.vm.network "private_network", ip: "10.0.0.3"
    ftp.vm.provision "ansible" do |ansible|
      ansible.playbook = "ftp.yml"
    end
  end
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "256"
    vb.gui = false
  end
end
