# LikeLion_Dreamary

### 드리머리_ 헬로 장고
1. 가상환경 & PIP이해
* 가상환경이란?
    자신이 원하는 파이썬 환경 구축을 위해 필요한 모듈만 담아놓은 바구니   
    장고할때 무조건 가상환경 키고하기       
* PIP란?
    파이썬으로 작성된 패키지 소프트웨어를 관리하는 패키지 관리 시스템
    장고를 설치해주는 도구      

* 실습시작!
    + 레포지토리 생성
    + .gitignore 파일 만들고 gitignore.io 사이트에서 우리가 사용하는 django, visualcode, python 치고 내용 복붙 // 일일이 올리지않아도 되는 파일들 따로지정, 캐시
    + media 밑에 venv쓰기 // venv는 따로 올리지 않겠다 선언
        
    + 가상환경 만들기 : python -m venv venv
    + 가상환경 키기: source venv/Scripts/activate   
        가상환경을 키면 (venv) 뜸
    + 장고 설치하기 : pip install django
    + 프로젝트 폴더 생성 : django-admin startproject dreamaryproject .  
    + 로컬서버 키기 : python manage.py runserver
    + manage.py : 장고에서 중요한 파일

* 프로젝트와 앱
    - 하나의 프로젝트 == 하나의 웹사이트
    - 프로젝트 안의 의미있는 기능들을 각각의 앱으로 관리
        + 앱 생성 : python manage.py startapp page
        + 프로젝트한테 새로운 앱이 생겼다고 알려주기        
        dreamayproject - settings.py - INSTALLED_APPS에 'page.apps.pageConfig', 추가        

* django 파일 알아보기
    * settings.py : 전체 프로젝트를 관리하는 설정 파일 
    * urls.py : 프로젝트의 url 관리파일

* django 앱 알아보기
    * views.py : 웹 요청을 받고, 전달받은 데이터를 처리해서 가공하는 파일

* 홈페이지 출력하기
    1. settings.py : 프로젝트에세 앱의 존재 알리기
    2. Templates : User에게 보여줄 HTML 파일 만들기
    3. views.py : 요청이 들어오면 HTML 파일을 열어주는 함수 정의
    4. urls.py : url요청을 views와 연결     
    // path()는 크게 3가지로 나누어짐       
        어떤주소, 어떤함수, 장고전체에서 어떻게 부를지


        