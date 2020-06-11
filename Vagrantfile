Vagrant.configure("2") do |config|
  config.vm.box = "debian/stretch64"
  if ENV['FIRST_RUN'] == 'true'
    config.vbguest.auto_update = false
    config.vm.synced_folder ".", "/vagrant", disabled: true
  else
    config.vm.synced_folder ".", "/vagrant", create: true, type: "virtualbox"
    config.vm.synced_folder "./www", "/var/www", create: true, type: "virtualbox", owner: "www-data", group: "www-data"
  end
end
