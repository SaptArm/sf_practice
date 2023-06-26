$setup_django = <<-'SCRIPT' 
echo "Install python3 Django" 
sudo apt-get update
sudo apt-get -y install python3 python3-pip libpq-dev gcc
sudo pip3 install psycopg2
sudo apt-get -y install python-django-common python3-django
SCRIPT

Vagrant.configure("2") do |config|
  
  config.vm.box = "bionic"

  config.vm.define "django" do |django|
    django.vm.provision :shell, inline: $setup_django
  config.vm.provision "file", source: "/home/administrator/vgrant/practice/emptyfile/111.py", destination: "$HOME/remote/emptyfile.py"
  end
end