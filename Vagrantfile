# A Vagrant project with tools needed for development.
#
# Tools included:
# - Ubuntu Xenial
# - Terraform
# - AWS CLI
# - Ansible

Vagrant.configure(2) do |config|
	config.vm.network "public_network", bridge: "en1: Wi-Fi (AirPort)"
	config.vm.define "rrdesktop" do |devbox|
		devbox.vm.box = "ubuntu/xenial64"
    	#devbox.vm.network "private_network", ip: "192.168.199.9"
    	devbox.vm.hostname = "rrdesktop"
      	devbox.vm.provision "shell", path: "scripts/install.sh"
    	devbox.vm.provider "virtualbox" do |vbox|
			vbox.name = "rrdesktop"
    		vbox.memory = 4096
    		vbox.cpus = 2
    	end
	end
end
