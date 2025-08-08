
# برنامه‌نویسی شی‌گرا و ماژولار در پایتون

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

حتماً داوود جان! ادامه مقاله از بخش ۱۴ به بعد رو برات با ساختار حرفه‌ای، زبان روان، و مارک‌داون کامل می‌نویسم تا مقاله‌ات بی‌نقص باشه:

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