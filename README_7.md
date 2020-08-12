# LikeLion_Dreamary
### CRUD #1

<오늘 할 내용>
* CRUD 개념 이해
    * Create / Read / Update / Delete
    # creat     
    새로운 객체를 생성해 데이터 저장        
    POST사용

    # Update        
    정보수정이 필요한 객체를 찾아, 데이터를 새롭게 저장     
    POST사용

    # DELETE        
    제거가 필요한 객체를 찾아 제거      


* GET / POST 이해
    * 클라이언트에서 서버로 요청을 보내는 방법
    * GET
    ```
    Data를 URL에 포함시켜 전송      
    캐싱가능,, // 캐시같은 느낌     
    REST에서 활용    
    ```

    * POST
    ```
    Data를 Body에 넣어 전송 (URL에서 노출X)     
    캐싱 불가능     
    CREATE / UPDATE에서 활용
    ```
    1. new.html
    ````      
        image라는 이름으로 file을 받음
        '등록 완료하기'버튼을 누르면 url 'create'를 실행
    ```` 

    2. views.py
    ````
        create하러 왔더니       
        request.FILES['image'] ,        
        image라는 이름으로 아까 요청에서 들어왔던 FILE을  POST라는 객체에 저장
    ````

## render VS redirect 차이점
    * render : 항상 요청과 함께 무언가를 반환, 어떠한값을 view에서 template으로 넘겨줌

    * redirect : save한다음 그냥 주소를 이동만 시켜줌

## views.py
    ````
    1. 파이썬으로 함수 생성
    2. 함수를 통해 내가 원하는 형태로 데이터 처리
    3. ~html로 데이터 보냄      
        * render함수
            * 데이터값을 받아온 후 html로 데이터 보냄.
        * request 인자
            * 어떠한 요청을 처리하기 위해 생성
    ````
    => 다른 html로 이동가능하도록 함수 만듦

## urls.py
    => views.py에서 만든 함수를 연결!          

    ````
    urlpatterns = [
        path()
    ]
    형태로 사용
    ````




