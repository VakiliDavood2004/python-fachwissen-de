## 🇩🇪 Deutsch – `8-django-deployment.md`


# Kapitel 8: Deployment eines Django-Projekts

In diesem Kapitel lernen wir, wie man ein Django-Projekt von der Entwicklungsumgebung auf einen Produktionsserver überträgt.

---

## 🧰 Voraussetzungen

- Fertiges Django-Projekt
- Linux-Server (z. B. Ubuntu)
- SSH-Zugang
- Domain (optional)

---

## 🚀 Schritte zum Deployment

### 1. Python und Pakete installieren

```bash
sudo apt update
sudo apt install python3-pip python3-venv
```

### 2. Virtuelle Umgebung erstellen

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Pakete installieren

```bash
pip install django gunicorn
```

---

## 🔐 Sicherheitseinstellungen

In `settings.py`:

```python
DEBUG = False
ALLOWED_HOSTS = ['example.com', 'Server-IP']
```

---

## 🗃️ Statische Dateien sammeln

```bash
python manage.py collectstatic
```

---

## 🔥 Gunicorn starten

```bash
gunicorn projectname.wsgi:application --bind 0.0.0.0:8000
```

---

## 🌐 Nginx konfigurieren

Datei: `/etc/nginx/sites-available/projectname`

```nginx
server {
    listen 80;
    server_name example.com;

    location /static/ {
        alias /pfad/zu/staticfiles/;
    }

    location / {
        proxy_pass http://127.0.0.1:8000;
    }
}
```

---

## 🔁 Seite aktivieren

```bash
sudo ln -s /etc/nginx/sites-available/projectname /etc/nginx/sites-enabled/
sudo systemctl restart nginx
```

---

## 📌 Fazit

Wir haben gelernt, wie man ein Django-Projekt mit Gunicorn und Nginx auf einem Linux-Server bereitstellt. Im nächsten Kapitel geht es um Optimierung und Monitoring.


---
---


## 🇬🇧 English – `8-django-deployment.md`


# Chapter 8: Deploying a Django Project

In this chapter, we’ll learn how to deploy a Django project from development to a production server.

---

## 🧰 Prerequisites

- Completed Django project
- Linux server (e.g., Ubuntu)
- SSH access
- Domain name (optional)

---

## 🚀 Deployment Steps

### 1. Install Python and packages

```bash
sudo apt update
sudo apt install python3-pip python3-venv
```

### 2. Create virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install django gunicorn
```

---

## 🔐 Security Settings

In `settings.py`:

```python
DEBUG = False
ALLOWED_HOSTS = ['example.com', 'server-ip']
```

---

## 🗃️ Collect static files

```bash
python manage.py collectstatic
```

---

## 🔥 Run Gunicorn

```bash
gunicorn projectname.wsgi:application --bind 0.0.0.0:8000
```

---

## 🌐 Configure Nginx

File: `/etc/nginx/sites-available/projectname`

```nginx
server {
    listen 80;
    server_name example.com;

    location /static/ {
        alias /path/to/staticfiles/;
    }

    location / {
        proxy_pass http://127.0.0.1:8000;
    }
}
```

---

## 🔁 Enable site

```bash
sudo ln -s /etc/nginx/sites-available/projectname /etc/nginx/sites-enabled/
sudo systemctl restart nginx
```

---

## 📌 Summary

We learned how to deploy a Django project using Gunicorn and Nginx on a Linux server. In the next chapter, we’ll explore optimization and monitoring.


---
---


## 🇮🇷 فارسی – `8-django-deployment.md`


# فصل ۸: دیپلوی پروژه Django

در این فصل یاد می‌گیریم چگونه پروژه Django را از حالت توسعه به محیط واقعی (Production) منتقل کنیم.

---

## 🧰 پیش‌نیازها

- پروژه Django آماده
- سرور لینوکس (مثلاً Ubuntu)
- دسترسی SSH
- دامنه (اختیاری)

---

## 🚀 مراحل دیپلوی

### 1. نصب پایتون و پکیج‌ها روی سرور

```bash
sudo apt update
sudo apt install python3-pip python3-venv
```

### 2. ساخت محیط مجازی

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. نصب پکیج‌ها

```bash
pip install django gunicorn
```

---

## 🔐 تنظیمات امنیتی

در `settings.py`:

```python
DEBUG = False
ALLOWED_HOSTS = ['example.com', 'IP-Server']
```

---

## 🗃️ جمع‌آوری فایل‌های استاتیک

```bash
python manage.py collectstatic
```

---

## 🔥 اجرای Gunicorn

```bash
gunicorn projectname.wsgi:application --bind 0.0.0.0:8000
```

---

## 🌐 تنظیم Nginx

فایل کانفیگ در `/etc/nginx/sites-available/projectname`:

```nginx
server {
    listen 80;
    server_name example.com;

    location /static/ {
        alias /path/to/staticfiles/;
    }

    location / {
        proxy_pass http://127.0.0.1:8000;
    }
}
```

---

## 🔁 فعال‌سازی سایت

```bash
sudo ln -s /etc/nginx/sites-available/projectname /etc/nginx/sites-enabled/
sudo systemctl restart nginx
```

---

## 📌 جمع‌بندی

در این فصل یاد گرفتیم چگونه پروژه Django را روی سرور لینوکس با Gunicorn و Nginx دیپلوی کنیم. در فصل بعدی به سراغ بهینه‌سازی و مانیتورینگ پروژه می‌رویم.
