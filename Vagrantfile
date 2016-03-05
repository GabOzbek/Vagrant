
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.



Vagrant.configure(2) do |config|

	config.vm.define "docker-wildfly" do |dockerwildfly|
	config.ssh.forward_agent = true 		
	config.vm.boot_timeout = 30
	config.ssh.insert_key = false
	

 		dockerwildfly.vm.provider "docker" do |wildfly|
			wildfly.has_ssh = true
			wildfly.vagrant_vagrantfile = "./dockerhost/Vagrantfile"
			wildfly.build_dir = "dockerhost/wildfly"
			wildfly.name = "wildfly"		
			wildfly.remains_running = true
			wildfly.vagrant_machine = "docker-host"
			wildfly.ports = ["8080:8080"]
 		end
	end


	config.vm.define "docker-db" do |dockerdb|
	config.ssh.forward_agent = true 		
	config.vm.boot_timeout = 30
	config.ssh.insert_key = false

 		dockerdb.vm.provider "docker" do |db|
			db.has_ssh = true
			db.vagrant_vagrantfile = "./dockerhost/Vagrantfile"
			db.build_dir = "dockerhost/database"
			db.vagrant_machine = "docker-host"
			db.name = "oraclelinux"		
			db.remains_running = false
			db.ports = ["49161:1521"]
 		end
	end




end

  
