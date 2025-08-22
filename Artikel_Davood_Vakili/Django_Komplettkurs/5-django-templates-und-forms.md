## 🇩🇪 Deutsch – `5-django-templates-und-forms.md`


# Kapitel 5: Templates und Formulare in Django

In diesem Kapitel lernen wir, wie man HTML-Seiten mit Django-Templates rendert und Formulare zur Dateneingabe erstellt.

---

## 🧩 Was ist ein Template?

Templates sind HTML-Dateien, die mit Django-Tags und Variablen dynamische Inhalte anzeigen können.

---

## 🛠 Template-Ordner erstellen

Im App-Ordner:

```
blog/
├── templates/
│   └── home.html
```

Inhalt von `home.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Startseite</title>
</head>
<body>
    <h1>Hallo {{ name }}!</h1>
</body>
</html>
```

---

## 👁 View mit Template

In `views.py`:

```python
from django.shortcuts import render

def home(request):
    context = {'name': 'Davood'}
    return render(request, 'home.html', context)
```

---

## 📄 Einfaches Formular

In `forms.py`:

```python
from django import forms

class ContactForm(forms.Form):
    name = forms.CharField(max_length=100)
    email = forms.EmailField()
    message = forms.CharField(widget=forms.Textarea)
```

---

## 🧠 View für Formular

In `views.py`:

```python
from .forms import ContactForm

def contact(request):
    if request.method == 'POST':
        form = ContactForm(request.POST)
        if form.is_valid():
            # Daten verarbeiten
            return HttpResponse("Nachricht gesendet.")
    else:
        form = ContactForm()
    return render(request, 'contact.html', {'form': form})
```

---

## 🧾 Template für Formular

In `contact.html`:

```html
<form method="post">
    {% csrf_token %}
    {{ form.as_p }}
    <button type="submit">Senden</button>
</form>
```

---

## 📌 Fazit

Wir haben gelernt, wie man Templates erstellt, Daten darin anzeigt und Formulare zur Benutzereingabe verwendet. Im nächsten Kapitel geht es um Authentifizierung und Benutzerverwaltung.


---
---


## 🇬🇧 English – `5-django-templates-and-forms.md`


# Chapter 5: Templates and Forms in Django

In this chapter, we’ll learn how to render HTML pages using Django templates and create forms to collect user input.

---

## 🧩 What Is a Template?

Templates are HTML files that use Django tags and variables to display dynamic content.

---

## 🛠 Creating a Template Folder

Inside your app:

```
blog/
├── templates/
│   └── home.html
```

Content of `home.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Homepage</title>
</head>
<body>
    <h1>Hello {{ name }}!</h1>
</body>
</html>
```

---

## 👁 View with Template

In `views.py`:

```python
from django.shortcuts import render

def home(request):
    context = {'name': 'Davood'}
    return render(request, 'home.html', context)
```

---

## 📄 Simple Form

In `forms.py`:

```python
from django import forms

class ContactForm(forms.Form):
    name = forms.CharField(max_length=100)
    email = forms.EmailField()
    message = forms.CharField(widget=forms.Textarea)
```

---

## 🧠 View for Form

In `views.py`:

```python
from .forms import ContactForm

def contact(request):
    if request.method == 'POST':
        form = ContactForm(request.POST)
        if form.is_valid():
            # Process data
            return HttpResponse("Your message has been sent.")
    else:
        form = ContactForm()
    return render(request, 'contact.html', {'form': form})
```

---

## 🧾 Template for Form

In `contact.html`:

```html
<form method="post">
    {% csrf_token %}
    {{ form.as_p }}
    <button type="submit">Submit</button>
</form>
```

---

## 📌 Summary

We learned how to create templates, pass data to them, and build forms for user input. In the next chapter, we’ll explore authentication and user management.


---
---


## 🇮🇷 فارسی – `5-django-templates-und-forms.md`


# فصل ۵: قالب‌ها (Templates) و فرم‌ها در Django

در این فصل یاد می‌گیریم چگونه صفحات HTML را با قالب‌های Django نمایش دهیم و فرم‌هایی برای دریافت اطلاعات از کاربر بسازیم.

---

## 🧩 قالب چیست؟

قالب‌ها فایل‌های HTML هستند که با استفاده از تگ‌ها و متغیرهای Django می‌توانند داده‌های پویا را نمایش دهند.

---

## 🛠 ساخت پوشه قالب‌ها

در پوشه اپلیکیشن خود، یک پوشه به نام `templates` بسازید:

```
blog/
├── templates/
│   └── home.html
```

محتوای فایل `home.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>صفحه اصلی</title>
</head>
<body>
    <h1>سلام {{ name }}!</h1>
</body>
</html>
```

---

## 👁 ویو با قالب

در `views.py`:

```python
from django.shortcuts import render

def home(request):
    context = {'name': 'داوود'}
    return render(request, 'home.html', context)
```

---

## 📄 فرم ساده با Django

در `forms.py` اپلیکیشن خود:

```python
from django import forms

class ContactForm(forms.Form):
    name = forms.CharField(max_length=100)
    email = forms.EmailField()
    message = forms.CharField(widget=forms.Textarea)
```

---

## 🧠 ویو برای فرم

در `views.py`:

```python
from .forms import ContactForm

def contact(request):
    if request.method == 'POST':
        form = ContactForm(request.POST)
        if form.is_valid():
            # پردازش داده‌ها
            return HttpResponse("پیام شما ارسال شد.")
    else:
        form = ContactForm()
    return render(request, 'contact.html', {'form': form})
```

---

## 🧾 قالب فرم

در `contact.html`:

```html
<form method="post">
    {% csrf_token %}
    {{ form.as_p }}
    <button type="submit">ارسال</button>
</form>
```

---

## 📌 جمع‌بندی

در این فصل یاد گرفتیم چگونه قالب‌ها را بسازیم، داده‌ها را در آن‌ها نمایش دهیم و فرم‌هایی برای دریافت اطلاعات از کاربر ایجاد کنیم. در فصل بعدی به سراغ احراز هویت و مدیریت کاربران می‌رویم.
