# bad-us_infra

#1. Make ssh key on local machine and identificate this key

ssh-keygen -t rsa -f ~/.ssh/appuser -C appuser -P ""
ssh-add ~/.ssh/appuser

#2. Use ssh with key

ssh -i ~/.ssh/appuser -A appuser@84.201.141.78

#3. Connect to local machine

ssh 10.129.0.31

#4* Connecting to local machine by hostname

add in file /etc/hosts or c:\windows\system32\drivers\etc\hosts host record 

10.129.0.31 someinternalhost

#or

add to file ~/.ssh/config

Host someinternalhost
HostName 10.129.0.31
User root
ProxyCommand ssh -A root@bastion nc %h %p

Host bastion
HostName 84.201.141.78
User root

# IP addresses

bastion_IP = 84.201.141.78
someinternalhost_IP = 10.129.0.31
domen name = otusler.completo.su

# Home Work 4 Yandex Cloud. Yandex CLi


# Connect:

testapp_IP = 158.160.108.33
testapp_port = 9292
test_url = http://158.160.108.33:9292

# Scripts

- install_ruby.sh
- install_mongodb.sh
- deploy.sh

# Start and run

    ./startup-script.sh
