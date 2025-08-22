## 🇩🇪 Deutsch – `2-django-projektstruktur.md`


# Kapitel 2: Projektstruktur in Django

In diesem Kapitel lernen wir die grundlegende Struktur eines Django-Projekts kennen und verstehen die Funktion der wichtigsten Dateien und Ordner.

---

## 📁 Projektstruktur nach Erstellung

Nach dem Befehl `django-admin startproject myproject` sieht die Struktur wie folgt aus:

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

---

## 📝 Erklärung der Dateien

### 🔹 `manage.py`

- Kommandozeilen-Tool zur Verwaltung des Projekts
- Ausführen von Befehlen wie `runserver`, `migrate`, `createsuperuser`

### 🔹 Innerer Ordner `myproject/`

Dieser Ordner enthält die Hauptkonfiguration des Projekts.

#### `__init__.py`

- Leere Datei, die den Ordner als Python-Paket kennzeichnet

#### `settings.py`

- Globale Einstellungen des Projekts:
  - Datenbankkonfiguration
  - Installierte Apps
  - Pfade für statische und Medien-Dateien
  - Sprache und Zeitzone

#### `urls.py`

- Definition der URL-Routen
- Verknüpfung von URLs mit Views oder Apps

#### `wsgi.py`

- Schnittstelle für WSGI-Server (z. B. Gunicorn)
- Wird in produktiven Umgebungen verwendet

#### `asgi.py`

- Schnittstelle für ASGI-Server (für WebSockets und Async)
- Geeignet für Echtzeit-Anwendungen

---

## 📦 Django-Apps

Ein Django-Projekt kann mehrere Apps enthalten. Eine neue App wird so erstellt:

```bash
python manage.py startapp blog
```

Struktur der App:

```
blog/
├── admin.py
├── apps.py
├── models.py
├── tests.py
├── views.py
├── migrations/
│   └── __init__.py
├── __init__.py
```

---

## 🧩 Erklärung der App-Dateien

### `models.py`

- Definition der Datenbankmodelle

### `views.py`

- Logik zur Verarbeitung von HTTP-Anfragen

### `admin.py`

- Registrierung von Modellen im Django-Admin

### `apps.py`

- App-Konfiguration

### `tests.py`

- Unit-Tests für die App

### `migrations/`

- Datenbankmigrationen basierend auf Modelländerungen

---

## 🔗 App im Projekt registrieren

Die App muss in `settings.py` unter `INSTALLED_APPS` hinzugefügt werden:

```python
INSTALLED_APPS = [
    ...
    'blog',
]
```

---

## 📌 Fazit

In diesem Kapitel haben wir die Projektstruktur von Django kennengelernt, die wichtigsten Dateien erklärt und eine App erstellt und eingebunden. Im nächsten Kapitel geht es um Datenbankmodelle.


---
---


## 🇬🇧 English – `2-django-project-structure.md`


# Chapter 2: Django Project Structure

In this chapter, we’ll explore the basic structure of a Django project and understand the role of each file and folder.

---

## 📁 Project Structure After Creation

After running `django-admin startproject myproject`, the structure looks like this:

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

---

## 📝 File Descriptions

### 🔹 `manage.py`

- Command-line utility for managing the project
- Used for commands like `runserver`, `migrate`, `createsuperuser`

### 🔹 Inner `myproject/` Folder

Contains the main configuration for the project.

#### `__init__.py`

- Empty file that marks the folder as a Python package

#### `settings.py`

- Global project settings:
  - Database configuration
  - Installed apps
  - Static and media file paths
  - Language and timezone

#### `urls.py`

- Defines URL routes
- Connects URLs to views or apps

#### `wsgi.py`

- Interface for WSGI servers (e.g., Gunicorn)
- Used in production environments

#### `asgi.py`

- Interface for ASGI servers (supports WebSockets and async)
- Ideal for real-time applications

---

## 📦 Django Apps

A Django project can contain multiple apps. To create a new app:

```bash
python manage.py startapp blog
```

App structure:

```
blog/
├── admin.py
├── apps.py
├── models.py
├── tests.py
├── views.py
├── migrations/
│   └── __init__.py
├── __init__.py
```

---

## 🧩 App File Descriptions

### `models.py`

- Defines database models

### `views.py`

- Contains logic for handling HTTP requests

### `admin.py`

- Registers models with Django’s admin interface

### `apps.py`

- App configuration

### `tests.py`

- Unit tests for the app

### `migrations/`

- Stores database migrations based on model changes

---

## 🔗 Registering the App in the Project

To activate the app, add it to `INSTALLED_APPS` in `settings.py`:

```python
INSTALLED_APPS = [
    ...
    'blog',
]
```

---

## 📌 Summary

In this chapter, we explored Django’s project structure, explained the key files, and created and registered a new app. In the next chapter, we’ll dive into database models.


---
---


## 🇮🇷 فارسی – `2-django-projektstruktur.md`


# فصل ۲: ساختار پروژه در Django

در این فصل با ساختار اولیه یک پروژه Django آشنا می‌شویم و نقش هر فایل و پوشه را بررسی می‌کنیم.

---

## 📁 ساختار پروژه پس از ایجاد

پس از اجرای دستور `django-admin startproject myproject`، ساختار زیر ایجاد می‌شود:

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

---

## 📝 توضیح فایل‌ها و پوشه‌ها

### 🔹 `manage.py`

- ابزار خط فرمان برای مدیریت پروژه
- اجرای دستورات مانند `runserver`, `migrate`, `createsuperuser`

### 🔹 پوشه داخلی `myproject/`

این پوشه شامل تنظیمات اصلی پروژه است.

#### `__init__.py`

- فایل خالی برای شناسایی پوشه به عنوان یک پکیج پایتون

#### `settings.py`

- تنظیمات کلی پروژه مانند:
  - پایگاه داده
  - اپلیکیشن‌های نصب‌شده
  - مسیرهای استاتیک و مدیا
  - زبان و منطقه زمانی

#### `urls.py`

- تعریف مسیرهای URL پروژه
- اتصال URLها به ویوها یا اپلیکیشن‌ها

#### `wsgi.py`

- رابط بین Django و سرورهای WSGI (مثل Gunicorn)
- برای اجرای پروژه در محیط production

#### `asgi.py`

- رابط برای سرورهای ASGI (برای پشتیبانی از WebSocket و async)
- مناسب برای پروژه‌های real-time

---

## 📦 اپلیکیشن‌ها در Django

در Django، پروژه می‌تواند شامل چندین اپلیکیشن باشد. برای ایجاد یک اپلیکیشن جدید:

```bash
python manage.py startapp blog
```

ساختار اپلیکیشن:

```
blog/
├── admin.py
├── apps.py
├── models.py
├── tests.py
├── views.py
├── migrations/
│   └── __init__.py
├── __init__.py
```

---

## 🧩 توضیح فایل‌های اپلیکیشن

### `models.py`

- تعریف مدل‌های پایگاه داده

### `views.py`

- تعریف ویوها (منطق پاسخ‌دهی به درخواست‌ها)

### `admin.py`

- ثبت مدل‌ها در پنل مدیریت Django

### `apps.py`

- تنظیمات اپلیکیشن

### `tests.py`

- نوشتن تست‌های واحد برای اپلیکیشن

### `migrations/`

- نگهداری تغییرات مدل‌ها برای پایگاه داده

---

## 🔗 اتصال اپلیکیشن به پروژه

برای فعال‌سازی اپلیکیشن، باید آن را در `settings.py` اضافه کنیم:

```python
INSTALLED_APPS = [
    ...
    'blog',
]
```

---

## 📌 جمع‌بندی

در این فصل با ساختار پروژه Django آشنا شدیم، نقش فایل‌های اصلی را بررسی کردیم و نحوه ایجاد و اتصال اپلیکیشن‌ها را یاد گرفتیم. در فصل بعدی، به سراغ مدل‌ها و پایگاه داده می‌رویم.
