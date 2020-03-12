#This vagrant file will be for mostly testing deployment
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"

  config.vm.hostname = "idp.test.renu.ac.ug"

  config.vm.network "public_network", ip: "196.43.159.38"

  #
   config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
     vb.gui = true
     vb.name = "Ubuntu16 IdP"

  #
  #   # Customize the amount of memory on the VM:
     vb.memory = "1024"
   end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
   config.vm.provision "shell", inline: <<-SHELL
     sudo apt update
     sudo apt install -y software-properties-common
     sudo apt-add-repository --yes --update ppa:ansible/ansible
     sudo apt install -y ansible cowsay sshpass apache2
     sudo apt upgrade -y
   SHELL
end
