Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.define "server"  do |server|
  	server.vm.hostname = "server"
  	server.vm.network :private_network, ip: "192.168.100.10"
  	server.vm.network :public_network
  end

  config.vm.define "client"  do |client|
  	client.vm.hostname = "client01"
	  client.vm.network :private_network, ip: "192.168.100.20"
  end
end
