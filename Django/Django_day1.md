# Django 혼자 시작해보기(window)

## 1. Django 시작할 폴더 생성

> 나만의 가상환경 생성하기
```
python -m venv myvenv
```

> 생성한 myvenv를 활성화
```
myvenv\Scripts\activate 실행
(생성한 가상환경명)
```

> 활성화 되었는지 확인
```
(myvenv) C:\django> 처럼 앞에 가상환경명이 붙었으면 설정 완료
```

> DJango 설치
```
pip install Django
```

> 샘플 프로젝트 만들어보기
```
django-admin startproject myweb .
```

> 현재 위치에 myweb 폴더와 manage.py가 생성되었는지 확인  
> App을 추가해보기
```
python manage.py startapp photo
```

> photo 폴더가 생성된 것을 확인
> 프로젝트 실행해보기

```
python manage.py runserver
```

>뭔가 오류 메세지가 많이 뜨지만 실행은 된거를 확인  
> http://127.0.0.1:8000 에서 실행을 확인  
> 8000은 Django 기본 포트번호
> 정상 실행 확인 후 터미널에서 Ctrl + C 입력하여 종료

-------------------------

## Django 프로젝트 구성요소

### 1. managy.py
   - django.core.management module에서 execute_from_command 함수
    호출하여 사용자 입력 명령어 처리
   - 직접 건드릴일은 거의없고 명령어 처리해주는 파일

### 2. settings.py
   - 프로젝트의 설정 파일
     - 자주 사용하는 옵션
        > DEBUG = TRUE   
        > 오류가 발생했을경우 에러가 웹페이지에 그대로 노출  
        > 개발시에는 켜놓고 사용하고 사용자들에게는 배포할때는 꺼놓고 배포

        > ALLOWED_HOSTS = []  
        > 허용할 호스트 주소, 로컬에서는 기본으로 설정되어 있기떄문에 작성할 필요 없지만
        > 배포할때에는 배포하는 서버의 호스트 주소를 입력

        > INSTALLED_APPS = [...]  
        > 설치된 앱들을 등록하는 옵션, 새 프로젝트를 추가했을때 이곳에 선언해주어야 정상 적용  

### 3. urls.py
   - 프로젝트의 url주소를 등록해놓은 파일
   - 내부의 path()를 사용하여 원하는 주소를 등록