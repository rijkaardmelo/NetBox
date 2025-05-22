Vagrant.configure("2") do |config|
    config.vm.box = "debian/bookworm64"

    config.vm.define "netbox" do |netbox|
        netbox.vm.hostname = "netbox"
        
        netbox.vm.network "public_network", 
            ip: "10.90.0.200",
            netmask: "255.255.255.0",
            bridge: "enp2s0f0",
            use_dhcp_assigned_default_route: true

        netbox.vm.provider "virtualbox" do |vb|
            vb.cpus = 4
            vb.memory = 8192
            vb.name = "netbox"
        end

    end

end
