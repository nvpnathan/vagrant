Vagrant.configure(2) do |config|

  # Specify the default SSH username and private key
  config.ssh.username = "ubuntu"
  config.ssh.private_key_path = "~/.ssh/privkey.pem"

  # Configure the OpenStack provider for Vagrant
  config.vm.provider "openstack" do |os|

    # Specify OpenStack authentication information
    os.openstack_auth_url = "https://vio.corp.local:5000/v2.0"
    os.openstack_network_url = "https://vio.corp.local:9696/v2.0"
    os.username = "demo"
    os.password = "VMware1!"
    os.tenant_name = "demo"

    # Specify instance information
    os.server_name = "vagrant-test"
    os.flavor = "m1.tiny"
    os.image = "ubuntu-trusty-cloudimg"
    os.floating_ip_pool = "ext-net"
    os.networks = "vagrant-net"
    os.keypair_name = "demo"
    os.security_groups = ["default"]
  end
end
