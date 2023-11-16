# Dolphin


웹 사이트 구축 방법

1.APMSETUP.exe 파일을 실행시켜 APMSETUP을 설치합니다. APM_Setup 파일을 압축해제 하신다음 로컬 디스크 C에 저장합니다.
APMSETUP.exe 설치가 완료되고 크롬과 같은 웹 브라우저에 ‘127.0.0.1’입력 하면
이렇게 화면이 보이면 설치에 성공하신 겁니다.

<img width="568" alt="스크린샷 2023-11-16 오후 11 53 36" src="https://github.com/5uhye0n/Dolphin/assets/149215175/025f5a56-4e89-49a7-a446-e08947c9ffa8">

2. mysql이 설치 되어있는지 확인
cmd 창을 열어서 ‘mysql -u root -p'를 입력하시고 password에 ’apmsetup‘을 입력했을 때 로그인이 성공하는지 확인하면 됩니다.

<img width="563" alt="스크린샷 2023-11-16 오후 11 54 12" src="https://github.com/5uhye0n/Dolphin/assets/149215175/2ba20140-f0db-4ea8-a7a5-3a613509eeb7">

이렇게 mysql>이 나오면 성공입니다.
그런 다음에 
mysql> 여기에 WHS_Dolphin 폴더에 있는 query.txt파일의 내용을 복사 붙여넣기 해주시면 데이터베이스가 구축이 됩니다.

그런 다음 웹 브라우저에 http://127.0.0.1/WHS_Dolphin/index.php 이렇게 입력하시면 

<img width="558" alt="스크린샷 2023-11-16 오후 11 54 32" src="https://github.com/5uhye0n/Dolphin/assets/149215175/120cb77f-3a1a-46f3-a43e-b7bec65cc987">

이렇게 웹 페이지가 나오면 구축에 성공하신 겁니다.
페이지 실행이 안된다면 파일 위치 이렇게 되어 있는지 확인
C:\APM_Setup\htdocs\WHS_Dolphin


그리고 APM_Setup에 들어가서 readme.txt 위에 php.ini라는 파일이 보일텐데 그 파일을 열어서
 
<img width="564" alt="스크린샷 2023-11-16 오후 11 54 45" src="https://github.com/5uhye0n/Dolphin/assets/149215175/b82fc8b6-2652-4f9b-8902-c63d6d65a0ba">

이부분이 On이 아니라 Off로 수정하시고 저장하셔야 저희 공격이 가능해 집니다.
그리고 저장하신 다음에는 
여기 화면에서 Apache2를 STOP하시고 다시 START를 눌러서 Apache2를 재시작해주세요.

<img width="432" alt="스크린샷 2023-11-16 오후 11 54 58" src="https://github.com/5uhye0n/Dolphin/assets/149215175/e998b060-ec86-40a9-9a5e-26e372d84e8e">
