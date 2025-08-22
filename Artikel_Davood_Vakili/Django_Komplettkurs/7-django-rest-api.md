## 🇩🇪 Deutsch – `7-django-rest-api.md`


# Kapitel 7: Erstellung einer API mit Django REST Framework

In diesem Kapitel lernen wir, wie man mit dem Django REST Framework eine API erstellt, die Daten im JSON-Format bereitstellt.

---

## ⚙️ Installation von Django REST Framework

Im Terminal:

```
pip install djangorestframework
```

In `settings.py`:

```python
INSTALLED_APPS = [
    ...
    'rest_framework',
]
```

---

## 📦 Modell erstellen

In `models.py`:

```python
from django.db import models

class Post(models.Model):
    title = models.CharField(max_length=100)
    content = models.TextField()
```

---

## 🧪 Serializer erstellen

In `serializers.py`:

```python
from rest_framework import serializers
from .models import Post

class PostSerializer(serializers.ModelSerializer):
    class Meta:
        model = Post
        fields = '__all__'
```

---

## 🔁 API-View erstellen

In `views.py`:

```python
from rest_framework import viewsets
from .models import Post
from .serializers import PostSerializer

class PostViewSet(viewsets.ModelViewSet):
    queryset = Post.objects.all()
    serializer_class = PostSerializer
```

---

## 🚦 URL konfigurieren

In `urls.py`:

```python
from django.urls import path, include
from rest_framework.routers import DefaultRouter
from .views import PostViewSet

router = DefaultRouter()
router.register(r'posts', PostViewSet)

urlpatterns = [
    path('api/', include(router.urls)),
]
```

---

## 🧪 API testen

Besuche:

```
http://localhost:8000/api/posts/
```

Hier kannst du JSON-Daten anzeigen, hinzufügen, bearbeiten und löschen.

---

## 📌 Fazit

Wir haben gelernt, wie man mit Django REST Framework eine API erstellt. Im nächsten Kapitel geht es um Tests und Sicherheit.

---

## 🇬🇧 English – `7-django-rest-api.md`


# Chapter 7: Building an API with Django REST Framework

In this chapter, we’ll learn how to build an API using Django REST Framework to serve data in JSON format.

---

## ⚙️ Install Django REST Framework

In terminal:

```
pip install djangorestframework
```

In `settings.py`:

```python
INSTALLED_APPS = [
    ...
    'rest_framework',
]
```

---

## 📦 Create Model

In `models.py`:

```python
from django.db import models

class Post(models.Model):
    title = models.CharField(max_length=100)
    content = models.TextField()
```

---

## 🧪 Create Serializer

In `serializers.py`:

```python
from rest_framework import serializers
from .models import Post

class PostSerializer(serializers.ModelSerializer):
    class Meta:
        model = Post
        fields = '__all__'
```

---

## 🔁 Create API View

In `views.py`:

```python
from rest_framework import viewsets
from .models import Post
from .serializers import PostSerializer

class PostViewSet(viewsets.ModelViewSet):
    queryset = Post.objects.all()
    serializer_class = PostSerializer
```

---

## 🚦 Configure URLs

In `urls.py`:

```python
from django.urls import path, include
from rest_framework.routers import DefaultRouter
from .views import PostViewSet

router = DefaultRouter()
router.register(r'posts', PostViewSet)

urlpatterns = [
    path('api/', include(router.urls)),
]
```

---

## 🧪 Test the API

Visit:

```
http://localhost:8000/api/posts/
```

You can view, add, edit, and delete JSON data.

---

## 📌 Summary

We learned how to build an API using Django REST Framework. In the next chapter, we’ll explore testing and securing the API.


---
---


## 🇮🇷 فارسی – `7-django-rest-api.md`


# فصل ۷: ساخت API با Django REST Framework

در این فصل یاد می‌گیریم چگونه با استفاده از Django REST Framework یک API بسازیم تا داده‌ها را به‌صورت JSON ارائه کنیم.

---

## ⚙️ نصب Django REST Framework

در ترمینال:

```
pip install djangorestframework
```

در `settings.py`:

```python
INSTALLED_APPS = [
    ...
    'rest_framework',
]
```

---

## 📦 ساخت مدل

در `models.py`:

```python
from django.db import models

class Post(models.Model):
    title = models.CharField(max_length=100)
    content = models.TextField()
```

---

## 🧪 ساخت Serializer

در `serializers.py`:

```python
from rest_framework import serializers
from .models import Post

class PostSerializer(serializers.ModelSerializer):
    class Meta:
        model = Post
        fields = '__all__'
```

---

## 🔁 ساخت View API

در `views.py`:

```python
from rest_framework import viewsets
from .models import Post
from .serializers import PostSerializer

class PostViewSet(viewsets.ModelViewSet):
    queryset = Post.objects.all()
    serializer_class = PostSerializer
```

---

## 🚦 تنظیم URL

در `urls.py`:

```python
from django.urls import path, include
from rest_framework.routers import DefaultRouter
from .views import PostViewSet

router = DefaultRouter()
router.register(r'posts', PostViewSet)

urlpatterns = [
    path('api/', include(router.urls)),
]
```

---

## 🧪 تست API

اکنون می‌توانید به آدرس زیر بروید:

```
http://localhost:8000/api/posts/
```

و داده‌ها را به‌صورت JSON مشاهده، اضافه، ویرایش و حذف کنید.

---

## 📌 جمع‌بندی

در این فصل یاد گرفتیم چگونه با Django REST Framework یک API بسازیم. در فصل بعدی به سراغ تست‌نویسی و امنیت API می‌رویم.
