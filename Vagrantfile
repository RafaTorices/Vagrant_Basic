
# Vagrantfile para provisionar un servidor Ubuntu 22.04 con VirtualBox

Vagrant.configure("2") do |config|
  # Especificar la caja (box) que se va a usar
  config.vm.box = "ubuntu/jammy64"
  config.ssh.insert_key = false

  # Configuracion del nombre de la VM
  config.vm.define "ubuntu2204" do |ubuntu2204|
    ubuntu2204.vm.hostname = "ubuntu2204"

    # Configuracion de red (puedes personalizarla segun tus necesidades)
    ubuntu2204.vm.network "private_network", ip: "192.168.56.10"

    # Configuracion de VirtualBox
    ubuntu2204.vm.provider "virtualbox" do |vb|
      vb.name = "Ubuntu 22.04 Server"
      vb.memory = "2048" # memoria RAM asignada a la VM
      vb.cpus = 2 # n#mero de CPUs asignadas a la VM
    end
  end
end

