## 🇩🇪 Deutsch – `6-django-auth-und-benutzerverwaltung.md`


# Kapitel 6: Authentifizierung und Benutzerverwaltung in Django

In diesem Kapitel lernen wir, wie man Benutzer registriert, anmeldet, abmeldet und den Zugriff auf Seiten schützt.

---

## 🔐 Django Auth-System

Django bietet ein integriertes Authentifizierungssystem mit:

- Benutzer-Modell
- Login- und Registrierungsformulare
- Sitzungsverwaltung
- Berechtigungen und Gruppen

---

## 🧑‍💻 Benutzerregistrierung

In `forms.py`:

```python
from django.contrib.auth.forms import UserCreationForm
from django.contrib.auth.models import User

class RegisterForm(UserCreationForm):
    class Meta:
        model = User
        fields = ['username', 'email', 'password1', 'password2']
```

In `views.py`:

```python
from .forms import RegisterForm
from django.shortcuts import render, redirect

def register(request):
    if request.method == 'POST':
        form = RegisterForm(request.POST)
        if form.is_valid():
            form.save()
            return redirect('login')
    else:
        form = RegisterForm()
    return render(request, 'register.html', {'form': form})
```

---

## 🔑 Benutzer-Login

```python
from django.contrib.auth import authenticate, login

def user_login(request):
    if request.method == 'POST':
        username = request.POST['username']
        password = request.POST['password']
        user = authenticate(request, username=username, password=password)
        if user:
            login(request, user)
            return redirect('home')
    return render(request, 'login.html')
```

---

## 🚪 Benutzer-Logout

```python
from django.contrib.auth import logout

def user_logout(request):
    logout(request)
    return redirect('login')
```

---

## 🛡️ Seiten schützen

```python
from django.contrib.auth.decorators import login_required

@login_required
def dashboard(request):
    return render(request, 'dashboard.html')
```

---

## 📌 Fazit

Wir haben gelernt, wie man Benutzer registriert, anmeldet, abmeldet und Seiten schützt. Im nächsten Kapitel geht es um Modelle und das Admin-Panel.


---
---


## 🇬🇧 English – `6-django-auth-and-user-management.md`


# Chapter 6: Authentication and User Management in Django

In this chapter, we’ll learn how to register users, log them in and out, and protect views using authentication.

---

## 🔐 Django’s Built-in Auth System

Django provides a powerful authentication system including:

- User model
- Login and registration forms
- Session management
- Permissions and groups

---

## 🧑‍💻 User Registration

In `forms.py`:

```python
from django.contrib.auth.forms import UserCreationForm
from django.contrib.auth.models import User

class RegisterForm(UserCreationForm):
    class Meta:
        model = User
        fields = ['username', 'email', 'password1', 'password2']
```

In `views.py`:

```python
from .forms import RegisterForm
from django.shortcuts import render, redirect

def register(request):
    if request.method == 'POST':
        form = RegisterForm(request.POST)
        if form.is_valid():
            form.save()
            return redirect('login')
    else:
        form = RegisterForm()
    return render(request, 'register.html', {'form': form})
```

---

## 🔑 User Login

```python
from django.contrib.auth import authenticate, login

def user_login(request):
    if request.method == 'POST':
        username = request.POST['username']
        password = request.POST['password']
        user = authenticate(request, username=username, password=password)
        if user:
            login(request, user)
            return redirect('home')
    return render(request, 'login.html')
```

---

## 🚪 User Logout

```python
from django.contrib.auth import logout

def user_logout(request):
    logout(request)
    return redirect('login')
```

---

## 🛡️ Protecting Views

```python
from django.contrib.auth.decorators import login_required

@login_required
def dashboard(request):
    return render(request, 'dashboard.html')
```

---

## 📌 Summary

We learned how to register users, log them in and out, and protect views using authentication. In the next chapter, we’ll explore models and the Django admin panel.


---
---


## 🇮🇷 فارسی – `6-django-auth-und-benutzerverwaltung.md`


# فصل ۶: احراز هویت و مدیریت کاربران در Django

در این فصل یاد می‌گیریم چگونه کاربران را ثبت‌نام کنیم، وارد سیستم کنیم، خارج کنیم و دسترسی آن‌ها را مدیریت کنیم.

---

## 🔐 سیستم احراز هویت Django

جنگو به‌صورت پیش‌فرض یک سیستم احراز هویت قدرتمند دارد که شامل:

- مدل کاربر
- فرم‌های ورود و ثبت‌نام
- مدیریت نشست‌ها (Sessions)
- مجوزها و گروه‌ها

---

## 🧑‍💻 ثبت‌نام کاربر

در `forms.py`:

```python
from django.contrib.auth.forms import UserCreationForm
from django.contrib.auth.models import User

class RegisterForm(UserCreationForm):
    class Meta:
        model = User
        fields = ['username', 'email', 'password1', 'password2']
```

در `views.py`:

```python
from .forms import RegisterForm
from django.shortcuts import render, redirect

def register(request):
    if request.method == 'POST':
        form = RegisterForm(request.POST)
        if form.is_valid():
            form.save()
            return redirect('login')
    else:
        form = RegisterForm()
    return render(request, 'register.html', {'form': form})
```

---

## 🔑 ورود کاربر

در `views.py`:

```python
from django.contrib.auth import authenticate, login

def user_login(request):
    if request.method == 'POST':
        username = request.POST['username']
        password = request.POST['password']
        user = authenticate(request, username=username, password=password)
        if user:
            login(request, user)
            return redirect('home')
    return render(request, 'login.html')
```

---

## 🚪 خروج کاربر

```python
from django.contrib.auth import logout

def user_logout(request):
    logout(request)
    return redirect('login')
```

---

## 🛡️ محافظت از صفحات

در `views.py`:

```python
from django.contrib.auth.decorators import login_required

@login_required
def dashboard(request):
    return render(request, 'dashboard.html')
```

---

## 📌 جمع‌بندی

در این فصل یاد گرفتیم چگونه کاربران را ثبت‌نام کنیم، وارد و خارج کنیم و صفحات را با احراز هویت محافظت کنیم. در فصل بعدی به سراغ مدیریت مدل‌ها و پنل ادمین می‌رویم.
