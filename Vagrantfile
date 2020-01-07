
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  # config.vm.define "ftp-server" do |ftp|
  #   ftp.vm.network "private_network", ip: "192.168.5.6"
  #   ftp.vm.provision "ansible" do |ansible|
  #     ansible.playbook = "ftp.yml"
  #   end
  # end
  # config.vm.define "web-server" do |web|
  #   web.vm.network "private_network", ip: "192.168.5.7"
  #   web.vm.provision "ansible" do |ansible|
  #     ansible.playbook = "web.yml"
  #   end
  # end
  config.vm.define "nginx-web-server" do |web|
    web.vm.network "private_network", ip: "192.168.5.8"
    web.vm.provision "ansible" do |ansible|
      ansible.playbook = "web-nginx.yml"
    end
  end
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "256"
    vb.gui = false
  end
end
