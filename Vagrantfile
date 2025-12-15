Vagrant.configure("2") do |config|
  config.vm.box = "debian/bookworm64"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 1
  end

  # ===================== ARQ =====================
  config.vm.define "arq" do |arq|
    arq.vm.hostname = "arq.tyrone.victor.devops"
    arq.vm.network "private_network", ip: "192.168.56.123"

    arq.vm.provider "virtualbox" do |vb|
      vb.customize ["createhd", "--filename", "arq-disk1.vdi", "--size", 10240]
      vb.customize ["createhd", "--filename", "arq-disk2.vdi", "--size", 10240]
      vb.customize ["storageattach", :id, "--storagectl", "SATA Controller",
                     "--port", 1, "--device", 0, "--type", "hdd",
                     "--medium", "arq-disk1.vdi"]
      vb.customize ["storageattach", :id, "--storagectl", "SATA Controller",
                     "--port", 2, "--device", 0, "--type", "hdd",
                     "--medium", "arq-disk2.vdi"]
    end
  end

  # ===================== DB =====================
  config.vm.define "db" do |db|
    db.vm.hostname = "db.tyrone.victor.devops"
    db.vm.network "private_network", type: "dhcp"
  end

  # ===================== APP1 =====================
  config.vm.define "app1" do |app1|
    app1.vm.hostname = "app1.tyrone.victor.devops"
    app1.vm.network "private_network", type: "dhcp"
  end

  # ===================== CLI =====================
  config.vm.define "cli" do |cli|
    cli.vm.hostname = "cli.tyrone.victor.devops"
    cli.vm.network "private_network", type: "dhcp"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbooks/site.yml"
  end
end
