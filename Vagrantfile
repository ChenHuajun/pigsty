Vagrant.configure("2") do |config|
    config.vm.box = "centos/7"
    config.vm.box_check_update = false
    config.ssh.insert_key = false

    config.vm.define "node0", primary: true do |s|
        s.vm.hostname = "node0"
        s.vm.network "private_network", ip: "10.10.10.10"
        s.vm.provider "virtualbox" do |v|
            v.linked_clone = true
            v.customize [
                    "modifyvm", :id,
                    "--memory", 2048,
                    "--cpus", "2",
                    "--nictype1", "virtio",
                    "--nictype2", "virtio",
                    "--hwvirtex", "on",
                    "--ioapic", "on",
                    "--rtcuseutc", "on",
                    "--vtxvpid", "on",
                    "--largepages", "on"
                ]
        end
        s.vm.provision "shell", inline: "/vagrant/bin/setup-node.sh"
    end

    config.vm.define "node1" do |s|
        s.vm.hostname = "node1"
        s.vm.network "private_network", ip: "10.10.10.11"
        s.vm.provider "virtualbox" do |v|
            v.linked_clone = true
            v.customize [
                    "modifyvm", :id,
                    "--memory", 1024,
                    "--cpus", "1",
                    "--nictype1", "virtio",
                    "--nictype2", "virtio",
                    "--hwvirtex", "on",
                    "--ioapic", "on",
                    "--rtcuseutc", "on",
                    "--vtxvpid", "on",
                    "--largepages", "on"
                ]
        end
        s.vm.provision "shell", inline: "/vagrant/bin/setup-node.sh"
    end

    config.vm.define "node2" do |s|
        s.vm.hostname = "node2"
        s.vm.network "private_network", ip: "10.10.10.12"
        s.vm.provider "virtualbox" do |v|
            v.linked_clone = true
            v.customize [
                    "modifyvm", :id,
                    "--memory", 1024,
                    "--cpus", "1",
                    "--nictype1", "virtio",
                    "--nictype2", "virtio",
                    "--hwvirtex", "on",
                    "--ioapic", "on",
                    "--rtcuseutc", "on",
                    "--vtxvpid", "on",
                    "--largepages", "on"
                ]
        end
        s.vm.provision "shell", inline: "/vagrant/bin/setup-node.sh"
    end

        config.vm.define "node3" do |s|
            s.vm.hostname = "node3"
            s.vm.network "private_network", ip: "10.10.10.13"
            s.vm.provider "virtualbox" do |v|
                v.linked_clone = true
                v.customize [
                        "modifyvm", :id,
                        "--memory", 1024,
                        "--cpus", "1",
                        "--nictype1", "virtio",
                        "--nictype2", "virtio",
                        "--hwvirtex", "on",
                        "--ioapic", "on",
                        "--rtcuseutc", "on",
                        "--vtxvpid", "on",
                        "--largepages", "on"
                    ]
            end
        s.vm.provision "shell", inline: "/vagrant/bin/setup-node.sh"
        end
end