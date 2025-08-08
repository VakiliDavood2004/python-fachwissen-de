# 🇩🇪 Abschnitt 3: Objektorientierte und modulare Programmierung in Python

In diesem Artikel erkunden wir zwei wichtige Programmierparadigmen in Python:  
**Objektorientierte Programmierung (OOP)** und  
**Modulare Programmierung**.

Diese Stile helfen uns, strukturierten, wartbaren und skalierbaren Code zu schreiben.

---

## Inhaltsverzeichnis

1. Einführung in OOP und modulare Programmierung  
2. Klassen definieren und Objekte erstellen  
3. Attribute und Methoden  
4. Konstruktoren (`__init__`)  
5. Vererbung  
6. Polymorphismus  
7. Kapselung  
8. Modulare Programmierung in Python  
9. Module erstellen und verwenden  
10. Praktische Übungen  
11. Mini-Projekt: Bestellverwaltung im Shop  
12. Vergleich OOP mit funktionalem Stil  
13. Tests für Klassen schreiben  
14. Empfohlene Ressourcen  
15. Abschließendes Fazit  

---

## 1. Einführung in OOP und modulare Programmierung

Die objektorientierte Programmierung basiert auf dem Konzept der „Objekte“. Jedes Objekt ist eine Kombination aus Daten und Verhalten.  
Die modulare Programmierung konzentriert sich darauf, Code in unabhängige, wiederverwendbare Komponenten zu unterteilen.

**Vorteile von OOP:**

- Bessere Codeorganisation  
- Skalierbarkeit und Wartbarkeit  
- Wiederverwendbarkeit von Code  

**Vorteile der modularen Programmierung:**

- Trennung von Verantwortlichkeiten  
- Reduzierte Komplexität  
- Verbesserte Lesbarkeit und Testbarkeit  

---

## 2. Klassen definieren und Objekte erstellen

Klassen sind Vorlagen zur Erstellung von Objekten. Objekte sind Instanzen von Klassen.

```python
class Book:
    pass

my_book = Book()
print(type(my_book))  # Output: <class '__main__.Book'>
```

---

## 3. Attribute und Methoden

Attribute sind Daten, die zu einem Objekt gehören. Methoden sind Funktionen, die auf dem Objekt ausgeführt werden.

```python
class Phone:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def call(self, number):
        print(f"Calling {number} using {self.brand} {self.model}")

device = Phone("Samsung", "Galaxy S21")
device.call("09120059751")
```

---

## 4. Konstruktoren (`__init__`)

Die Methode `__init__` wird beim Erstellen eines Objekts ausgeführt und dient zur Initialisierung.

```python
class User:
    def __init__(self, name, email):
        self.name = name
        self.email = email

    def introduce(self):
        print(f"Name: {self.name} - Email: {self.email}")

u = User("Davood", "davood@example.com")
u.introduce()
```

---

## 5. Vererbung

Vererbung ermöglicht es uns, Attribute und Methoden von einer Klasse auf eine andere zu übertragen.

```python
class Device:
    def turn_on(self):
        print("Device is now on.")

class Laptop(Device):
    def turn_on(self):
        print("Laptop is now on.")

dell = Laptop()
dell.turn_on()
```

---

## 6. Polymorphismus

Polymorphismus bedeutet, dass eine Funktion je nach Objekttyp unterschiedlich reagieren kann.

```python
class Bird:
    def sound(self):
        print("Tweet tweet")

class Car:
    def sound(self):
        print("Beep beep")

def play_sound(obj):
    obj.sound()

play_sound(Bird())
play_sound(Car())
```

---

## 7. Kapselung

Kapselung bedeutet, interne Details einer Klasse zu verbergen und deren Daten zu schützen.

```python
class Account:
    def __init__(self):
        self.__password = "1234"

    def check_password(self, input_password):
        if input_password == self.__password:
            print("Access granted")
        else:
            print("Incorrect password")

my_account = Account()
my_account.check_password("1234")
```

---

## 8. Modulare Programmierung in Python

In der modularen Programmierung platzieren wir Code in separaten Dateien, um ihn wiederverwendbar zu machen.

### Datei: `math_tools.py`

```python
def multiply(a, b):
    return a * b

def divide(a, b):
    return a / b
```

### Verwendung in einer anderen Datei:

```python
import math_tools

print(math_tools.multiply(4, 5))  # Output: 20
```

---

## 9. Module erstellen und verwenden

So erstellst du ein Modul:

1. Erstelle eine `.py`-Datei  
2. Definiere Funktionen oder Klassen darin  
3. Verwende `import` in einer anderen Datei, um darauf zuzugreifen  

Beispiel:

```python
# Datei: greetings.py
def greet(name):
    print(f"Hello, dear {name}!")

# Datei: main.py
import greetings

greetings.greet("Davood")
```

---

## 10. Praktische Übungen

1. Erstelle eine Klasse `Student` mit Attributen für Name und Studienfach sowie einer Methode zur Ausgabe der Informationen.  
2. Erstelle eine Klasse `Order` mit Methoden zum Hinzufügen von Artikeln und zur Berechnung des Gesamtpreises.  
3. Erstelle eine Klasse `Driver`, die von einer Klasse `Person` erbt und eine Methode zum Fahren enthält.  
4. Erstelle ein Modul mit Funktionen zur Temperaturumrechnung (Celsius in Fahrenheit).  
5. Erstelle eine Klasse `Timer` mit Start- und Stopmethoden und verwende Kapselung zum Schutz der Zeitdaten.  

---

## 11. Mini-Projekt: Bestellverwaltung im Shop

### Datei: `product.py`

```python
# Datei: product.py
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price
```

### Datei: `order.py`

```python
from product import Product

class Order:
    def __init__(self):
        self.items = []

    def add(self, product):
        self.items.append(product)

    def total(self):
        return sum([p.price for p in self.items])
```

### Datei: `main.py`

```python
from product import Product
from order import Order

p1 = Product("Book", 120000)
p2 = Product("Pen", 8000)

order = Order()
order.add(p1)
order.add(p2)

print(f"Total order: {order.total()} Toman")
```

---

## 12. Vergleich OOP mit funktionalem Stil

| Merkmal         | Objektorientiert                | Funktional                    |
|----------------|----------------------------------|-------------------------------|
| Fokus           | Objekte und Klassen             | Reine Funktionen              |
| Zustandsänderung| Erlaubt                         | Vermeidet Zustandsänderung    |
| Testbarkeit     | Abhängig vom Design             | Einfacher                     |
| Struktur        | Hierarchisch                    | Linear und funktionsbasiert   |

---

## 13. Tests für Klassen schreiben

```python
import unittest

class Car:
    def __init__(self, model):
        self.model = model

    def move(self):
        return f"{self.model} is moving."

class TestCar(unittest.TestCase):
    def test_move(self):
        c = Car("Toyota")
        self.assertEqual(c.move(), "Toyota is moving.")

if __name__ == "__main__":
    unittest.main()
```

---

## 14. Empfohlene Ressourcen

Um dein Verständnis der objektorientierten und modularen Programmierung in Python zu vertiefen, sind die folgenden Ressourcen sehr empfehlenswert:

- [Offizielle Python-Dokumentation](https://docs.python.org/3/tutorial/classes.html) – Ein vollständiger Leitfaden zu Klassen und OOP in Python  
- Buch: *Python Object-Oriented Programming* von Dusty Phillips  
- Online-Kurse auf Plattformen wie Coursera, Udemy und edX  
- Dokumentation zur `unittest`-Bibliothek für das Schreiben von Tests  
- Tutorials und Artikel auf [Real Python](https://realpython.com)

---

## ❓ Fragen zu Abschnitt Sechs: Objektorientierte und modulare Programmierung in Python

### 1️⃣ Was ist der Unterschied zwischen einer Klasse und einem Objekt in Python?
- Erkläre anhand eines Beispiels, wie eine Klasse definiert und ein Objekt daraus erstellt wird.

### 2️⃣ Was ist Vererbung in der objektorientierten Programmierung und wozu dient sie?
- Schreibe ein Beispiel für eine Basisklasse und eine Kindklasse, die Attribute erbt.

### 3️⃣ Was ist der Unterschied zwischen den Methoden `__init__()` und `__str__()` in Python-Klassen?
- Erkläre die Verwendung jeder Methode mit einem Beispiel.

### 4️⃣ Wie kann man ein Python-Modul definieren und in einer anderen Datei verwenden?
- Gib ein Beispiel für die Erstellung einer Datei `mymodule.py` und deren Import in der Hauptdatei.

### 5️⃣ Welche Vorteile hat es, ein Programm modular zu gestalten?
- Nenne Aspekte wie Lesbarkeit, Testbarkeit, Wartbarkeit und Wiederverwendbarkeit.

---

## 15. Abschließendes Fazit

Objektorientierte und modulare Programmierung sind zwei grundlegende Säulen beim Design professioneller Software.  
Durch die Verwendung von Klassen, Objekten, Vererbung und Kapselung kannst du Code schreiben, der sowohl skalierbar als auch wartbar ist.  
Die Aufteilung des Codes in unabhängige Module ermöglicht es dir, Projekte zu erstellen, die lesbar, testbar und wiederverwendbar sind.

Wenn du größere und professionellere Python-Projekte erstellen möchtest, ist die Beherrschung dieser beiden Stile unerlässlich.  
Übung, kleine Projekte und das Studium zuverlässiger Ressourcen ebnen dir den Weg für deinen Lernprozess.



---



# 🇬🇧 Section 3: Object-Oriented and Modular Programming in Python

In this article, we explore two important programming paradigms in Python:  
**Object-Oriented Programming (OOP)** and  
**Modular Programming**.

These styles help us write structured, maintainable, and scalable code.

---

## Table of Contents

1. Introduction to OOP and Modular Programming  
2. Defining Classes and Creating Objects  
3. Attributes and Methods  
4. Constructors (`__init__`)  
5. Inheritance  
6. Polymorphism  
7. Encapsulation  
8. Modular Programming in Python  
9. Creating and Using Modules  
10. Practical Exercises  
11. Mini Project: Store Order Management  
12. Comparing OOP with Functional Style  
13. Writing Tests for Classes  
14. Recommended Resources  
15. Final Conclusion  

---

## 1. Introduction to OOP and Modular Programming

Object-oriented programming is based on the concept of “objects.” Each object is a combination of data and behavior.  
Modular programming focuses on dividing code into independent, reusable components.

**Advantages of OOP:**

- Better code organization  
- Scalability and maintainability  
- Code reuse  

**Advantages of Modular Programming:**

- Separation of concerns  
- Reduced complexity  
- Improved readability and testability  

---

## 2. Defining Classes and Creating Objects

Classes are templates for creating objects. Objects are instances of classes.

```python
class Book:
    pass

my_book = Book()
print(type(my_book))  # Output: <class '__main__.Book'>
```

---

## 3. Attributes and Methods

Attributes are data that belong to an object. Methods are functions that operate on the object.

```python
class Phone:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def call(self, number):
        print(f"Calling {number} using {self.brand} {self.model}")

device = Phone("Samsung", "Galaxy S21")
device.call("09120059751")
```

---

## 4. Constructors (`__init__`)

The `__init__` method runs when an object is created and is used for initialization.

```python
class User:
    def __init__(self, name, email):
        self.name = name
        self.email = email

    def introduce(self):
        print(f"Name: {self.name} - Email: {self.email}")

u = User("Davood", "davood@example.com")
u.introduce()
```

---

## 5. Inheritance

Inheritance allows us to transfer attributes and methods from one class to another.

```python
class Device:
    def turn_on(self):
        print("Device is now on.")

class Laptop(Device):
    def turn_on(self):
        print("Laptop is now on.")

dell = Laptop()
dell.turn_on()
```

---

## 6. Polymorphism

Polymorphism means a function can behave differently depending on the object type.

```python
class Bird:
    def sound(self):
        print("Tweet tweet")

class Car:
    def sound(self):
        print("Beep beep")

def play_sound(obj):
    obj.sound()

play_sound(Bird())
play_sound(Car())
```

---

## 7. Encapsulation

Encapsulation means hiding internal details of a class and protecting its data.

```python
class Account:
    def __init__(self):
        self.__password = "1234"

    def check_password(self, input_password):
        if input_password == self.__password:
            print("Access granted")
        else:
            print("Incorrect password")

my_account = Account()
my_account.check_password("1234")
```

---

## 8. Modular Programming in Python

In modular programming, we place code in separate files to make it reusable.

### File: `math_tools.py`

```python
def multiply(a, b):
    return a * b

def divide(a, b):
    return a / b
```

### Usage in another file:

```python
import math_tools

print(math_tools.multiply(4, 5))  # Output: 20
```

---

## 9. Creating and Using Modules

To create a module:

1. Create a `.py` file  
2. Define functions or classes inside it  
3. Use `import` in another file to access them  

Example:

```python
# File: greetings.py
def greet(name):
    print(f"Hello, dear {name}!")

# File: main.py
import greetings

greetings.greet("Davood")
```

---

## 10. Practical Exercises

1. Create a `Student` class with attributes for name and major, and a method to print info.  
2. Create an `Order` class with methods to add items and calculate total price.  
3. Create a `Driver` class that inherits from a `Person` class and includes a driving method.  
4. Create a module with functions to convert temperature (Celsius to Fahrenheit).  
5. Create a `Timer` class with start and stop methods, using encapsulation to protect time data.  

---

## 11. Mini Project: Store Order Management

### File: `product.py`

```python
# File: product.py
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price
```

### File: `order.py`

```python
from product import Product

class Order:
    def __init__(self):
        self.items = []

    def add(self, product):
        self.items.append(product)

    def total(self):
        return sum([p.price for p in self.items])
```

### File: `main.py`

```python
from product import Product
from order import Order

p1 = Product("Book", 120000)
p2 = Product("Pen", 8000)

order = Order()
order.add(p1)
order.add(p2)

print(f"Total order: {order.total()} Toman")
```

---

## 12. Comparing OOP with Functional Style

| Feature         | Object-Oriented                 | Functional                    |
|----------------|----------------------------------|-------------------------------|
| Focus           | Objects and Classes             | Pure Functions                |
| State Mutation  | Allowed                         | Avoided                       |
| Testability     | Depends on design               | Easier                        |
| Structure       | Hierarchical                    | Linear and function-driven    |

---

## 13. Writing Tests for Classes

```python
import unittest

class Car:
    def __init__(self, model):
        self.model = model

    def move(self):
        return f"{self.model} is moving."

class TestCar(unittest.TestCase):
    def test_move(self):
        c = Car("Toyota")
        self.assertEqual(c.move(), "Toyota is moving.")

if __name__ == "__main__":
    unittest.main()
```
---

## 14. Recommended Resources

To deepen your understanding of object-oriented and modular programming in Python, the following resources are highly recommended:

- [Official Python Documentation](https://docs.python.org/3/tutorial/classes.html) – A complete guide to classes and OOP in Python  
- Book: *Python Object-Oriented Programming* by Dusty Phillips  
- Online courses on platforms like Coursera, Udemy, and edX  
- Documentation for the `unittest` library for writing class tests  
- Tutorials and articles on [Real Python](https://realpython.com)

---

## ❓ Section Six Questions: Object-Oriented and Modular Programming in Python

### 1️⃣ What is the difference between a class and an object in Python?
- Explain with an example how a class is defined and how an object is created from it.

### 2️⃣ What is inheritance in object-oriented programming and what is its purpose?
- Write an example of a base class and a child class that inherits its attributes.

### 3️⃣ What is the difference between the `__init__()` and `__str__()` methods in Python classes?
- Explain the use of each with an example.

### 4️⃣ How can you define a Python module and use it in another file?
- Provide an example of creating a `mymodule.py` file and importing it in the main file.

### 5️⃣ What are the benefits of designing a program in a modular way?
- Mention aspects like readability, testability, maintainability, and reusability.

---

## 15. Final Conclusion

Object-oriented and modular programming are two essential pillars in designing professional software.  
By using classes, objects, inheritance, and encapsulation, you can write code that is both scalable and maintainable.  
On the other hand, dividing code into independent modules allows you to build projects that are readable, testable, and reusable.

If you aim to build larger and more professional Python projects, mastering these two styles is a must.  
Practice, small projects, and studying reliable resources will pave the way for your learning journey.



---



# 🇮🇷 بخش 3 برنامه‌نویسی شی‌گرا و ماژولار در پایتون

در این مقاله، با دو سبک مهم برنامه‌نویسی در پایتون آشنا می‌شویم:  
**برنامه‌نویسی شی‌گرا (Object-Oriented Programming – OOP)** و  
**برنامه‌نویسی ماژولار (Modular Programming)**.

این دو سبک به ما کمک می‌کنند تا کدهایی ساختارمند، قابل نگهداری، و قابل توسعه بنویسیم.
 
---

## فهرست مطالب

1. مقدمه‌ای بر OOP و Modular Programming  
2. تعریف کلاس و ساخت شیء  
3. ویژگی‌ها (Attributes) و رفتارها (Methods)  
4. سازنده‌ها (`__init__`)  
5. وراثت (Inheritance)  
6. چندریختی (Polymorphism)  
7. کپسوله‌سازی (Encapsulation)  
8. برنامه‌نویسی ماژولار در پایتون  
9. ساخت و استفاده از ماژول‌ها  
10. تمرین‌های عملی  
11. پروژه‌ی کوچک: مدیریت سفارشات فروشگاه  
12. مقایسه OOP با سبک تابعی  
13. تست‌نویسی کلاس‌ها  
14. منابع پیشنهادی  
15. نتیجه‌گیری نهایی  

---

## 1. مقدمه‌ای بر OOP و Modular Programming

برنامه‌نویسی شی‌گرا بر اساس مفهوم "اشیاء" طراحی شده است. هر شیء ترکیبی از داده‌ها و رفتارهاست.  
برنامه‌نویسی ماژولار به تقسیم کد به بخش‌های مستقل و قابل استفاده مجدد می‌پردازد.

**مزایای OOP:**

- سازمان‌دهی بهتر کد  
- قابلیت توسعه و نگهداری  
- استفاده مجدد از کد  

**مزایای Modular Programming:**

- جداسازی وظایف  
- کاهش پیچیدگی  
- افزایش خوانایی و تست‌پذیری  

---

## 2. تعریف کلاس و ساخت شیء

کلاس‌ها قالب‌هایی برای ساخت اشیاء هستند. اشیاء نمونه‌هایی از کلاس‌ها هستند.

```python
class Book:
    pass

my_book = Book()
print(type(my_book))  # Output: <class '__main__.Book'>
```

---

## 3. ویژگی‌ها (Attributes) و رفتارها (Methods)

ویژگی‌ها داده‌هایی هستند که به شیء تعلق دارند. رفتارها توابعی هستند که روی شیء اجرا می‌شوند.

```python
class Phone:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def call(self, number):
        print(f"Calling {number} using {self.brand} {self.model}")

device = Phone("Samsung", "Galaxy S21")
device.call("09120059751")
```

---

## 4. سازنده‌ها (`__init__`)

تابع `__init__` هنگام ساخت شیء اجرا می‌شود و برای مقداردهی اولیه استفاده می‌شود.

```python
class User:
    def __init__(self, name, email):
        self.name = name
        self.email = email

    def introduce(self):
        print(f"Name: {self.name} - Email: {self.email}")

u = User("Davood", "davood@example.com")
u.introduce()
```

---

## 5. وراثت (Inheritance)

وراثت به ما اجازه می‌دهد ویژگی‌ها و رفتارهای یک کلاس را به کلاس دیگر منتقل کنیم.

```python
class Device:
    def turn_on(self):
        print("Device is now on.")

class Laptop(Device):
    def turn_on(self):
        print("Laptop is now on.")

dell = Laptop()
dell.turn_on()
```

---

## 6. چندریختی (Polymorphism)

چندریختی یعنی یک تابع می‌تواند رفتارهای متفاوتی بسته به نوع شیء داشته باشد.

```python
class Bird:
    def sound(self):
        print("Tweet tweet")

class Car:
    def sound(self):
        print("Beep beep")

def play_sound(obj):
    obj.sound()

play_sound(Bird())
play_sound(Car())
```

---

## 7. کپسوله‌سازی (Encapsulation)

کپسوله‌سازی یعنی پنهان‌سازی جزئیات داخلی کلاس و محافظت از داده‌ها.

```python
class Account:
    def __init__(self):
        self.__password = "1234"

    def check_password(self, input_password):
        if input_password == self.__password:
            print("Access granted")
        else:
            print("Incorrect password")

my_account = Account()
my_account.check_password("1234")
```

---

## 8. برنامه‌نویسی ماژولار در پایتون

در برنامه‌نویسی ماژولار، کدها را در فایل‌های جداگانه قرار می‌دهیم تا قابل استفاده مجدد باشند.

### فایل `math_tools.py`

```python
def multiply(a, b):
    return a * b

def divide(a, b):
    return a / b
```

### استفاده در فایل دیگر:

```python
import math_tools

print(math_tools.multiply(4, 5))  # Output: 20
```

---

## 9. ساخت و استفاده از ماژول‌ها

برای ساخت ماژول:

1. یک فایل `.py` بسازید  
2. توابع یا کلاس‌ها را در آن تعریف کنید  
3. در فایل دیگر با `import` استفاده کنید  

مثال:

```python
# File: greetings.py
def greet(name):
    print(f"Hello, dear {name}!")

# File: main.py
import greetings

greetings.greet("Davood")
```

---

## 10. تمرین‌های عملی

1. کلاس `دانشجو` بسازید با ویژگی‌های نام و رشته، و متدی برای چاپ اطلاعات.  
2. کلاس `سفارش` بسازید با متد افزودن کالا و محاسبه مجموع قیمت.  
3. کلاس `راننده` بسازید که از کلاس `شخص` ارث‌بری کند و متدی برای رانندگی داشته باشد.  
4. ماژولی بسازید که توابع مربوط به تبدیل دما (سانتی‌گراد به فارنهایت) را شامل شود.  
5. کلاس `تایمر` بسازید با متد شروع و توقف، و از کپسوله‌سازی برای محافظت از زمان استفاده کنید.  

---

## 11. پروژه‌ی کوچک: مدیریت سفارشات فروشگاه

### فایل `product.py`

```python
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price
```

### فایل `order.py`

```python
from product import Product

class Order:
    def __init__(self):
        self.items = []

    def add(self, product):
        self.items.append(product)

    def total(self):
        return sum([p.price for p in self.items])
```

### فایل `main.py`

```python
from product import Product
from order import Order

p1 = Product("Book", 120000)
p2 = Product("Pen", 8000)

order = Order()
order.add(p1)
order.add(p2)

print(f"Total order: {order.total()} Toman")
```

---

## 12. مقایسه OOP با سبک تابعی

| ویژگی           | شی‌گرا                        | تابعی                        |
|----------------|------------------------------|------------------------------|
| تمرکز          | اشیاء و کلاس‌ها              | توابع خالص                   |
| تغییر وضعیت    | مجاز                         | اجتناب از آن                 |
| تست‌پذیری      | وابسته به طراحی             | ساده‌تر                     |
| ساختار         | سلسله‌مراتبی                 | خطی و تابع‌محور             |

---

## 13. تست‌نویسی کلاس‌ها

```python
import unittest

class Car:
    def __init__(self, model):
        self.model = model

    def move(self):
        return f"{self.model} is moving."

class TestCar(unittest.TestCase):
    def test_move(self):
        c = Car("Toyota")
        self.assertEqual(c.move(), "Toyota is moving.")

if __name__ == "__main__":
    unittest.main()
```
---

## 14. منابع پیشنهادی

برای یادگیری عمیق‌تر برنامه‌نویسی شی‌گرا و ماژولار در پایتون، منابع زیر توصیه می‌شوند:

- [مستندات رسمی پایتون](https://docs.python.org/3/tutorial/classes.html) – راهنمای کامل کلاس‌ها و شی‌گرایی در پایتون  
- کتاب "Python Object-Oriented Programming" نوشته Dusty Phillips  
- دوره‌های آموزشی در پلتفرم‌های Coursera، Udemy، و edX  
- مستندات کتابخانه `unittest` برای تست‌نویسی کلاس‌ها  
- مقالات و آموزش‌های رسمی در [Real Python](https://realpython.com)

---


## ❓ سوالات بخش ششم: برنامه‌نویسی شی‌گرا و ماژولار در پایتون (Objektorientierte und modulare Programmierung in Python)

### 1️⃣ تفاوت بین کلاس (class) و شیء (object) در پایتون چیست؟
- با ذکر مثال توضیح دهید که چگونه یک کلاس تعریف می‌شود و چگونه از آن شیء ساخته می‌شود.

### 2️⃣ مفهوم وراثت (Inheritance) در برنامه‌نویسی شی‌گرا چیست و چه کاربردی دارد؟
- مثالی از کلاس پایه و کلاس فرزند بنویسید که ویژگی‌ها را به ارث می‌برد.

### 3️⃣ تفاوت بین متدهای `__init__()` و `__str__()` در کلاس‌های پایتون چیست؟
- کاربرد هرکدام را با مثال توضیح دهید.

### 4️⃣ چگونه می‌توان یک ماژول پایتونی تعریف و در فایل دیگر استفاده کرد؟
- مثالی از ساخت فایل `mymodule.py` و استفاده از آن در فایل اصلی با `import` بیاورید.

### 5️⃣ چه مزایایی دارد که برنامه را به صورت ماژولار طراحی کنیم؟
- به مواردی مثل خوانایی، تست‌پذیری، نگهداری آسان، و استفاده‌ی مجدد اشاره کنید.

---

## 15. نتیجه‌گیری نهایی

برنامه‌نویسی شی‌گرا و ماژولار دو ستون مهم در طراحی نرم‌افزارهای حرفه‌ای هستند.  
با استفاده از کلاس‌ها، اشیاء، وراثت، و کپسوله‌سازی می‌توان کدی نوشت که هم قابل توسعه باشد و هم قابل نگهداری.  
از طرفی، با تقسیم کد به ماژول‌های مستقل، می‌توان پروژه‌هایی ساخت که خوانا، تست‌پذیر، و قابل استفاده مجدد باشند.

اگر می‌خواهید پروژه‌های بزرگ‌تر و حرفه‌ای‌تری در پایتون بسازید، تسلط بر این دو سبک ضروری است.  
تمرین، پروژه‌های کوچک، و مطالعه منابع معتبر، مسیر یادگیری شما را هموار خواهد کرد.

---