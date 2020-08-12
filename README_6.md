# LikeLion_Dreamary
### URL과 Template을 효율적으로 관리하는 법

<오늘 할 내용>
1. URL Include 이해& 구현
    * URL Include : 앱 별로 URL을 관리할 수 있도록 구조화 
    
    * 실습
        1. 앱 폴더 내에 urls.py구축

2. Template 상속 구현
    * base.html 생성
    * base.css 생성 // css는 위에서 아래로 덮어쓰면서 읽음

    * 페이지별 다른 내용은 다음을 통해 유동성 있도록 함
    ```
    {% block content %}
    {% endblock %}
    ```

    * 다른 페이지에선 base.html를 상속으로해서 사용
    ````
    {% extends 'base.html' %}
    ````
    