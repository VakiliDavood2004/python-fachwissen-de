# 📘 Umfassende Einführung in die Programmiersprache C

---

## 🧠 Einleitung

Die Programmiersprache C wurde 1972 von Dennis Ritchie entwickelt und gilt als eine der grundlegendsten und einflussreichsten Sprachen der Informatik. Viele moderne Sprachen wie C++, Java, Python und Rust basieren auf C. Wer Programmieren wirklich verstehen will, sollte mit C beginnen.

---

## 🎯 Warum C lernen?

- 🔧 **Tiefes Verständnis für Computer:** C zeigt dir, wie Speicher, Prozessor und Betriebssysteme funktionieren.
- 🚀 **Hohe Geschwindigkeit:** C-Programme sind extrem schnell.
- 🧩 **Portabilität:** C-Code läuft auf verschiedenen Betriebssystemen.
- 🧠 **Algorithmisches Denken:** C trainiert dein logisches Denken und deine Problemlösungsfähigkeiten.

---

## 🛠️ Entwicklungsumgebung einrichten

### Unter Windows:
- [Code::Blocks](http://www.codeblocks.org/) installieren  
- oder [Dev-C++](https://sourceforge.net/projects/orwelldevcpp/)

### Unter Linux:
```bash
sudo apt update
sudo apt install gcc
```

### Unter macOS:
```bash
xcode-select --install
```

---

## 🧱 Grundstruktur eines C-Programms

```c
#include <stdio.h>

int main() {
    printf("Hallo Welt!\n");
    return 0;
}
```

### Erklärung:

| Teil | Beschreibung |
|------|--------------|
| `#include <stdio.h>` | Einbinden der Standardbibliothek für Ein-/Ausgabe |
| `int main()` | Hauptfunktion, Einstiegspunkt des Programms |
| `printf()` | Gibt Text auf dem Bildschirm aus |
| `return 0;` | Beendet das Programm erfolgreich |

---

## 🔤 Datentypen in C

| Typ | Beschreibung | Beispiel |
|-----|--------------|----------|
| `int` | Ganzzahl | `int alter = 25;` |
| `float` | Dezimalzahl | `float pi = 3.14;` |
| `char` | Einzelnes Zeichen | `char note = 'A';` |
| `double` | Präzise Dezimalzahl | `double g = 9.81;` |

---

## 📦 Variablen und Operatoren

### Variablen deklarieren:
```c
int x = 10;
float y = 5.5;
```

### Operatoren:

| Operator | Zweck | Beispiel |
|----------|-------|----------|
| `+` | Addition | `x + y` |
| `-` | Subtraktion | `x - y` |
| `*` | Multiplikation | `x * y` |
| `/` | Division | `x / y` |
| `%` | Modulo | `x % 3` |

---

## 🔁 Kontrollstrukturen

### Bedingungen:
```c
int punktzahl = 85;
if (punktzahl >= 90) {
    printf("Ausgezeichnet!\n");
} else if (punktzahl >= 70) {
    printf("Gut!\n");
} else {
    printf("Mehr üben!\n");
}
```

### Schleifen:

#### For-Schleife:
```c
for (int i = 0; i < 5; i++) {
    printf("Zahl: %d\n", i);
}
```

#### While-Schleife:
```c
int i = 0;
while (i < 5) {
    printf("Zahl: %d\n", i);
    i++;
}
```

#### Do-While-Schleife:
```c
int i = 0;
do {
    printf("Zahl: %d\n", i);
    i++;
} while (i < 5);
```

---

## 🧮 Funktionen in C

Funktionen helfen, den Code modular und wiederverwendbar zu gestalten.

```c
int summe(int a, int b) {
    return a + b;
}

int main() {
    int ergebnis = summe(3, 4);
    printf("Ergebnis: %d\n", ergebnis);
    return 0;
}
```

---

## 📚 Arrays

Arrays speichern mehrere Werte desselben Typs.

```c
int zahlen[3] = {10, 20, 30};
printf("Zweite Zahl: %d\n", zahlen[1]);
```

---

## 📌 Zeiger (Pointers)

Zeiger speichern Speicheradressen von Variablen.

```c
int x = 10;
int *ptr = &x;
printf("Wert von x: %d\n", *ptr);
```

| Konzept | Beschreibung |
|---------|--------------|
| `&x` | Adresse der Variable x |
| `*ptr` | Wert an der Adresse des Zeigers |

---

## 🗂️ Einfache Datenstrukturen

### Strings:
```c
char name[] = "Davood";
printf("Name: %s\n", name);
```

### Strukturen:
```c
struct Auto {
    char modell[20];
    int jahr;
};

int main() {
    struct Auto meinAuto = {"BMW", 2020};
    printf("Modell: %s\n", meinAuto.modell);
    return 0;
}
```

---

## 🧪 Übungsprojekte

Hier sind 10 einfache Projekte, die du in C umsetzen kannst:

### 1. Einfacher Taschenrechner
> Zwei Zahlen eingeben und die Grundrechenarten ausführen.

### 2. Digitale Uhr
> Uhrzeit im Format `HH:MM:SS` anzeigen.

### 3. Notiz-App
> Text vom Benutzer eingeben, speichern und anzeigen.

### 4. Auto-Preis-Schätzer
> Modell eingeben und geschätzten Preis anzeigen.

### 5. Fakultätsberechnung
> Zahl eingeben und Fakultät berechnen.

### 6. Primzahlprüfung
> Zahl eingeben und prüfen, ob sie eine Primzahl ist.

### 7. Temperaturumrechner
> Celsius in Fahrenheit umrechnen.

### 8. Zeichenzähler
> Zeichenanzahl eines Strings zählen.

### 9. Einmaleins-Tabelle
> Multiplikationstabelle von 1 bis 10 ausgeben.

### 10. Einkaufsliste verwalten
> Artikel speichern, hinzufügen und löschen.

---

## 🧠 Fazit

C zu lernen ist wie das Fundament eines Gebäudes zu legen. Mit einem starken Grundverständnis kannst du später komplexe Projekte und andere Sprachen viel leichter meistern. Übe regelmäßig, baue kleine Programme und dokumentiere deinen Code sauber.


---
---


# 📘 Comprehensive Beginner’s Guide to the C Programming Language

---

## 🧠 Introduction

C is one of the most influential and foundational programming languages in computer science. Developed by Dennis Ritchie in 1972, it has shaped the design of many modern languages like C++, Java, Python, and Rust. If you want to learn programming from the ground up, C is the perfect starting point.

---

## 🎯 Why Learn C?

- 🔧 **Deep Understanding of Computers:** C helps you understand how memory, processors, and operating systems work.
- 🚀 **High Performance:** C programs run extremely fast.
- 🧩 **Portability:** C code can run on various operating systems.
- 🧠 **Algorithmic Thinking:** C trains your brain to solve complex problems efficiently.

---

## 🛠️ Setting Up Your Environment

### On Windows:
- Install [Code::Blocks](http://www.codeblocks.org/)
- Or [Dev-C++](https://sourceforge.net/projects/orwelldevcpp/)

### On Linux:
```bash
sudo apt update
sudo apt install gcc
```

### On macOS:
```bash
xcode-select --install
```

---

## 🧱 Basic Structure of a C Program

```c
#include <stdio.h>

int main() {
    printf("Hello, world!\n");
    return 0;
}
```

### Explanation:

| Part | Description |
|------|-------------|
| `#include <stdio.h>` | Imports the standard input/output library |
| `int main()` | Main function where execution starts |
| `printf()` | Prints text to the screen |
| `return 0;` | Ends the program successfully |

---

## 🔤 Data Types in C

| Type | Description | Example |
|------|-------------|---------|
| `int` | Integer | `int age = 25;` |
| `float` | Decimal number | `float pi = 3.14;` |
| `char` | Single character | `char grade = 'A';` |
| `double` | More precise decimal | `double g = 9.81;` |

---

## 📦 Variables and Operators

### Declaring Variables:
```c
int x = 10;
float y = 5.5;
```

### Common Operators:

| Operator | Purpose | Example |
|----------|---------|---------|
| `+` | Addition | `x + y` |
| `-` | Subtraction | `x - y` |
| `*` | Multiplication | `x * y` |
| `/` | Division | `x / y` |
| `%` | Modulus | `x % 3` |

---

## 🔁 Control Structures

### Conditional Statements:
```c
int score = 85;
if (score >= 90) {
    printf("Excellent!\n");
} else if (score >= 70) {
    printf("Good!\n");
} else {
    printf("Keep trying!\n");
}
```

### Loops:

#### For Loop:
```c
for (int i = 0; i < 5; i++) {
    printf("Number: %d\n", i);
}
```

#### While Loop:
```c
int i = 0;
while (i < 5) {
    printf("Number: %d\n", i);
    i++;
}
```

#### Do-While Loop:
```c
int i = 0;
do {
    printf("Number: %d\n", i);
    i++;
} while (i < 5);
```

---

## 🧮 Functions in C

Functions help break your program into reusable blocks.

```c
int sum(int a, int b) {
    return a + b;
}

int main() {
    int result = sum(3, 4);
    printf("Result: %d\n", result);
    return 0;
}
```

---

## 📚 Arrays

Arrays store multiple values of the same type.

```c
int numbers[3] = {10, 20, 30};
printf("Second number: %d\n", numbers[1]);
```

---

## 📌 Pointers

Pointers store memory addresses of variables.

```c
int x = 10;
int *ptr = &x;
printf("Value of x: %d\n", *ptr);
```

| Concept | Description |
|--------|-------------|
| `&x` | Address of variable x |
| `*ptr` | Value stored at the pointer’s address |

---

## 🗂️ Simple Data Structures

### Strings:
```c
char name[] = "Davood";
printf("Name: %s\n", name);
```

### Structs:
```c
struct Car {
    char model[20];
    int year;
};

int main() {
    struct Car myCar = {"BMW", 2020};
    printf("Model: %s\n", myCar.model);
    return 0;
}
```

---

## 🧪 Practice Projects

Here are 10 beginner-friendly projects to help you apply what you've learned. Try writing each one in C.

### 1. Simple Calculator
> Take two numbers and perform addition, subtraction, multiplication, and division.

### 2. Digital Clock
> Display time in `HH:MM:SS` format using loops and delays.

### 3. Note-Taking App
> Accept a string from the user, store it in an array, and print it.

### 4. Car Price Estimator
> Input car model and display an estimated price.

### 5. Factorial Calculator
> Input a number and calculate its factorial using loops or recursion.

### 6. Prime Number Checker
> Input a number and check if it’s prime.

### 7. Temperature Converter
> Convert Celsius to Fahrenheit.

### 8. Character Counter
> Input a string and count the number of characters.

### 9. Multiplication Table
> Print multiplication tables from 1 to 10 using nested loops.

### 10. Shopping List Manager
> Store items in an array and allow adding/removing items.

---

## 🧠 Conclusion

Learning C is like building the foundation of a skyscraper. Once you master the basics, you’ll be ready to explore advanced topics and other languages with confidence. Keep practicing, build projects, and always document your code.


---
---


# 📘 آموزش جامع مقدماتی زبان برنامه‌نویسی C

---

## 🧠 مقدمه

زبان C یکی از مهم‌ترین زبان‌های برنامه‌نویسی در تاریخ کامپیوتر است. این زبان پایه‌ای برای بسیاری از زبان‌های مدرن مانند C++، Java، Python و Rust محسوب می‌شود. اگر می‌خواهی برنامه‌نویسی را اصولی یاد بگیری، C بهترین نقطه شروع است.

---

## 🎯 چرا زبان C را یاد بگیریم؟

- 🔧 **درک عمیق از ساختار کامپیوتر:** با C می‌توانی بفهمی حافظه، پردازنده و سیستم‌عامل چگونه کار می‌کنند.
- 🚀 **سرعت بالا:** برنامه‌های C بسیار سریع اجرا می‌شوند.
- 🧩 **قابل حمل بودن:** کدهای C روی سیستم‌عامل‌های مختلف قابل اجرا هستند.
- 🧠 **تقویت ذهن الگوریتمی:** چون C سطح پایین‌تر از زبان‌های مدرن است، ذهن را برای حل مسائل پیچیده آماده می‌کند.

---

## 🛠️ نصب و راه‌اندازی محیط برنامه‌نویسی

### ویندوز:
- نصب [Code::Blocks](http://www.codeblocks.org/)
- یا [Dev-C++](https://sourceforge.net/projects/orwelldevcpp/)

### لینوکس:
```bash
sudo apt update
sudo apt install gcc
```

### مک:
```bash
xcode-select --install
```

---

## 🧱 ساختار کلی یک برنامه C

```c
#include <stdio.h>

int main() {
    printf("سلام دنیا!\n");
    return 0;
}
```

### توضیح بخش‌ها:

| بخش | توضیح |
|------|-------|
| `#include <stdio.h>` | وارد کردن کتابخانه استاندارد برای ورودی/خروجی |
| `int main()` | تابع اصلی برنامه |
| `printf()` | چاپ متن روی صفحه |
| `return 0;` | پایان موفق برنامه |

---

## 🔤 انواع داده‌ها در C

| نوع داده | توضیح | مثال |
|----------|--------|-------|
| `int` | عدد صحیح | `int age = 25;` |
| `float` | عدد اعشاری | `float pi = 3.14;` |
| `char` | یک کاراکتر | `char grade = 'A';` |
| `double` | عدد اعشاری دقیق‌تر | `double g = 9.81;` |

---

## 📦 متغیرها و عملگرها

### تعریف متغیر:
```c
int x = 10;
float y = 5.5;
```

### عملگرها:

| عملگر | کاربرد | مثال |
|-------|--------|------|
| `+` | جمع | `x + y` |
| `-` | تفریق | `x - y` |
| `*` | ضرب | `x * y` |
| `/` | تقسیم | `x / y` |
| `%` | باقیمانده | `x % 3` |

---

## 🔁 ساختارهای کنترلی

### شرط‌ها:
```c
int score = 85;
if (score >= 90) {
    printf("عالی!\n");
} else if (score >= 70) {
    printf("خوب!\n");
} else {
    printf("نیاز به تلاش بیشتر!\n");
}
```

### حلقه‌ها:

#### حلقه for:
```c
for (int i = 0; i < 5; i++) {
    printf("عدد: %d\n", i);
}
```

#### حلقه while:
```c
int i = 0;
while (i < 5) {
    printf("عدد: %d\n", i);
    i++;
}
```

#### حلقه do-while:
```c
int i = 0;
do {
    printf("عدد: %d\n", i);
    i++;
} while (i < 5);
```

---

## 🧮 توابع در C

توابع برای تقسیم برنامه به بخش‌های کوچک‌تر استفاده می‌شوند.

```c
int sum(int a, int b) {
    return a + b;
}

int main() {
    int result = sum(3, 4);
    printf("نتیجه: %d\n", result);
    return 0;
}
```

---

## 📚 آرایه‌ها

آرایه‌ها مجموعه‌ای از داده‌ها با نوع یکسان هستند.

```c
int numbers[3] = {10, 20, 30};
printf("عدد دوم: %d\n", numbers[1]);
```

---

## 📌 اشاره‌گرها (Pointers)

اشاره‌گرها آدرس حافظه متغیرها را ذخیره می‌کنند.

```c
int x = 10;
int *ptr = &x;
printf("مقدار x: %d\n", *ptr);
```

| مفهوم | توضیح |
|-------|-------|
| `&x` | آدرس متغیر x |
| `*ptr` | مقدار ذخیره‌شده در آدرس اشاره‌گر |

---

## 🗂️ ساختارهای داده‌ای ساده

### رشته‌ها (Strings):
```c
char name[] = "Davood";
printf("نام: %s\n", name);
```

### ساختارها (Structs):
```c
struct Car {
    char model[20];
    int year;
};

int main() {
    struct Car myCar = {"BMW", 2020};
    printf("مدل: %s\n", myCar.model);
    return 0;
}
```

---

## 🧪 تمرین‌ها و پروژه‌های ساده

در ادامه ۱۰ تمرین کاربردی برای تقویت مهارت‌های زبان C آورده شده است. هر تمرین را به صورت یک برنامه بنویسید.

### 1. ماشین‌حساب ساده
> دریافت دو عدد و انجام عملیات جمع، تفریق، ضرب و تقسیم.

### 2. ساعت دیجیتال
> نمایش ساعت با فرمت `HH:MM:SS` با استفاده از حلقه و تأخیر زمانی.

### 3. یادداشت‌برداری
> دریافت متن از کاربر و ذخیره در آرایه، سپس چاپ آن.

### 4. قیمت‌گذار خودرو
> دریافت مدل خودرو و نمایش قیمت تقریبی.

### 5. محاسبه فاکتوریل
> دریافت عدد و محاسبه فاکتوریل با حلقه یا تابع بازگشتی.

### 6. بررسی عدد اول
> دریافت عدد و بررسی اول بودن آن.

### 7. تبدیل دما
> تبدیل دمای سانتی‌گراد به فارنهایت.

### 8. شمارش حروف
> دریافت رشته و شمارش تعداد کاراکترها.

### 9. جدول ضرب
> چاپ جدول ضرب ۱ تا ۱۰ با استفاده از حلقه تو در تو.

### 10. مدیریت لیست خرید
> ذخیره لیست اقلام در آرایه و امکان افزودن یا حذف آیتم‌ها.

---

## 🧠 نتیجه‌گیری

یادگیری زبان C مثل ساختن اسکلت یک ساختمان است. اگر این پایه را محکم بسازی، می‌توانی به راحتی زبان‌های دیگر را یاد بگیری و پروژه‌های حرفه‌ای بسازی. این مقاله فقط شروع راه است. تمرین کن، پروژه بساز، و همیشه کدت را مستندسازی کن.

