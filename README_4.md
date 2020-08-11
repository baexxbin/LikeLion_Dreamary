# LikeLion_Dreamary
### Model과 Admin에 대해 알아보기

<오늘 할 것>
1. Model 이해
    * Model이란?        
    데이터에 접속하고 관리하도록 도와주는 객체.
    장고와 데이터베이스 서로 소통할 수 있게 도와주는 것.        

    * 모델 생성 & 적용
        * models.py     # 모델명의 첫 글자는 무조건 대문자!     
        // 모델은 class로 틀을 정해줌
        ```
            1. class 모델명(models.Model):
                image = models.ImageFile(upload_to ='images/')      <!--이런식으로 name, address등등 넣어주기 -->
        ```
        * Terminal
        ```
            1. python manage.py makemigrations (+ 앱 이름)  
            // 변역을 하는 것   

            2. pyhton manage.py migrate (+ 앱 이름) 
            // 끝나고 난 다음 변역한 내용 DB에 적용 
        ```
        # models.py까지는 장고안의 파일임으로 장고가 알아들을 수 있음
        
        # 데이터베이스는 장고와 별개이기 때문에 못알아들음, 장고가 뭐라뭐라해도 DB못알아들음
        
        # makemigrations : DB가 알아들을 수 있도록 변역해주는 것

2. Model과 Database의 연동이해 & 실습
    * 실습
    Pillow --> 장고에서 이미지를 올리고 작업할때 활용가능 

3. Admin 파악
    * 장고는 admin 기능 기본 제공
    * Terminal
    ``` python manage.py createsuperuser  ```

    * admin에게 Model 알려주기

