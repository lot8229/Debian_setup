# Linux File Tree
> 파일 구분
```
d >> 디렉토리 
l >> 파일
```

>파일 설명 

media : cd 나 usb 등의 파일 관련

r >> 읽기권한
w >> 쓰기권한
x >> 실행권환

>psswd 파일 

사용자의 패스워드 파일을 기록죽이다.

[id][사용자][uid][groupid][?][그파일의 주소?]

>shadow 파일 
>group 파일 

가장 중요한 파일

>sudo 
사용자가 루트의 권한을 갖게 하는 것

** 권환 중요하다. 

>alias 

시험에 나올정도는 아니다,

>.파일

숨김 파일이다. ls 명령어를 통해서 존재확인을 할수 있다.

>symbol link

soft link : 바로가기를 생성 할때 inode 가 새로 생겨서 서로 다른 inode 가 생성되는 것.

hard link : 바로 가기를 생성 할떄 inode 가 똑같은 파일을 생기게 한다.

>chmod 

drxr--r--r-- 같은 권한을 바꿔주는 것.
 user | group | other 

 chmod 755 -->권한으로 10진수로 바꿈 

>chown 

소유자를 바꿔주는 것이다.

>find /home -name  gsm


>/var

변수나 가변적인 것들을 저장하는 공간

>block 장치

cdrom 등 추가적인 메모리 장치

>mount 

블록장치를 넣어주는것

반대 :umount