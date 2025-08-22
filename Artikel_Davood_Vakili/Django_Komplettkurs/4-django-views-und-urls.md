## 🇩🇪 Deutsch – `4-django-views-und-urls.md`


# Kapitel 4: Views und URLs in Django

In diesem Kapitel lernen wir, wie man Views definiert und über URLs im Browser zugänglich macht.

---

## 👁 Was ist ein View?

Ein View verarbeitet die Anfrage eines Nutzers und liefert eine Antwort zurück – z. B. HTML, JSON oder Text.

---

## 🛠 Einfachen View definieren

In `views.py` deiner App:

```python
from django.http import HttpResponse

def home(request):
    return HttpResponse("Hallo Davood! Dies ist die Startseite.")
```

---

## 🔗 View mit URL verbinden

In `urls.py` deiner App:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.home, name='home'),
]
```

In der Hauptdatei `urls.py` des Projekts:

```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('blog.urls')),  # Beispiel-App: blog
]
```

---

## 📄 Im Browser anzeigen

Server starten:

```bash
python manage.py runserver
```

Im Browser öffnen:

```
http://127.0.0.1:8000/
```

✅ View wird angezeigt.

---

## 📦 Klassenbasierte Views

Beispiel:

```python
from django.views import View
from django.http import HttpResponse

class AboutView(View):
    def get(self, request):
        return HttpResponse("Dies ist die Über-uns-Seite.")
```

In `urls.py`:

```python
from .views import AboutView

urlpatterns = [
    path('about/', AboutView.as_view(), name='about'),
]
```

---

## 📌 Fazit

Wir haben gelernt, wie man Views erstellt, sie mit URLs verknüpft und im Browser darstellt. Im nächsten Kapitel geht es um Templates und die Darstellung von HTML.


---
---


## 🇬🇧 English – `4-django-views-and-urls.md`


# Chapter 4: Views and URLs in Django

In this chapter, we’ll learn how to define views and connect them to URLs so they can be displayed in the browser.

---

## 👁 What Is a View?

A view handles user requests and returns a response—such as HTML, JSON, or plain text.

---

## 🛠 Defining a Simple View

In your app’s `views.py` file:

```python
from django.http import HttpResponse

def home(request):
    return HttpResponse("Hello Davood! This is the homepage.")
```

---

## 🔗 Connecting View to URL

In your app’s `urls.py` file:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.home, name='home'),
]
```

In the project’s main `urls.py` file:

```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('blog.urls')),  # Assuming your app is named blog
]
```

---

## 📄 Display in Browser

Run the server:

```bash
python manage.py runserver
```

Open your browser:

```
http://127.0.0.1:8000/
```

✅ The view message is displayed.

---

## 📦 Class-Based Views

Example:

```python
from django.views import View
from django.http import HttpResponse

class AboutView(View):
    def get(self, request):
        return HttpResponse("This is the About page.")
```

In `urls.py`:

```python
from .views import AboutView

urlpatterns = [
    path('about/', AboutView.as_view(), name='about'),
]
```

---

## 📌 Summary

We learned how to define views, connect them to URLs, and display them in the browser. In the next chapter, we’ll explore templates and rendering HTML pages.


---
---


## 🇮🇷 فارسی – `4-django-views-und-urls.md`


# فصل ۴: ویوها و مسیرها (URLs) در Django

در این فصل یاد می‌گیریم چگونه ویوها را تعریف کنیم و آن‌ها را از طریق URLها در مرورگر نمایش دهیم.

---

## 👁 ویو چیست؟

ویو (View) در Django مسئول پاسخ‌دهی به درخواست‌های کاربر است. ویوها می‌توانند داده‌ها را از مدل دریافت کرده و آن‌ها را در قالب HTML نمایش دهند.

---

## 🛠 تعریف یک ویو ساده

در فایل `views.py` اپلیکیشن خود:

```python
from django.http import HttpResponse

def home(request):
    return HttpResponse("سلام داوود! این صفحه اصلی است.")
```

---

## 🔗 اتصال ویو به URL

در فایل `urls.py` اپلیکیشن (اگر وجود ندارد، بساز):

```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.home, name='home'),
]
```

سپس در فایل `urls.py` اصلی پروژه:

```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('blog.urls')),  # فرض بر این است که اپلیکیشن blog نام دارد
]
```

---

## 📄 نمایش در مرورگر

اجرای سرور:

```bash
python manage.py runserver
```

باز کردن مرورگر:

```
http://127.0.0.1:8000/
```

✅ پیام ویو نمایش داده می‌شود.

---

## 📦 ویوهای مبتنی بر کلاس (Class-Based Views)

مثال:

```python
from django.views import View
from django.http import HttpResponse

class AboutView(View):
    def get(self, request):
        return HttpResponse("این صفحه درباره ما است.")
```

در `urls.py`:

```python
from .views import AboutView

urlpatterns = [
    path('about/', AboutView.as_view(), name='about'),
]
```

---

## 📌 جمع‌بندی

در این فصل یاد گرفتیم چگونه ویوها را تعریف کنیم، آن‌ها را به URLها متصل کنیم و در مرورگر نمایش دهیم. در فصل بعدی به سراغ قالب‌ها (Templates) و نمایش HTML می‌رویم.
