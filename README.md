
sudo su

apt update

apt upgrade

wget https://download.java.net/java/ga/jdk11/openjdk-11_linux-x64_bin.tar.gz -O /tmp/openjdk-11+28_linux-x64_bin.tar.gz

mkdir /usr/lib/jvm/

tar xfvz /tmp/openjdk-11+28_linux-x64_bin.tar.gz --directory /usr/lib/jvm/

rm /etc/alternatives/java

ln -s /usr/lib/jvm/jdk-11/bin/java /etc/alternatives/java

sudo apt install python3-setuptools

pip3 install influxdb==5.2.3 --break-system-packages

apt install ansible git -y

git clone https://github.com/hasmukh007/ruuvigw.git

cd ruuvigw/

ansible-playbook -i "127.0.0.1," ruuvigw.yml
