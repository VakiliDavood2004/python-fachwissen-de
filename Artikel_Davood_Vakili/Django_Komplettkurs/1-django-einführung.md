## 🇩🇪 Deutsch – `1-django-einführung.md`

# Kapitel 1: Einführung in Django

## 🎯 Was ist Django?

Django ist ein leistungsstarkes, hochentwickeltes Web-Framework für die Programmiersprache Python. Es hilft Entwicklern, Webanwendungen schneller, sicherer und strukturierter zu erstellen.

## ✅ Vorteile von Django

- **Hohe Entwicklungsgeschwindigkeit**: Mit integrierten Tools wie Admin-Panel und ORM.
- **Hohe Sicherheit**: Schutz vor SQL-Injection, XSS und CSRF.
- **Skalierbarkeit**: Geeignet für kleine bis große Projekte.
- **Aktive Community**: Umfangreiche Dokumentation und Support.

## 🛠 Einsatzbereiche

- Nachrichtenportale, Online-Shops, Lernplattformen
- Entwicklung von REST-APIs für mobile Apps
- Content-Management-Systeme (CMS)
- Datengetriebene Dashboards und Analyse-Tools

---

## ⚙️ Installation und Erste Schritte

### 1. Python installieren

Überprüfen Sie, ob Python installiert ist:

```bash
python --version
```

Falls nicht, laden Sie es von [python.org](https://www.python.org/) herunter.

### 2. Virtuelle Umgebung erstellen (empfohlen)

```bash
python -m venv env
source env/bin/activate  # Linux/Mac
env\Scripts\activate     # Windows
```

### 3. Django installieren

```bash
pip install django
```

### 4. Installation überprüfen

```bash
django-admin --version
```

---

## 🚀 Erstes Django-Projekt erstellen

```bash
django-admin startproject myproject
cd myproject
python manage.py runserver
```

Im Browser öffnen:

```
http://127.0.0.1:8000/
```

Wenn die Willkommensseite erscheint, war die Einrichtung erfolgreich ✅

---

## 📁 Projektstruktur

```
myproject/
├── manage.py
├── myproject/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
```

### Datei-Erklärungen:
- `manage.py`: Projektverwaltung
- `settings.py`: Projekteinstellungen
- `urls.py`: URL-Routing
- `wsgi.py` / `asgi.py`: Server-Schnittstellen

---

## 📌 Fazit

In diesem Kapitel haben wir Django kennengelernt, seine Vorteile und Einsatzbereiche betrachtet sowie die Installation und das erste Projekt durchgeführt. Im nächsten Kapitel geht es um die Projektstruktur und das Erstellen von Apps.


---
---


## 🇬🇧 English – `1-django-introduction.md`

# Chapter 1: Introduction to Django

## 🎯 What is Django?

Django is a powerful, high-level web framework for Python. It helps developers build web applications faster, more securely, and with better structure.

## ✅ Advantages of Django

- **Rapid development**: Built-in tools like admin panel and ORM
- **High security**: Protection against SQL injection, XSS, CSRF
- **Scalability**: Suitable for small to large projects
- **Active community**: Rich documentation and support

## 🛠 Use Cases

- News websites, e-commerce platforms, educational portals
- REST API development for mobile apps
- Content Management Systems (CMS)
- Data-driven dashboards and analytics tools

---

## ⚙️ Installation and Getting Started

### 1. Install Python

Check if Python is installed:

```bash
python --version
```

If not, download it from [python.org](https://www.python.org/).

### 2. Create a virtual environment (recommended)

```bash
python -m venv env
source env/bin/activate  # Linux/Mac
env\Scripts\activate     # Windows
```

### 3. Install Django

```bash
pip install django
```

### 4. Verify installation

```bash
django-admin --version
```

---

## 🚀 Create Your First Django Project

```bash
django-admin startproject myproject
cd myproject
python manage.py runserver
```

Open your browser:

```
http://127.0.0.1:8000/
```

If you see the Django welcome page, setup was successful ✅

---

## 📁 Project Structure

```
myproject/
├── manage.py
├── myproject/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
```

### File Descriptions:
- `manage.py`: Project management tool
- `settings.py`: Project configuration
- `urls.py`: URL routing
- `wsgi.py` / `asgi.py`: Server interfaces

---

## 📌 Summary

In this chapter, we introduced Django, explored its benefits and use cases, and walked through installation and project setup. In the next chapter, we’ll dive into project structure and app creation.


---
---


# فصل اول: معرفی جنگو (Django)

## 🎯 جنگو چیست؟

جنگو یک فریم‌ورک قدرتمند و سطح بالا برای توسعه وب با زبان پایتون است. این فریم‌ورک به توسعه‌دهندگان کمک می‌کند تا سریع‌تر، امن‌تر و با ساختاری منظم‌تر وب‌سایت‌ها و اپلیکیشن‌های تحت وب بسازند.

## ✅ مزایای جنگو

- **سرعت توسعه بالا**: با ابزارهای آماده مثل پنل مدیریت و ORM، زمان توسعه کاهش می‌یابد.
- **امنیت بالا**: جنگو به‌صورت پیش‌فرض در برابر حملاتی مثل SQL Injection، XSS و CSRF محافظت می‌کند.
- **مقیاس‌پذیری**: مناسب برای پروژه‌های کوچک تا بزرگ، از وبلاگ شخصی تا شبکه‌های اجتماعی.
- **جامعه فعال**: مستندات کامل و انجمن‌های پشتیبانی قوی.

## 🛠 کاربردهای جنگو

- ساخت وب‌سایت‌های خبری، فروشگاهی، آموزشی
- توسعه REST API برای اپلیکیشن‌های موبایل
- ساخت پنل‌های مدیریت محتوا (CMS)
- پروژه‌های داده‌محور و داشبوردهای تحلیلی

---

## ⚙️ نصب و راه‌اندازی اولیه

### 1. نصب پایتون

ابتدا مطمئن شوید که پایتون روی سیستم شما نصب شده است. برای بررسی:

```bash
python --version
```

اگر نصب نیست، از [python.org](https://www.python.org/) دانلود و نصب کنید.

### 2. ساخت محیط مجازی (اختیاری ولی توصیه‌شده)

```bash
python -m venv env
source env/bin/activate  # در لینوکس یا مک
env\Scripts\activate     # در ویندوز
```

### 3. نصب جنگو

```bash
pip install django
```

### 4. بررسی نصب

```bash
django-admin --version
```

اگر نسخه‌ای نمایش داده شد، نصب موفق بوده است.

---

## 🚀 ساخت اولین پروژه جنگو

برای ساخت پروژه جدید:

```bash
django-admin startproject myproject
cd myproject
python manage.py runserver
```

سپس مرورگر را باز کرده و وارد آدرس زیر شوید:

```
http://127.0.0.1:8000/
```

اگر صفحه خوش‌آمدگویی جنگو را دیدید، یعنی پروژه با موفقیت اجرا شده است ✅

---

## 📁 ساختار اولیه پروژه

پس از ساخت پروژه، ساختار پوشه‌ها به شکل زیر خواهد بود:

```
myproject/
├── manage.py
├── myproject/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
```

### توضیح فایل‌ها:
- `manage.py`: ابزار مدیریت پروژه
- `settings.py`: تنظیمات کلی پروژه
- `urls.py`: مسیرهای URL پروژه
- `wsgi.py` و `asgi.py`: برای اجرای پروژه در سرورهای مختلف

---

## 📌 نتیجه‌گیری

در این فصل با مفاهیم پایه جنگو، مزایا، کاربردها و نحوه نصب و اجرای اولیه آشنا شدیم. در فصل بعدی، به ساخت اپلیکیشن و بررسی ساختار پروژه می‌پردازیم.

