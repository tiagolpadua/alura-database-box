Vagrant.configure("2") do |config|
	config.vm.define "alura-database" do |db|
		db.vm.box = "ubuntu/bionic64"
		db.vm.provision "shell", path: "assets/install.sh"
		db.vm.provision "file", source: "assets/mysqld.cnf", destination: "/tmp/mysqld.cnf"
		db.vm.provision "file", source: "assets/script-inicial.sql", destination: "/tmp/script-inicial.sql"
		db.vm.provision "shell", path: "assets/post-install.sh"
	end
end