VAGRANTFILE_API_VERSION = '2'

# puts 'Dropboxに置いている .zsh_history を参照できるようにする'
# FileUtils.mkdir_p("#{ENV['HOME']}/dev/_backup/dotfiles")
# FileUtils.ln_sf("#{ENV['HOME']}/Dropbox/backup/dotfiles/.zsh_history", "#{ENV['HOME']}/dev/_backup/dotfiles/.zsh_history")

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box'

  config.vm.network 'private_network', ip: '192.168.33.10'

  config.vm.provider 'virtualbox' do |v|
    v.memory = 1024
    v.cpus = 2
  end

  # nfs: trueで画像の読み込みなど速くなった
  # http://dev.akinaka.net/2014/01/14/vagrant-synced-folder-nfs-setting
  config.vm.synced_folder '~/dev', '/root/dev', type: 'rsync'

  # `vagrant ssh` したとき `root` でログインする
  config.ssh.username = 'root'

  # rootでSSH接続するためにVagrantが生成したauthorized_keysをrootでも使う
  config.vm.provision 'shell', inline: 'sudo cp -f /home/vagrant/.ssh/authorized_keys /root/.ssh'

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'playbooks/site.yml'
  end
end
