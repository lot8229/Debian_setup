# Debian Setup
## - Isntall Debian

ftp.kaist.ac.kr
에서 데비안 10.0.7 버전 설치 

vm ware 설치 후 데비안 iso 파일 넣기 

vm ware tools 설치 

vi etc/sudoers 파일 열어서 
%wheel ALL=(ALL:ALL) ALL

<유저이름> ALL=ALL(ALL:ALL) ALL

으로 고친후 sudo 로 아파치 설치 

sudo apt-get install apache2

아파치 2 의 셋팅은 apache2_setup.md 애서

apt update

apt install sudo   
usermod -aG sudo <유저이름>

>Path 오류 잡는 방법  
export PATH="$PATH:/sbin:/usr/sbin:usr/local/sbin"

이러면 잡힐뜻 하다.
