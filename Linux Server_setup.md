# Linux Server Setup
> 1. Debian 설치  
- ftp.kaist.ac.kr 에서 debian 파일 설치
- vmware 설치 
- vmware 에 데비안 iso 파일 설치
- 이다음 은 debiansetup.md 파일에서 
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
여기서 다알맞게 다운 후 리눅스에 적용?

적용 전에 포트 3306 을 방화벽에 혀용해주는 명령어

ufw allow 3306 이란 명령어가 not found 이다.