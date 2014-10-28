VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box'

  config.vm.network 'private_network', ip: '192.168.33.10'

  config.vm.provider 'virtualbox' do |v|
    v.memory = 1024
    v.cpus = 2
  end

  config.vm.synced_folder '~/dev', '/root/dev', type: 'nfs'
  config.vm.synced_folder '~/Dropbox/devenv', '/root/dropbox', type: 'nfs'

  # `vagrant ssh` したとき `root` でログインする
  config.ssh.username = 'root'

  # rootでSSH接続するためにVagrantが生成したauthorized_keysをrootでも使う
  config.vm.provision 'shell', inline: 'sudo cp -f /home/vagrant/.ssh/authorized_keys /root/.ssh'

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'playbooks/site.yml'
  end
end
