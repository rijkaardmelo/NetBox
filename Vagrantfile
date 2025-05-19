Vagrant.configure("2") do |config|
    config.vm.box = "debian/bookworm64"

    config.vm.define "netbox" do |netbox|
        netbox.vm.hostname = "netbox"
        
        netbox.vm.network "public_network", 
            ip: "192.168.31.200",
            netmask: "255.255.255.0",
            bridge: "wlp0s20f3",
            use_dhcp_assigned_default_route: true

        netbox.vm.provider "virtualbox" do |vb|
            vb.cpus = 2
            vb.memory = 4096
            vb.name = "netbox"
        end
    end

end
