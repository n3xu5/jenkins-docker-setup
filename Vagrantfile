Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/xenial64"
    config.vm.network "private_network", ip: "192.168.50.11"
    config.vm.provider "virtualbox" do |v|
        v.memory = 1024

        # Only allow drift of 1 sec, instead of 20 min default
        v.customize [ "guestproperty", "set", :id, "/VirtualBox/GuestAdd/VBoxService/--timesync-set-threshold", 1000 ]
    end
end
