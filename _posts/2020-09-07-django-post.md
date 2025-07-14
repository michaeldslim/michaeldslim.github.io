---
title: "Install Python Django"

categories:
  - Blog
tags:
  - django
last_modified_at: 2020-09-08T19:10:00-0700
---

### Install python django (Mac OS + Python3)

```
pip install pipenv
```

next step: create a django project folder (for example, Django)

```
mkdir Django

cd Django

pipenv install django==2.2
```

```
pipenv shell

django-admin startproject django_project .

python manage.py runserver (to see a welcome page)
```

ctrl+c to exit

next step: create an app

```
python manage.py startapp hello
```

### Run django

next step: open the project's settings.py add the app name (for example, hello)

```
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'hello', ✅
]
```

next step: create a view, open the views.py in the app (hello) folder and add these

```
from django.http import HttpResponse

def myView(request):
    return HttpResponse('Hello world')
```

next step: add a particular url to the urls.py in the project folder

```
from django.contrib import admin
from django.urls import path
from hello.views import myView ✅

urlpatterns = [
    path('admin/', admin.site.urls),
    path('hello/', myView), ✅
]

```

next step: run django server

```
python manage.py runserver
```

check the url for example, http://127.0.0.1:8000/hello/

.
.
.

exit from pipenv shell
