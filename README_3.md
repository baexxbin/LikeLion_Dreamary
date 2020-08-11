# LikeLion_Dreamary

### 드리머리_Django가 관리하는 법
< 오늘 할 내용 >
```
1. 템플릿 언어를 통해 여러 페이지 관리
2. Static file 관리하기
```

< 지난 시간 복습 >
```  
* 가상환경 : 자신이 원하는 파이썬 환경 구축을 위해 필요한 모듈만 담아 놓은 바구니       
    (venv)꼭 키고 진행하기!!!

    * PIP : 패키지 관리 시스템
```
1. bootstrap 적용
    * bootstrap이란 : 프론트앤드 개발을 빠르고 쉽게 할 수 있는 오픈 소스        

    * 실습!
    부트스트랩에서 디자인 따와서 수정하기

2. URL / Template 언어이해 & 구현
    * URL 괸리는 어떻게?        
        장고에서 URL관리는 urls.py의 urlpatterns에서 담당

    * path의 구조
    ```
    path('introduce/', views.introduce, name = "introduce"),        

    introduce/ : 주소창에 쓰는 주소     
    views.introduce : 사용자 요청이 들어왔을때 반환해주는 함수        
    name = "introduce" : 장고프로젝트 안에서 이 URL이 어떤 이름으로 불릴지 // 해당 path를 대표하는 이름          
    ```
    * Template 언어
    ```
    local서버에서 각각의 페이지를 띄우기 위해서 필요한 특별한 언어      

    {{}} : 템플릿 변수("명사")        
        장고에서 html과 서로 쓸 수 있도록 연동을 위한 언어, 보통 결과값 같은것을 변수로 나타내 출력할 때 씀

    {%%} : 템플릿 태그("동사")        
        URL을 부르거나 반복문, 조건문 같은걸 html에서 할 수 있도록
    ```

3. Static 파일 (Image,CSS) 이해
    * Static File이란?      
      내용이 고정되어있어 응답을 할 때 파일을 그대로 보내주면 되는 파일     
    
    * Static : 웹 서비스를 위해 개발자가 준비해두는 파일

    * Media : 웹 서비스 이용자들이 업로드하는 파일  

    * Static File 처리하기
    ```
    STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'page', 'static')
    ]
    --> static 파일을 어디서 모아올지

    STATIC_ROOT = os.path.join(BASE_DIR, 'static')
    --> 이렇게 모은 static파일들을 어디다 둘지 // static이라는 폴더에 둔다

    {% load static %} : html에서 사용할때, 맨 위에 적어주기
    ```
    로컬서버도 하나의 서버이기 때문에 템플릿 언어로 스태틱 파일 읽어오기


