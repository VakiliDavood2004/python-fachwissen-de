# 🇩🇪 Beschreibung auf Deutsch
---
## 🎨 Umfassender Leitfaden zu PyQt — Erstellung moderner grafischer Benutzeroberflächen mit Python

---

## 📍 Was ist PyQt?

**PyQt** ist eine Sammlung von Python-Modulen, die die Qt-Toolkits verwenden, um leistungsstarke grafische Anwendungen zu erstellen. Qt wurde von Trolltech entwickelt und ist eines der beliebtesten Frameworks für Benutzeroberflächen auf Windows, Linux und macOS.

PyQt wird von Riverbank Computing gepflegt und unterstützt sowohl Qt4 als auch Qt5.

---

## 🔧 Installation von PyQt

PyQt5 kannst du mit folgendem Befehl installieren:

```bash
pip install PyQt5
```

Für das grafische Design-Werkzeug Qt Designer:

```bash
pip install pyqt5-tools
```

---

## 🧠 Grundkonzepte in PyQt

- **Widgets**: GUI-Komponenten wie Buttons, Labels, Tabellen, Textfelder etc.  
- **Layouts**: Steuerung der Anordnung von Widgets im Fenster  
- **Signals und Slots**: Mechanismus zur Ereignisverarbeitung zwischen Komponenten  

---

## ✏️ Erstes PyQt-Programm

```python
import sys
from PyQt5.QtWidgets import QApplication, QLabel

app = QApplication(sys.argv)
label = QLabel("Hallo Welt!")
label.show()
sys.exit(app.exec_())
```

---

## 📦 Wichtige GUI-Komponenten

- `QWidget`: Basisklasse für alle Widgets  
- `QMainWindow`: Hauptfenster einer Anwendung  
- `QPushButton`: Schaltfläche  
- `QLineEdit`: Textfeld zur Eingabe  
- `QLabel`: Anzeige von Text  
- `QTableWidget`: Tabellenansicht  
- `QComboBox`: Dropdown-Menü  
- `QCheckBox`: Auswahlfeld  
- `QRadioButton`: Optionsfeld  

---

## 🔁 Layouts zur Anordnung von Widgets

Drei Haupttypen:

- `QVBoxLayout`: Vertikale Anordnung  
- `QHBoxLayout`: Horizontale Anordnung  
- `QGridLayout`: Raster-Layout

```python
from PyQt5.QtWidgets import QWidget, QVBoxLayout, QPushButton

window = QWidget()
layout = QVBoxLayout()

btn1 = QPushButton("Button 1")
btn2 = QPushButton("Button 2")

layout.addWidget(btn1)
layout.addWidget(btn2)

window.setLayout(layout)
window.show()
```

---

## 🔗 Signals und Slots

```python
def on_click():
    print("Button wurde geklickt!")

btn.clicked.connect(on_click)
```

---

## 🎨 Arbeiten mit Qt Designer

Qt Designer ist ein grafisches Tool zum Entwerfen von Benutzeroberflächen. Nach dem Design wird eine `.ui`-Datei erzeugt, die in Python-Code umgewandelt werden kann:

```bash
pyuic5 design.ui -o design.py
```

Danach kannst du den generierten Code direkt in deinem Projekt verwenden.

---

## 📁 Dialoge und Fensterverwaltung

- `QDialog`: Dialogfenster  
- `QMessageBox`: Informationsmeldungen  
- `QFileDialog`: Dateiauswahl  
- `QInputDialog`: Eingabeaufforderungen  

---

## 📂 Anbindung an Datenbanken

Du kannst Datenbanken wie SQLite oder MySQL mit Modulen wie `sqlite3` oder `SQLAlchemy` integrieren. Inhalte lassen sich z. B. im `QTableWidget` anzeigen.

---

## 🧩 Beispielprojekt: Einfache Taschenrechner-App

```python
from PyQt5.QtWidgets import QApplication, QWidget, QPushButton, QVBoxLayout, QLineEdit

class Calculator(QWidget):
    def __init__(self):
        super().__init__()
        self.setWindowTitle("Einfacher Taschenrechner")
        self.layout = QVBoxLayout()
        self.display = QLineEdit()
        self.button = QPushButton("Berechne")
        self.button.clicked.connect(self.calculate)
        self.layout.addWidget(self.display)
        self.layout.addWidget(self.button)
        self.setLayout(self.layout)

    def calculate(self):
        result = eval(self.display.text())
        self.display.setText(str(result))

app = QApplication([])
window = Calculator()
window.show()
app.exec_()
```

---

## 🧪 Übungsideen

> Zum Üben:
>
> - Erstelle ein Registrierungsformular mit Validierung  
> - Design eines Datei-Browsers  
> - Integration eines Pandas-DataFrames in eine GUI-Tabelle  
> - Darstellung von Diagrammen mit Matplotlib in einem PyQt-Fenster  

---

## 🔗 Nützliche Ressourcen

- [Offizielle PyQt5-Dokumentation](https://www.riverbankcomputing.com/software/pyqt/intro)
- [PyQt5 Tutorial bei W3Schools](https://www.w3schools.com/python/python_gui_pyqt.asp)
- [PyQt5 Video-Tutorials auf YouTube](https://www.youtube.com/results?search_query=pyqt5+tutorial)

---

## 🎯 Fazit

PyQt ist ein leistungsfähiges Toolkit zur Erstellung grafischer Anwendungen mit Python. Dank seiner Flexibilität und umfangreichen Komponenten kannst du professionelle Desktop-Anwendungen entwickeln. Der Einstieg ist leicht, und mit etwas Übung kannst du beeindruckende GUIs bauen.




----





# 🇬🇧 Description in English
---
## 🎨 Comprehensive Guide to PyQt — Building Modern Graphical User Interfaces with Python

---

## 📍 What is PyQt?

**PyQt** is a set of Python bindings for the Qt application framework, used to build powerful GUI applications. Originally developed by Trolltech, Qt is one of the most widely used UI frameworks across Windows, Linux, and macOS.

PyQt is maintained by Riverbank Computing and supports both Qt4 and Qt5.

---

## 🔧 Installing PyQt

To install PyQt5:

```bash
pip install PyQt5
```

To get Qt Designer (for drag-and-drop UI design):

```bash
pip install pyqt5-tools
```

---

## 🧠 Core Concepts in PyQt

- **Widgets**: GUI components such as buttons, labels, tables, input fields  
- **Layouts**: Arranging widgets within a window  
- **Signals and Slots**: A communication mechanism to handle events between components  

---

## ✏️ First PyQt Program

```python
import sys
from PyQt5.QtWidgets import QApplication, QLabel

app = QApplication(sys.argv)
label = QLabel("Hello, World!")
label.show()
sys.exit(app.exec_())
```

---

## 📦 Key GUI Components

- `QWidget`: Base class for all widgets  
- `QMainWindow`: Main window of an application  
- `QPushButton`: Button  
- `QLineEdit`: Input field  
- `QLabel`: Text display  
- `QTableWidget`: Table view  
- `QComboBox`: Drop-down menu  
- `QCheckBox`: Checkbox  
- `QRadioButton`: Radio button  

---

## 🔁 Layouts for Widget Arrangement

Three main types:

- `QVBoxLayout`: Vertical layout  
- `QHBoxLayout`: Horizontal layout  
- `QGridLayout`: Grid layout  

```python
from PyQt5.QtWidgets import QWidget, QVBoxLayout, QPushButton

window = QWidget()
layout = QVBoxLayout()

btn1 = QPushButton("Button 1")
btn2 = QPushButton("Button 2")

layout.addWidget(btn1)
layout.addWidget(btn2)

window.setLayout(layout)
window.show()
```

---

## 🔗 Signals and Slots

```python
def on_click():
    print("Button clicked!")

btn.clicked.connect(on_click)
```

---

## 🎨 Working with Qt Designer

Qt Designer allows visual UI design. After designing, a `.ui` file is generated that can be converted to Python code:

```bash
pyuic5 design.ui -o design.py
```

You can then import and use that code in your project.

---

## 📁 Dialogs and Window Management

- `QDialog`: Dialog windows  
- `QMessageBox`: Message alerts  
- `QFileDialog`: File selection  
- `QInputDialog`: Prompt for input  

---

## 📂 Integrating with Databases

You can use SQLite or MySQL with modules like `sqlite3` or `SQLAlchemy`. Data can be shown inside widgets like `QTableWidget`.

---

## 🧩 Sample Project: Simple Calculator App

```python
from PyQt5.QtWidgets import QApplication, QWidget, QPushButton, QVBoxLayout, QLineEdit

class Calculator(QWidget):
    def __init__(self):
        super().__init__()
        self.setWindowTitle("Simple Calculator")
        self.layout = QVBoxLayout()
        self.display = QLineEdit()
        self.button = QPushButton("Calculate")
        self.button.clicked.connect(self.calculate)
        self.layout.addWidget(self.display)
        self.layout.addWidget(self.button)
        self.setLayout(self.layout)

    def calculate(self):
        result = eval(self.display.text())
        self.display.setText(str(result))

app = QApplication([])
window = Calculator()
window.show()
app.exec_()
```

---

## 🧪 Practice Ideas

> To sharpen your PyQt skills:
>
> - Build a registration form with input validation  
> - Design a file browser  
> - Display Pandas DataFrames in a PyQt table  
> - Embed Matplotlib charts inside PyQt windows  

---

## 🔗 Useful Resources

- [Official PyQt5 Documentation](https://www.riverbankcomputing.com/software/pyqt/intro)  
- [PyQt5 Tutorial on W3Schools](https://www.w3schools.com/python/python_gui_pyqt.asp)  
- [PyQt5 YouTube Tutorials](https://www.youtube.com/results?search_query=pyqt5+tutorial)

---

## 🎯 Conclusion

PyQt is a powerful toolkit for building desktop applications using Python. Its flexibility and rich features allow developers to create professional-grade interfaces. Whether you're a beginner or ready for complex projects, PyQt offers endless possibilities.





---





# 🇮🇷 توضیحات به زبان فارسی
---
## 🎨 راهنمای کامل PyQt — ساخت رابط گرافیکی حرفه‌ای در پایتون

---

## 📍 PyQt چیست؟

**PyQt** مجموعه‌ای از ماژول‌های پایتون است که از ابزارک‌های Qt استفاده می‌کنند و به شما امکان می‌دهند تا برنامه‌های گرافیکی قدرتمند بسازید. Qt توسط شرکت Trolltech توسعه داده شده و یکی از محبوب‌ترین ابزارها برای توسعه رابط کاربری در سیستم‌عامل‌های مختلف (Windows، Linux، macOS) است.

PyQt توسط شرکت Riverbank ساخته شده و از نسخه‌های Qt4 و Qt5 پشتیبانی می‌کند.

---

## 🔧 نصب PyQt

برای نصب PyQt5 می‌تونید از دستور زیر استفاده کنید:

```bash
pip install PyQt5
```

برای نصب ابزار طراحی رابط گرافیکی (Qt Designer):

```bash
pip install pyqt5-tools
```

---

## 🧠 مفاهیم اصلی در PyQt

- **Widgets (ویجت‌ها)**: اجزای گرافیکی مثل دکمه، لیبل، فرم، جدول و ...
- **Layouts (چیدمان‌ها)**: نحوه قرارگیری ویجت‌ها در صفحه
- **Signals and Slots (سیگنال و اسلات)**: مکانیزم ارتباط بین رویداد و عمل

---

## ✏️ اولین برنامه با PyQt

```python
import sys
from PyQt5.QtWidgets import QApplication, QLabel

app = QApplication(sys.argv)
label = QLabel("سلام دنیا!")
label.show()
sys.exit(app.exec_())
```

---

## 📦 اجزای اصلی رابط کاربری

- `QWidget`: کلاس پایه برای همه ویجت‌ها  
- `QMainWindow`: پنجره اصلی برنامه  
- `QPushButton`: دکمه  
- `QLineEdit`: کادر ورود متن  
- `QLabel`: نمایش متن  
- `QTableWidget`: جدول داده‌ای  
- `QComboBox`: منوی کشویی  
- `QCheckBox`: چک‌باکس  
- `QRadioButton`: دکمه رادیویی  

---

## 🔁 چیدمان ویجت‌ها

سه نوع اصلی چیدمان وجود دارد:

- `QVBoxLayout`: چیدمان عمودی  
- `QHBoxLayout`: چیدمان افقی  
- `QGridLayout`: چیدمان جدولی  

```python
from PyQt5.QtWidgets import QWidget, QVBoxLayout, QPushButton

window = QWidget()
layout = QVBoxLayout()

btn1 = QPushButton("دکمه ۱")
btn2 = QPushButton("دکمه ۲")

layout.addWidget(btn1)
layout.addWidget(btn2)

window.setLayout(layout)
window.show()
```

---

## 🔗 سیگنال و اسلات

```python
def on_click():
    print("دکمه کلیک شد!")

btn.clicked.connect(on_click)
```

---

## 🎨 استفاده از Qt Designer

Qt Designer ابزاری گرافیکی برای طراحی ویجت‌هاست. پس از طراحی رابط، فایل `.ui` تولید می‌شود که قابل تبدیل به کد پایتون است:

```bash
pyuic5 mydesign.ui -o mydesign.py
```

سپس می‌تونید از این طراحی در برنامه استفاده کنید.

---

## 📁 مدیریت پنجره‌ها و دیالوگ‌ها

- `QDialog`: دیالوگ‌ها برای هشدار یا گرفتن ورودی  
- `QMessageBox`: پیام‌نمای ساده  
- `QFileDialog`: انتخاب فایل  
- `QInputDialog`: دریافت ورودی از کاربر

---

## 📂 اتصال به پایگاه‌داده

می‌تونید با استفاده از ماژول‌هایی مانند `sqlite3` یا `SQLAlchemy` پایگاه‌داده‌ها رو به رابط گرافیکی متصل کنید و داده‌ها را در ویجت‌هایی مثل `QTableWidget` نمایش دهید.

---

## 🧩 پروژه نمونه: ماشین حساب

```python
from PyQt5.QtWidgets import QApplication, QWidget, QPushButton, QVBoxLayout, QLineEdit

class Calculator(QWidget):
    def __init__(self):
        super().__init__()
        self.setWindowTitle("ماشین حساب ساده")
        self.layout = QVBoxLayout()
        self.display = QLineEdit()
        self.button = QPushButton("محاسبه")
        self.button.clicked.connect(self.calculate)
        self.layout.addWidget(self.display)
        self.layout.addWidget(self.button)
        self.setLayout(self.layout)

    def calculate(self):
        result = eval(self.display.text())
        self.display.setText(str(result))

app = QApplication([])
window = Calculator()
window.show()
app.exec_()
```

---

## 🧪 تمرین‌های پیشنهادی

> برای تمرین بیشتر:
>
> - ساخت فرم ثبت‌نام با اعتبارسنجی  
> - طراحی پنجره جستجوی فایل‌ها  
> - اتصال دیتافریم Pandas به جدول گرافیکی  
> - نمایش نمودار با matplotlib در PyQt  

---

## 🔗 منابع آموزشی

- [مستند رسمی PyQt5](https://www.riverbankcomputing.com/software/pyqt/intro)
- [PyQt5 در W3Schools](https://www.w3schools.com/python/python_gui_pyqt.asp)
- [آموزش‌های ویدیویی PyQt در YouTube](https://www.youtube.com/results?search_query=pyqt5+tutorial)

---

## 🎯 نتیجه‌گیری

PyQt یک ابزار قدرتمند برای ساخت برنامه‌های گرافیکی در پایتونه که در کنار قابلیت‌های زیبا و حرفه‌ای، به شما اجازه می‌ده رابط‌هایی انعطاف‌پذیر و تعاملی بسازید. با یادگیری PyQt می‌تونی اپلیکیشن‌های دسکتاپ واقعی طراحی کنی و وارد دنیای توسعه نرم‌افزار حرفه‌ای بشی.