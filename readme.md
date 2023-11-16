# Dolphin
## 웹 사이트 구축 방법

### 1. APMSETUP.exe 파일 실행


### 2. APM_Setup 파일 압축해제 (Path : C:\ )
APMSETUP.exe 설치 완료 후 웹 브라우저에 ‘127.0.0.1’입력

아래와 같은 화면이 보이면 설치 성공

<img width="568" alt="스크린샷 2023-11-16 오후 11 53 36" src="https://github.com/5uhye0n/Dolphin/assets/149215175/025f5a56-4e89-49a7-a446-e08947c9ffa8">


### 3. mysql 설치 확인
### ```cmd```

    $ mysql -u root -p
    password : apmsetup
입력 시 로그인이 성공하는지 확인

<img width="563" alt="스크린샷 2023-11-16 오후 11 54 12" src="https://github.com/5uhye0n/Dolphin/assets/149215175/2ba20140-f0db-4ea8-a7a5-3a613509eeb7">

```mysql>```에 ```C:\APM_Setup\htdocs\WHS_Dolphin\query.txt``` 파일의 내용을 ```ctrl+c``` ```ctrl+v``` 하면 데이터베이스 구축이 완료


### 4.웹 브라우저에 ```http://127.0.0.1/WHS_Dolphin/index.php``` 입력

<img width="558" alt="스크린샷 2023-11-16 오후 11 54 32" src="https://github.com/5uhye0n/Dolphin/assets/149215175/120cb77f-3a1a-46f3-a43e-b7bec65cc987">

위와 같이 웹 페이지가 나온다면 구축 성공


## 페이지 실행이 안되는 경우 
### 1. 파일 위치 확인
```C:\APM_Setup\htdocs\WHS_Dolphin```

### 2. ```C:\APM_Setup\php.ini``` 수정


<img width="564" alt="스크린샷 2023-11-16 오후 11 54 45" src="https://github.com/5uhye0n/Dolphin/assets/149215175/b82fc8b6-2652-4f9b-8902-c63d6d65a0ba">

```magic_quotes_gpc```를  ```On```이 아니라 ```Off```로 수정 & 저장(On일 경우 공격 불가)

### 3. APMSETUP Monitor실행
-Apache2 ```STOP``` ->  ```START``` 눌러 Apache2 재시작

<img width="432" alt="스크린샷 2023-11-16 오후 11 54 58" src="https://github.com/5uhye0n/Dolphin/assets/149215175/e998b060-ec86-40a9-9a5e-26e372d84e8e">
