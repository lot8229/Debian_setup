# Linux Server Setup
> 1. Debian 설치  
- ftp.kaist.ac.kr 에서 debian 파일 설치
- vmware 설치 
- vmware 에 데비안 iso 파일 설치
 
DeskTop Environment 는 GUI 환경을 구성 할때만 사용하고 Server 용 Linux 에서는 사용하지 않는것을 권장한다. 

GNOME 과 WEBSERVER 만 설치하여 사용중이다,
> 2.sudoers 관련 설정
```
 su
 vi etc/sudoers
```
파일 을 열어서 적절한 위치에 

``` 
%wheel ALL=(ALL:ALL) ALL
유저이름 ALL=(ALL:ALL) ALL
```
을 넣어준다.
- sudo 명령어 가 먹지 않을떄
```
su 
apt update
apt install sudo
username -aG sudo username
export PATH = "$PATH:/sbin:/usr/sbin:usr/local/sbin"
```
> 3. vmware tools 설치

vmware 위의 탭바의 virtual machine --> install vmware tools

cd rom 이 마운트 되면 cd rom 에서 관련 압축파일 extract 

extract 한 위치로 이동 후 .pl 인스톨 파일 실행 

init6 로 reboot

> 4. 아파치 설치 확인 및 아파치 관련 설정

- 아파치 설치를 데비안 설치 시 함 (webserver 관련 파일 설치시)

- symboliclink 로 걸어준다.
```
ln ../mods-available/userdir.conf userdir.conf    
ln ../mods-available/userdir.load userdir.load
```

> 리눅스 에서 비프음 없에는 법

 ```
 seterm -blength 0
 ```

 > 5. mysql(maria DB) 설치하는 방법
https://mariadb.org/download/#mariadb-repositories 
여기서 알맞게 자신의 환경에 맞는 것을 선택한후에 

설치전 가이드의 명령어를 따라하여 먼저 해준다.

그리고 나서 
```
sudo apt-get install mariadb-server mariadb-client
```
를 리눅스에 적용시켜준다.

```
systemctl restart mysql
systemctl start mysql
```
을 하여서 리눅스를 재설치 해준다,


적용 전에 포트 3306 을 방화벽에 혀용해주는 명령어

ufw allow 3306 이란 명령어가 not found 이다.

--> 해결 : ufw 를 설치후 다시 하면 된다.
