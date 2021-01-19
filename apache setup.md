# Apache Setup
## - Install Apache2
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

>오류

apache2 restart 명령어가 실행이 안된다.

apache2 를 설치는 되었지만 apache2 관련 명령어는 실행이 되지 않는다.

apache2 를 install 했을땐 apache2 버전이 최신버전이라고 나오지만.

apache2 -v 명령어은 실행이 되지 않는다 

apache2clf restart 를 입력하라는데 이것또한 되지 않는다.

<a src="https://starblood.tistory.com/entry/Debian-Apache-%EC%84%A4%EC%B9%98%EC%99%80-%EA%B0%9C%EC%9D%B8-home-directory-%EC%84%A4%EC%A0%95"><출처></a>
