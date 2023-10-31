# django

1. 프로젝트 생성

```
django-admin startproject <pjtname> .
```

2. 가상환경 설정
```
python -m venv venv
```

3. 가상환경 활성화/비활성화
```
<!-- Window -->
source venv/Scripts/activate
```

4. 가상환경 내부에 django 설치
```
pip install django
```

5. 서버 실행 확인(종료 `Ctrl+c`)
```
python manage.py runserver
```

6. 앱생성
```
django-admin startapp <appname>
```

7. 앱등록
- `settings.py`의 `INSTALLED_APPS`에 등록
    `<appname>`을 등록

8. `url.py`
```python
from django.contrib import admin
from django.urls import path
from app_intro import views

urlpatterns = [
    ...
    path('admin/', admin.site.urls),
    path('index/', view.index),
]
```
