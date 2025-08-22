## 🇩🇪 Deutsch – `3-django-modelle-und-datenbank.md`


# Kapitel 3: Modelle und Datenbank in Django

In diesem Kapitel lernen wir, wie man Modelle in Django definiert und mit der Datenbank verbindet.

---

## 🧠 Was ist ein Modell?

Ein Modell repräsentiert die Datenstruktur einer Anwendung. Jedes Modell wird zu einer Tabelle in der Datenbank, und die Felder entsprechen den Spalten.

---

## 🛠 Einfaches Modell definieren

In der Datei `models.py` deiner App:

```python
from django.db import models

class Article(models.Model):
    title = models.CharField(max_length=200)
    content = models.TextField()
    published = models.BooleanField(default=False)
    created_at = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return self.title
```

---

## 📦 Häufige Feldtypen

| Feldtyp           | Beschreibung                        |
|-------------------|--------------------------------------|
| `CharField`       | Zeichenkette mit begrenzter Länge    |
| `TextField`       | Langer Text                          |
| `IntegerField`    | Ganze Zahl                           |
| `BooleanField`    | Wahr/Falsch                          |
| `DateTimeField`   | Datum und Uhrzeit                    |
| `EmailField`      | Gültige E-Mail-Adresse               |
| `ForeignKey`      | Beziehung zu anderem Modell          |

---

## 🔄 Migrationen durchführen

Nach dem Definieren der Modelle:

```bash
python manage.py makemigrations
python manage.py migrate
```

---

## 🛡 Modell im Admin registrieren

In der Datei `admin.py`:

```python
from django.contrib import admin
from .models import Article

admin.site.register(Article)
```

---

## 🧪 Modell im Admin testen

1. Server starten:

```bash
python manage.py runserver
```

2. Superuser erstellen:

```bash
python manage.py createsuperuser
```

3. Admin-Bereich öffnen:

```
http://127.0.0.1:8000/admin/
```

Modell verwalten ✅

---

## 📌 Fazit

Wir haben gelernt, wie man Modelle definiert, sie in die Datenbank migriert und im Admin-Bereich registriert. Im nächsten Kapitel geht es um Views und die Darstellung von Daten auf Webseiten.


---
---


## 🇬🇧 English – `3-django-models-and-database.md`


# Chapter 3: Models and Database in Django

In this chapter, we’ll learn how to define models in Django and connect them to the database.

---

## 🧠 What Is a Model?

A model represents the data structure of your application. Each model becomes a table in the database, and its fields become columns.

---

## 🛠 Defining a Simple Model

In your app’s `models.py` file:

```python
from django.db import models

class Article(models.Model):
    title = models.CharField(max_length=200)
    content = models.TextField()
    published = models.BooleanField(default=False)
    created_at = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return self.title
```

---

## 📦 Common Field Types

| Field Type        | Description                          |
|-------------------|--------------------------------------|
| `CharField`       | Short text string                    |
| `TextField`       | Long text                            |
| `IntegerField`    | Whole number                         |
| `BooleanField`    | True/False value                     |
| `DateTimeField`   | Date and time                        |
| `EmailField`      | Valid email address                  |
| `ForeignKey`      | Relationship to another model        |

---

## 🔄 Database Migration

After defining models, apply migrations:

```bash
python manage.py makemigrations
python manage.py migrate
```

---

## 🛡 Register Model in Admin Panel

Edit `admin.py`:

```python
from django.contrib import admin
from .models import Article

admin.site.register(Article)
```

---

## 🧪 Test Model in Admin Panel

1. Run the server:

```bash
python manage.py runserver
```

2. Create a superuser:

```bash
python manage.py createsuperuser
```

3. Access the admin panel:

```
http://127.0.0.1:8000/admin/
```

Manage your models ✅

---

## 📌 Summary

We learned how to define models, migrate them to the database, and register them in the admin panel. In the next chapter, we’ll explore views and how to display data on web pages.


---
---


## 🇮🇷 فارسی – `3-django-modelle-und-datenbank.md`


# فصل ۳: مدل‌ها و پایگاه داده در Django

در این فصل با مفهوم مدل‌ها در Django آشنا می‌شویم و نحوه اتصال آن‌ها به پایگاه داده را بررسی می‌کنیم.

---

## 🧠 مدل چیست؟

مدل‌ها در Django نمایانگر ساختار داده‌ها هستند. هر مدل به یک جدول در پایگاه داده تبدیل می‌شود و شامل فیلدهایی است که ستون‌های جدول را تشکیل می‌دهند.

---

## 🛠 تعریف یک مدل ساده

در فایل `models.py` اپلیکیشن خود، یک مدل تعریف می‌کنیم:

```python
from django.db import models

class Article(models.Model):
    title = models.CharField(max_length=200)
    content = models.TextField()
    published = models.BooleanField(default=False)
    created_at = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return self.title
```

---

## 📦 انواع فیلدهای رایج

| نوع فیلد         | توضیح                              |
|------------------|-------------------------------------|
| `CharField`      | رشته با طول محدود                  |
| `TextField`      | متن طولانی                         |
| `IntegerField`   | عدد صحیح                            |
| `BooleanField`   | مقدار درست یا غلط (True/False)     |
| `DateTimeField`  | تاریخ و زمان                        |
| `EmailField`     | ایمیل معتبر                         |
| `ForeignKey`     | ارتباط با مدل دیگر (کلید خارجی)    |

---

## 🔄 مهاجرت پایگاه داده

پس از تعریف مدل‌ها، باید آن‌ها را به پایگاه داده منتقل کنیم:

```bash
python manage.py makemigrations
python manage.py migrate
```

---

## 🛡 ثبت مدل در پنل مدیریت

برای نمایش مدل در پنل مدیریت Django، فایل `admin.py` را ویرایش می‌کنیم:

```python
from django.contrib import admin
from .models import Article

admin.site.register(Article)
```

---

## 🧪 تست مدل در پنل مدیریت

۱. اجرای سرور:

```bash
python manage.py runserver
```

۲. ساخت ادمین:

```bash
python manage.py createsuperuser
```

۳. ورود به پنل مدیریت:

```
http://127.0.0.1:8000/admin/
```

مدل‌ها را مشاهده و مدیریت کنید ✅

---

## 📌 جمع‌بندی

در این فصل یاد گرفتیم چگونه مدل‌ها را تعریف کنیم، آن‌ها را به پایگاه داده منتقل کنیم و در پنل مدیریت ثبت کنیم. در فصل بعدی به سراغ ویوها و نمایش داده‌ها در صفحات وب می‌رویم.

