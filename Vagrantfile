Vagrant.configure("2") do |config|

  # Specify the default SSH username and private key
  config.vm.box = "dummy"
  config.ssh.username = "ubuntu"
  config.ssh.private_key_path = "~/nness.pem"

  # Configure the OpenStack provider for Vagrant
  config.vm.provider :openstack do |os|

    # Specify OpenStack authentication information
    os.endpoint= "https://openstack.vballin.com:5000/v2.0/tokens"
    os.api_key = "VMware1!"
    os.username = "nness"
    os.tenant_name = "nness"

    # Specify instance information
    os.server_name = "vagrant-test"
    os.flavor = "m1.small"
    os.image = "ubuntu-trusty-cloudimg"
    os.floating_ip = :auto
    os.floating_ip_pool = "ext-net"
    os.network = "vagrant-net"
    os.keypair_name = "nness"
    os.security_groups = ["default"]
  end
end
