웹페이지를 돌리기위해 다음과 같은 작업을 실시해 주어야한다.

1. pip install django, pip install requests 등 import한 모듈을 전부 깔아준다
2. main 디렉토리의 apps.py 파일에서는 공공데이터 포털의 api를 받아온다. 하지만 서비스 키 부분을 공란으로 남겨두었기
때문에 공공데이터 포털에 접속후 해당 api 사용 신청을하고 받은 서비스 키를 8번줄에 있는 코드에 추가해야한다.
3. 링크는 그대로 사용하면 될 것이지만 만약 ssl인증서 오류가 난다면 링크의 주소를 https말고 http로 사용해야한다.(링크가 두개 있으니 오류나면 둘다 바꿔주는 것이 좋을 듯)

4. 다음은 main의 templates 디렉토리에 index.html 파일의 155번쨰 줄의 src = 부분 링크에 본인 카카오맵 api키를 추가하고 소괄호는 지워주면 된다.
5. 카카오맵 api에 본인이 서비스한 ip주소를 추가해야 맵에서 정보를 받아올 수 있다

6. 마지막으로 config 디렉토리에 sttings.py 파일의 29번쨰 줄 allowed_hosts에 본인이 서비스 할 ip를 추가해주어야 한다.
만약 로컬에서 돌라는거면 127.0.0.1만 있어도 된다.

7. 이제 서버를 돌릴때 터미널창에 python manage.py runserver 명령어를 치고 포트 8000번으로 접속하면 된다.