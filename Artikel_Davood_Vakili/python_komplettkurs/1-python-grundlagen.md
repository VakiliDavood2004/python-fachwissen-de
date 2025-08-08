# 🇩🇪 Grundlagen und Einführung in Python

Willkommen zum ersten Teil der Python-Lernreihe! In dieser Datei lernst du die grundlegenden Konzepte der Programmiersprache Python kennen. Ziel dieses Abschnitts ist es, ein solides Verständnis für die Struktur und Logik von Python zu entwickeln, damit du die nächsten Schritte mit Selbstvertrauen gehen kannst.

---

## 📚 Inhaltsverzeichnis

- Einführung in Python
- Installation und Einrichtung
- Syntax und Einrückung
- Variablen und Datentypen
- Operatoren
- Eingabe und Ausgabe
- Bedingte Anweisungen
- Schleifen
- Schreibstil und Best Practices
- Praktische Übungen
- Empfohlene Ressourcen
- Fazit

---

## 🧭 Einführung in Python

Python ist eine interpretierte, hochentwickelte und vielseitige Programmiersprache, die 1991 von Guido van Rossum entwickelt wurde. Aufgrund ihrer Einfachheit, Lesbarkeit und der großen Entwicklergemeinschaft gehört Python zu den beliebtesten Programmiersprachen weltweit.

### Wichtige Eigenschaften von Python:

- Einfache und verständliche Syntax
- Geeignet für Anfänger und Profis
- Unterstützt objektorientierte, funktionale und prozedurale Programmierung
- Plattformübergreifend (Windows, Linux, macOS)
- Einsatz in vielen Bereichen: Webentwicklung, Data Science, KI, Automatisierung u.v.m.

---

## 🛠️ Installation und Einrichtung

### Installation unter Windows

1. Besuche [python.org](https://www.python.org).
2. Lade die neueste Version von Python herunter.
3. Aktiviere beim Installieren die Option „Add Python to PATH“.
4. Öffne danach die Eingabeaufforderung (CMD) und gib folgenden Befehl ein:

```bash
python --version
```

Wenn die Version angezeigt wird, war die Installation erfolgreich.

### Installation unter Linux / macOS

```bash
sudo apt update
sudo apt install python3  # für Linux

brew install python3      # für macOS
```

---

## ✍️ Syntax und Einrückung

In Python ist die Einrückung entscheidend. Im Gegensatz zu Sprachen wie C oder Java, die Klammern `{}` verwenden, definiert Python Codeblöcke durch Leerzeichen oder Tabs.

### Beispiel:

```python
x = 10
if x > 5:
    print("Die Zahl ist größer als 5")
```

Die zweite Zeile muss eingerückt sein – üblich sind 4 Leerzeichen.

❗ Hinweis: Falsche Einrückung führt zu einem SyntaxError.

---

## 📦 Variablen und Datentypen

### Variablen definieren

In Python muss der Datentyp nicht explizit angegeben werden – er wird automatisch erkannt.

```python
name = "Davood"
alter = 30
note = 18.5
aktiv = True
```

### Regeln für Variablennamen

- Nur Buchstaben, Zahlen und Unterstriche (`_`) verwenden.
- Der Name darf nicht mit einer Zahl beginnen.
- Keine reservierten Wörter wie `print`, `if`, `for` verwenden.

### Grundlegende Datentypen

| Datentyp | Beispiel             | Beschreibung         |
|----------|----------------------|-----------------------|
| `int`    | `42`                 | Ganze Zahl            |
| `float`  | `3.14`               | Dezimalzahl           |
| `str`    | `"Hallo"`            | Zeichenkette (String) |
| `bool`   | `True`, `False`      | Wahrheitswert         |
| `list`   | `[1, 2, 3]`          | Liste von Werten      |
| `dict`   | `{"name": "Davood"}` | Schlüssel-Wert-Paare  |

---

## ➕ Operatoren

### Mathematische Operatoren

| Operator | Bedeutung     | Beispiel   |
|----------|---------------|------------|
| `+`      | Addition      | `5 + 3`    |
| `-`      | Subtraktion   | `10 - 2`   |
| `*`      | Multiplikation| `4 * 2`    |
| `/`      | Division      | `8 / 2`    |
| `%`      | Modulo        | `7 % 3`    |
| `**`     | Potenz        | `2 ** 3`   |

### Vergleichsoperatoren

```python
x = 5
y = 10

print(x == y)  # False
print(x < y)   # True
```

### Logische Operatoren

```python
a = True
b = False

print(a and b)  # False
print(a or b)   # True
print(not a)    # False
```

---

## 📥 Eingabe und 📤 Ausgabe

### Eingabe vom Benutzer

```python
name = input("Gib deinen Namen ein: ")
```

Die Eingabe ist immer ein String. Um sie in eine Zahl umzuwandeln:

```python
alter = int(input("Gib dein Alter ein: "))
```

### Ausgabe mit `print`

```python
print("Hallo", name)
```

Mehrere Werte können mit Kommas getrennt oder formatiert werden:

```python
print(f"Hallo {name}, willkommen!")
```

---

## 🔀 Bedingte Anweisungen

Bedingungen dienen zur Entscheidungsfindung im Programm.

### Einfaches Beispiel:

```python
zahl = int(input("Gib eine Zahl ein: "))

if zahl > 0:
    print("Die Zahl ist positiv")
elif zahl == 0:
    print("Die Zahl ist null")
else:
    print("Die Zahl ist negativ")
```

### Wichtige Hinweise:

- Verwende `if`, `elif`, `else`
- Jeder Block muss eingerückt sein
- Bedingungen können kombiniert werden:

```python
if x > 0 and x < 10:
    print("Die Zahl liegt zwischen 0 und 10")
```

---

## 🔁 Schleifen

### `for`-Schleife

Wiederholt eine Aktion mehrmals:

```python
for i in range(5):
    print("Nummer:", i)
```

`range(n)` erzeugt Zahlen von 0 bis `n-1`.

### `while`-Schleife

Wird ausgeführt, solange die Bedingung wahr ist:

```python
zahl = 0
while zahl < 3:
    print("Zahl:", zahl)
    zahl += 1
```

❗ Achte darauf, dass sich die Bedingung irgendwann ändert, sonst entsteht eine Endlosschleife.

---

## ✅ Schreibstil und Best Practices

- Verwende aussagekräftige Variablennamen.
- Achte auf korrekte Einrückung.
- Nutze Kommentare zur Erklärung wichtiger Abschnitte:

```python
# Dieser Abschnitt fragt den Namen des Benutzers ab
name = input("Wie heißt du? ")
```

- Teste deinen Code schrittweise.
- Lerne aus zuverlässigen Quellen.
- Übe mit realistischen Beispielen.

---

## 🧠 Praktische Übungen

### Übung 1: Begrüßung

Schreibe ein Programm, das den Namen des Benutzers abfragt und ihn begrüßt.

### Übung 2: Zahlenprüfung

Schreibe ein Programm, das eine Zahl abfragt und angibt, ob sie positiv, negativ oder null ist.

### Übung 3: Zählen bis 10

Verwende eine `for`-Schleife, um die Zahlen von 0 bis 9 auszugeben.

### Übung 4: Zahlen addieren

Schreibe ein Programm, das zwei Zahlen abfragt und ihre Summe ausgibt.

### Übung 5: Countdown

Verwende eine `while`-Schleife, um von 5 bis 1 rückwärts zu zählen.

---

## 📚 Empfohlene Ressourcen

- [Davood Vakilis Buchseite auf IranKetab](https://www.vakiklidavood2004.ir=)
- [Python lernen – Programmieren für Anfänger (auf Deutsch)](https://www.python-kurs.eu/)
- [Python Tutorial auf Deutsch – Programmieren lernen mit Python](https://www.programmierenlernenhq.de/python-tutorial/)
- [Python Einführung – Offizielle Dokumentation auf Deutsch](https://docs.python.org/de/3/tutorial/index.html)

---

## 🎯 Fazit

In diesem Abschnitt haben wir die grundlegenden Prinzipien von Python kennengelernt.



---



# 🇬🇧 Python Fundamentals and Basics

Welcome to the first part of the Python learning series! In this file, we’ll explore the foundational concepts of the Python programming language. The goal of this section is to build a solid understanding of Python’s structure and logic so you can confidently take the next steps.

---

## 📚 Table of Contents

- Introduction to Python
- Installation and Setup
- Syntax and Indentation
- Variables and Data Types
- Operators
- Input and Output
- Conditional Statements
- Loops
- Writing Tips and Best Practices
- Practical Exercises
- Recommended Resources
- Conclusion

---

## 🧭 Introduction to Python

Python is a high-level, interpreted, and multi-purpose programming language introduced by Guido van Rossum in 1991. Due to its simplicity, readability, and large developer community, Python is one of the most popular programming languages in the world.

### Key Features of Python:

- Simple and readable syntax
- Suitable for beginners and professionals
- Supports object-oriented, functional, and procedural programming
- Runs on various operating systems (Windows, Linux, macOS)
- Used in many fields: web development, data science, AI, automation, and more

---

## 🛠️ Installation and Setup

### Installing on Windows

1. Visit [python.org](https://www.python.org).
2. Download the latest version of Python.
3. During installation, check the "Add Python to PATH" option.
4. After installation, open the terminal (CMD) and enter:

```bash
python --version
```

If the version is displayed, the installation was successful.

### Installing on Linux / macOS

```bash
sudo apt update
sudo apt install python3  # for Linux

brew install python3      # for macOS
```

---

## ✍️ Syntax and Indentation

In Python, indentation is crucial. Unlike languages like C or Java that use braces `{}`, Python uses spaces or tabs to define code blocks.

### Example:

```python
x = 10
if x > 5:
    print("The number is greater than 5")
```

In this example, the second line must be indented. Typically, 4 spaces are used.

❗ Note: Incorrect indentation causes a SyntaxError.

---

## 📦 Variables and Data Types

### Defining Variables

In Python, you don’t need to declare the type of a variable. It’s inferred automatically.

```python
name = "Davood"
age = 21
score = 18.5
active = True
```

### Variable Naming Rules

- Use letters, numbers, and underscores (`_`) only.
- Variable names must not start with a number.
- Avoid reserved keywords like `print`, `if`, `for`.

### Basic Data Types

| Data Type | Example           | Description       |
|-----------|-------------------|-------------------|
| `int`     | `42`              | Integer           |
| `float`   | `3.14`            | Decimal number    |
| `str`     | `"Hello"`         | Text string       |
| `bool`    | `True`, `False`   | Boolean value     |
| `list`    | `[1, 2, 3]`       | List of values    |
| `dict`    | `{"name": "Davood"}` | Key-value pairs |

---

## ➕ Operators

### Arithmetic Operators

| Operator | Purpose     | Example   |
|----------|-------------|-----------|
| `+`      | Addition    | `5 + 3`   |
| `-`      | Subtraction | `10 - 2`  |
| `*`      | Multiplication | `4 * 2` |
| `/`      | Division    | `8 / 2`   |
| `%`      | Modulo      | `7 % 3`   |
| `**`     | Power       | `2 ** 3`  |

### Comparison Operators

```python
x = 5
y = 10

print(x == y)  # False
print(x < y)   # True
```

### Logical Operators

```python
a = True
b = False

print(a and b)  # False
print(a or b)   # True
print(not a)    # False
```

---

## 📥 Input and 📤 Output

### Getting Input from the User

```python
name = input("Enter your name: ")
```

Input is always received as a string. To convert to a number:

```python
age = int(input("Enter your age: "))
```

### Printing Output

```python
print("Hello", name)
```

You can separate values with commas or use formatting:

```python
print(f"Hello {name}, welcome!")
```

---

## 🔀 Conditional Statements

Conditional statements are used for decision-making in programs.

### Simple Example:

```python
number = int(input("Enter a number: "))

if number > 0:
    print("The number is positive")
elif number == 0:
    print("The number is zero")
else:
    print("The number is negative")
```

### Key Points:

- Use `if`, `elif`, `else`
- Each block must be indented
- Conditions can be combined:

```python
if x > 0 and x < 10:
    print("The number is between 0 and 10")
```

---

## 🔁 Loops

### `for` Loop

Used to repeat an action multiple times:

```python
for i in range(5):
    print("Number:", i)
```

The `range(n)` function generates numbers from 0 to `n-1`.

### `while` Loop

Repeats while a condition is true:

```python
number = 0
while number < 3:
    print("Number:", number)
    number += 1
```

❗ Make sure the condition changes to avoid infinite loops.

---

## ✅ Writing Tips and Best Practices

- Use clear and meaningful variable names.
- Write code with proper indentation.
- Use comments to explain important parts:

```python
# This section gets the user's name
name = input("What is your name? ")
```

- Test your code step by step.
- Learn from reliable sources.
- Practice with real-world examples.

---

## 🧠 Practical Exercises

### Exercise 1: Greet the User

Write a program that asks for the user's name and greets them.

### Exercise 2: Number Check

Write a program that takes a number and tells if it’s positive, negative, or zero.

### Exercise 3: Count to 10

Use a `for` loop to print numbers from 0 to 9.

### Exercise 4: Add Numbers

Write a program that takes two numbers and prints their sum.

### Exercise 5: Countdown

Use a `while` loop to print numbers from 5 to 1.

---

## 📚 Recommended Resources

- [Davood Vakili’s book page on IranKetab](https://www.vakiklidavood2004.ir=)
- [Python lernen – Programming for Beginners (in German)](https://www.python-kurs.eu/)
- [Python Tutorial in German – Learn to Code with Python](https://www.programmierenlernenhq.de/python-tutorial/)
- [Python Introduction – Official Documentation in German](https://docs.python.org/de/3/tutorial/index.html)

---

## 🎯 Conclusion

In this section, we explored the basic principles of Python.



---



# 🇮🇷 اصول و مبانی پایتون

به اولین بخش از مجموعه‌ی آموزش پایتون خوش آمدید! در این فایل، با مفاهیم پایه‌ای زبان پایتون آشنا می‌شویم. هدف این بخش، ایجاد درک عمیق از ساختار و منطق ابتدایی پایتون است تا بتوانید با اطمینان قدم‌های بعدی را بردارید.

---

## 📚 فهرست مطالب

- معرفی پایتون
- نصب و راه‌اندازی
- ساختار نوشتاری و تورفتگی
- متغیرها و انواع داده‌ها
- عملگرها
- ورودی و خروجی
- ساختارهای شرطی
- حلقه‌ها
- نکات نوشتاری و بهترین تمرین‌ها
- تمرین‌های کاربردی
- منابع پیشنهادی
- نتیجه‌گیری

---

## 🧭 معرفی پایتون

پایتون یک زبان برنامه‌نویسی سطح بالا، تفسیری و چندمنظوره است که توسط Guido van Rossum در سال ۱۹۹۱ معرفی شد. این زبان به دلیل سادگی، خوانایی بالا و جامعه‌ی بزرگ توسعه‌دهندگان، یکی از محبوب‌ترین زبان‌های برنامه‌نویسی در دنیاست.

### ویژگی‌های مهم پایتون:

- سینتکس ساده و قابل فهم
- مناسب برای مبتدیان و حرفه‌ای‌ها
- پشتیبانی از برنامه‌نویسی شی‌گرا، تابعی و رویه‌ای
- قابل اجرا در سیستم‌عامل‌های مختلف (ویندوز، لینوکس، مک)
- کاربرد در زمینه‌های مختلف: وب، داده‌کاوی، هوش مصنوعی، اتوماسیون، و...

---

## 🛠️ نصب و راه‌اندازی

### نصب در ویندوز

1. به سایت [python.org](https://www.python.org) بروید.
2. آخرین نسخه‌ی Python را دانلود کنید.
3. هنگام نصب، گزینه‌ی "Add Python to PATH" را فعال کنید.
4. پس از نصب، ترمینال (CMD) را باز کرده و دستور زیر را وارد کنید:

```bash
python --version
```

اگر نسخه‌ی پایتون نمایش داده شد، نصب موفق بوده است.

### نصب در لینوکس / مک

```bash
sudo apt update
sudo apt install python3  # برای لینوکس

brew install python3      # برای macOS
```

---

## ✍️ ساختار نوشتاری و تورفتگی (Indentation)

در پایتون، تورفتگی نقش کلیدی دارد. برخلاف زبان‌هایی مثل C یا Java که از براکت `{}` استفاده می‌کنند، پایتون با فاصله‌گذاری (space یا tab) بلوک‌های کد را مشخص می‌کند.

### مثال:

```python
x = 10
if x > 5:
    print("عدد بزرگ‌تر از ۵ است")
```

در این مثال، خط دوم باید با تورفتگی نوشته شود. معمولاً از ۴ فضای خالی استفاده می‌شود.

❗ توجه: تورفتگی اشتباه باعث خطای نحوی (SyntaxError) می‌شود.

---

## 📦 متغیرها و انواع داده‌ها

### تعریف متغیر

در پایتون، نیازی به تعیین نوع متغیر نیست. نوع داده به‌صورت خودکار تشخیص داده می‌شود.

```python
نام = "داوود"
سن = ۳۰
نمره = ۱۸.۵
فعال = True
```

### قواعد نام‌گذاری متغیرها

- فقط از حروف، اعداد و زیرخط (`_`) استفاده کنید.
- نام متغیر نباید با عدد شروع شود.
- از نام‌های رزرو شده مثل `print`, `if`, `for` استفاده نکنید.

### انواع داده‌های پایه

| نوع داده | مثال           | توضیح |
|----------|----------------|-------|
| `int`    | `42`           | عدد صحیح |
| `float`  | `3.14`         | عدد اعشاری |
| `str`    | `"سلام"`       | رشته‌ی متنی |
| `bool`   | `True`, `False`| مقدار منطقی |
| `list`   | `[1, 2, 3]`    | لیست از داده‌ها |
| `dict`   | `{"نام": "داوود"}` | دیکشنری (کلید-مقدار) |

---

## ➕ عملگرها

### عملگرهای ریاضی

| عملگر | کاربرد | مثال |
|-------|--------|-------|
| `+`   | جمع     | `5 + 3` |
| `-`   | تفریق   | `10 - 2` |
| `*`   | ضرب     | `4 * 2` |
| `/`   | تقسیم   | `8 / 2` |
| `%`   | باقی‌مانده | `7 % 3` |
| `**`  | توان     | `2 ** 3` |

### عملگرهای مقایسه‌ای

```python
x = 5
y = 10

print(x == y)  # False
print(x < y)   # True
```

### عملگرهای منطقی

```python
a = True
b = False

print(a and b)  # False
print(a or b)   # True
print(not a)    # False
```

---

## 📥 ورودی و 📤 خروجی

### دریافت ورودی از کاربر

```python
نام = input("نام خود را وارد کنید: ")
```

ورودی همیشه به‌صورت رشته (`str`) دریافت می‌شود. برای تبدیل به عدد:

```python
سن = int(input("سن خود را وارد کنید: "))
```

### چاپ خروجی

```python
print("سلام", نام)
```

می‌توان چند مقدار را با کاما جدا کرد یا از قالب‌بندی استفاده کرد:

```python
print(f"سلام {نام}، خوش آمدی!")
```

---

## 🔀 ساختارهای شرطی

ساختار شرطی برای تصمیم‌گیری در برنامه استفاده می‌شود.

### مثال ساده:

```python
عدد = int(input("یک عدد وارد کنید: "))

if عدد > 0:
    print("عدد مثبت است")
elif عدد == 0:
    print("عدد صفر است")
else:
    print("عدد منفی است")
```

### نکات مهم:

- از `if`, `elif`, `else` استفاده می‌شود.
- هر بلوک باید با تورفتگی مشخص شود.
- شرط‌ها می‌توانند ترکیبی باشند:

```python
if x > 0 and x < 10:
    print("عدد بین ۰ و ۱۰ است")
```

---

## 🔁 حلقه‌ها

### حلقه `for`

برای تکرار یک عمل چند بار:

```python
for i in range(5):
    print("شماره:", i)
```

تابع `range(n)` از ۰ تا `n-1` را تولید می‌کند.

### حلقه `while`

تا زمانی که شرط برقرار باشد:

```python
عدد = 0
while عدد < 3:
    print("عدد:", عدد)
    عدد += 1
```

❗ مراقب باشید که شرط حلقه حتماً در جایی تغییر کند تا حلقه بی‌نهایت نشود.

---

## ✅ نکات نوشتاری و بهترین تمرین‌ها

- از نام‌های واضح و معنادار برای متغیرها استفاده کنید.
- کد را با تورفتگی مناسب بنویسید.
- از کامنت‌ها برای توضیح بخش‌های مهم استفاده کنید:

```python
# این بخش نام کاربر را دریافت می‌کند
نام = input("نام شما چیست؟ ")
```

- کد را مرحله‌به‌مرحله تست کنید.
- از منابع معتبر برای یادگیری استفاده کنید.
- همیشه کد را با مثال‌های واقعی تمرین کنید.

---

## 🧠 تمرین‌های کاربردی

### تمرین ۱: سلام به کاربر

برنامه‌ای بنویس که نام کاربر را دریافت کرده و با او سلام کند.

### تمرین ۲: بررسی عدد

برنامه‌ای بنویس که عددی از کاربر بگیرد و مشخص کند مثبت، منفی یا صفر است.

### تمرین ۳: شمارش تا ۱۰

با استفاده از حلقه `for`، اعداد ۰ تا ۹ را چاپ کن.

### تمرین ۴: جمع اعداد

برنامه‌ای بنویس که دو عدد از کاربر دریافت کرده و حاصل جمع آن‌ها را نمایش دهد.

### تمرین ۵: شمارش معکوس

با استفاده از حلقه `while`، از عدد ۵ تا ۱ را چاپ کن.

---

## 📚 منابع پیشنهادی
- [صفحه‌ی کتاب‌های داوود وکیلی در ایران‌کتاب](https://www.vakiklidavood2004.ir=)
- [Python lernen – Programmieren für Anfänger (auf deutsch)](https://www.python-kurs.eu/)
- [Python Tutorial auf Deutsch – Programmieren lernen mit Python](https://www.programmierenlernenhq.de/python-tutorial/)
- [Python Einführung – offizielle Dokumentation auf Deutsch](https://docs.python.org/de/3/tutorial/index.html)
---

## 🎯 نتیجه‌گیری

در این بخش، با اصول اولیه‌ی پایتون آشنا شدیم