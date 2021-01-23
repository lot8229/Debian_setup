# 1과제 setup
- sudo 명령어 가 먹지 않을떄
```
su 
apt update
apt install sudo
username -aG sudo username
export PATH = "$PATH:/sbin:/usr/sbin:usr/local/sbin"
```
- apache2 가 설치 되지 않았을떄
```
sudo apt-get install apache2
sudo apt-get update
cd etc/apache2/mods-enabled

ln ../mods-available/userdir.conf userdir.conf
ln ../mods-available/userdir.load userdir.load

mkdir public_html
touch public_html/index.html

su
apache2 restart
```
-mariana DB 설치
```
