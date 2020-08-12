# LikeLion_Dreamary
### QuerySet & Method에 대해 알기 + PK, Get_object_or_404 활용

#### <지난 내용 복습>
* Model
    * MVT 패턴의 하나의 요소
    * 데이터에 접속하고 관리하도록 도와주는 객체
    * 모델 생성 -> DB가 알아듣도록 번역 -> 번역한 내용을 DB에 적용
    
    번역
    ```
    python manage.py makemigrations (+ 앱 이름)
    ```

    DB적용
    ```
    pyhton manage.py migrate (+ 앱 이름)
    ```

#### <오늘 할 내용>
* QuerySet, Method 이해&구현        
    * QuertSet : 전달받은 객체의 목록
   
    * 실습
    views.py )      
    1. 모델의 존재 알려주기
    ```     
        from .models import Designer
    ```    

    2. QuerySet을 Tempaltes로 보내기
    ```
        def home(request):      
          designers =Designer.objects.all()
          return render(request,'home.html',{'designers':designers})
    ```      


* PK, Get_object_or_404 이해
    * Detail Page 구현
    
    PK (Primary Key)     
    ````
    * 모델을 통해 생성된 객체들을 구분할 수 있는 고유한 키

    * Id로 등록됨

    ````

    Path Convertor
    ````
    * 여러 객체의 url을 계층적으로 다룰수 있도록 도와주는 도구 
    ````
    
    get_object_or_404
    ````
    * Object를 가져오려 했는데 없을 경우 나타나는 에러
    * views.py의 pk변수명과 urls.py의 변수명은 같아야 함
    ````

