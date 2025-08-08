# 🇩🇪 Beschreibung auf Deutsch
---
## 🧮 Umfassender Artikel über NumPy — Die numerische Bibliothek für Python

---

## ✨ Einleitung

NumPy (Numerical Python) ist eine Open-Source-Bibliothek für numerische und wissenschaftliche Berechnungen in Python. Sie bildet die Grundlage für viele andere Bibliotheken wie Pandas, TensorFlow, SciPy und Scikit-learn. NumPy führt komplexe mathematische Operationen schnell und effizient aus.

---

## 🔧 Installation von NumPy

Die Installation erfolgt über pip:

```bash
pip install numpy
```

---

## 🧠 Struktur und Hauptkonzepte

### Array (ndarray)

Das Herzstück von NumPy ist das mehrdimensionale Array `ndarray`, das speichereffizient und leistungsstark verarbeitet wird. Im Gegensatz zu Python-Listen ermöglicht es Vektoroperationen und numerische Berechnungen direkt auf Arrays.

---

## ✏️ Einfaches Array-Beispiel

```python
import numpy as np

a = np.array([1, 2, 3])
print(a)
```

---

## 🔢 Hauptmerkmale von NumPy

- Hohe Geschwindigkeit  
- Geringer Speicherverbrauch  
- Erweiterte mathematische Funktionen  
- Kompatibel mit anderen Bibliotheken  
- Vektoroperationen ohne Schleifen

---

## 🧮 Grundrechenarten

```python
a = np.array([2, 4, 6])
b = np.array([1, 3, 5])

print("Summe:", a + b)
print("Produkt:", a * b)
```

---

## 📐 Mehrdimensionale Arrays und Reshape

```python
m = np.array([[1, 2], [3, 4]])
print("Form:", m.shape)
print("Umformung:", m.reshape(4))
```

---

## 📊 Statistische Funktionen

```python
data = np.array([1, 2, 3, 4, 5])

print("Mittelwert:", np.mean(data))
print("Standardabweichung:", np.std(data))
print("Maximum:", np.max(data))
```

---

## 🔀 Filterung und Indexierung

```python
x = np.array([5, 10, 15, 20])
print("Größer als 10:", x[x > 10])
```

---

## 📦 Spezielle Arrays erzeugen

```python
print("Null-Array:", np.zeros((2, 3)))
print("Einsen-Array:", np.ones((3, 3)))
print("Zufallsarray:", np.random.rand(4))
```

---

## 🧩 Matrixoperationen

```python
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

print("Matrixprodukt:", np.dot(A, B))
```

---

## 🛠 Nützliche Funktionen in NumPy

### linspace und arange

```python
print(np.arange(0, 10, 2))      # [0 2 4 6 8]
print(np.linspace(0, 1, 5))     # [0.  0.25 0.5 0.75 1.]
```

### Bedingte Ersetzungen

```python
arr = np.array([1, 2, 3])
arr[arr < 2] = 100
```

---

## 🧪 Anwendungen in der Praxis

- Bildverarbeitung  
- Wissenschaftliche Datenanalyse  
- Maschinelles Lernen  
- Statistische Modellierung  
- Zeitreihenanalyse

---

## 🎯 Vergleich mit Python-Listen

| Eigenschaft         | NumPy ndarray | Python-Liste |
|---------------------|----------------|--------------|
| Geschwindigkeit      | Sehr hoch      | Mittel        |
| Speicherverbrauch     | Gering         | Hoch          |
| Vektoroperationen     | Ja             | Nein          |
| Numerische Funktionen | Erweitert      | Eingeschränkt |

---

## 🔗 Weiterführende Ressourcen

- [Offizielle Dokumentation von NumPy](https://numpy.org/doc/)
- [Real Python NumPy Guide](https://realpython.com/numpy-array-programming/)
- [Buch: „Python for Data Analysis“ von Wes McKinney]

---

## 🔚 Fazit

NumPy ist eines der grundlegendsten Werkzeuge in den Bereichen Data Science, künstliche Intelligenz, Signalverarbeitung und Statistik. Wenn du Python für wissenschaftliche oder analytische Aufgaben nutzt, ist das Lernen von NumPy ein entscheidender erster Schritt für deinen professionellen Weg.



---



# 🇬🇧 Description in English
---
## 🧮 Comprehensive Guide to NumPy — Python’s Numerical Library

---

## ✨ Introduction

NumPy (Numerical Python) is an open-source library for numerical and scientific computing in Python. It serves as the foundation for many other libraries like Pandas, TensorFlow, SciPy, and Scikit-learn. NumPy performs complex mathematical operations quickly and efficiently.

---

## 🔧 Installing NumPy

You can install it using pip:

```bash
pip install numpy
```

---

## 🧠 Structure and Key Concepts

### Array (ndarray)

The core of NumPy is its multidimensional array object `ndarray`, which is memory-efficient and fast. Unlike Python lists, it enables vectorized operations and numerical calculations directly on arrays.

---

## ✏️ Simple Array Example

```python
import numpy as np

a = np.array([1, 2, 3])
print(a)
```

---

## 🔢 Key Features of NumPy

- High speed  
- Low memory usage  
- Advanced mathematical functions  
- Compatibility with other libraries  
- Vectorized operations without loops

---

## 🧮 Basic Arithmetic

```python
a = np.array([2, 4, 6])
b = np.array([1, 3, 5])

print("Sum:", a + b)
print("Product:", a * b)
```

---

## 📐 Multidimensional Arrays and Reshaping

```python
m = np.array([[1, 2], [3, 4]])
print("Shape:", m.shape)
print("Reshaped:", m.reshape(4))
```

---

## 📊 Statistical Functions

```python
data = np.array([1, 2, 3, 4, 5])

print("Mean:", np.mean(data))
print("Std Dev:", np.std(data))
print("Max:", np.max(data))
```

---

## 🔀 Filtering and Indexing

```python
x = np.array([5, 10, 15, 20])
print("Greater than 10:", x[x > 10])
```

---

## 📦 Creating Special Arrays

```python
print("Zeros:", np.zeros((2, 3)))
print("Ones:", np.ones((3, 3)))
print("Random:", np.random.rand(4))
```

---

## 🧩 Matrix Operations

```python
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

print("Matrix Product:", np.dot(A, B))
```

---

## 🛠 Useful Functions in NumPy

### linspace and arange

```python
print(np.arange(0, 10, 2))      # [0 2 4 6 8]
print(np.linspace(0, 1, 5))     # [0.  0.25 0.5 0.75 1.]
```

### Conditional Replacement

```python
arr = np.array([1, 2, 3])
arr[arr < 2] = 100
```

---

## 🧪 Real-World Applications

- Image processing  
- Scientific data analysis  
- Machine learning  
- Statistical modeling  
- Time series analysis

---

## 🎯 NumPy vs Python Lists

| Feature              | NumPy ndarray | Python List   |
|----------------------|---------------|----------------|
| Speed                | Very high     | Moderate        |
| Memory usage         | Low           | High            |
| Vector operations    | Yes           | No              |
| Numerical functions  | Extensive     | Limited         |

---

## 🔗 Useful Resources

- [NumPy Official Documentation](https://numpy.org/doc/)
- [Real Python NumPy Guide](https://realpython.com/numpy-array-programming/)
- Book: *Python for Data Analysis* by Wes McKinney

---

## 🔚 Conclusion

NumPy is one of the most essential tools in data science, artificial intelligence, signal processing, and statistics. If you're using Python for scientific or analytical tasks, learning NumPy is the key first step on your professional journey.



---



# 🇮🇷 توضیحات به زبان فارسی
---
## 🧮 مقاله جامع درباره NumPy — کتابخانه عددی پایتون

---

## ✨ مقدمه

NumPy (Numerical Python) یک کتابخانه متن‌باز در پایتون است که برای محاسبات عددی و علمی طراحی شده است. این کتابخانه پایه‌ و اساس بسیاری از کتابخانه‌های دیگر مانند Pandas، TensorFlow، SciPy و Scikit-learn است. NumPy عملیات‌های پیچیده ریاضی را با سرعت بالا و بهینه انجام می‌دهد.

---

## 🔧 نصب کتابخانه NumPy

برای نصب می‌توان از pip استفاده کرد:

```bash
pip install numpy
```

---

## 🧠 ساختار و مفهوم اصلی

### آرایه (ndarray)

مرکز اصلی NumPy آرایه‌ی چندبعدی `ndarray` است که به‌صورت بسیار بهینه ذخیره‌سازی و پردازش می‌شود. برخلاف لیست‌های پایتون، ndarray امکان انجام عملیات ریاضی برداری را فراهم می‌کند.

---

## ✏️ تعریف یک آرایه ساده

```python
import numpy as np

a = np.array([1, 2, 3])
print(a)
```

---

## 🔢 ویژگی‌های اصلی NumPy

- سرعت بالا در محاسبات  
- اشغال حافظه کمتر  
- توابع ریاضی پیشرفته (ماتریس، بردار، خطی، آماری)  
- سازگاری با دیگر کتابخانه‌ها  
- عملیات برداری و عدم نیاز به حلقه‌ها

---

## 🧮 عملیات ریاضی پایه

```python
a = np.array([2, 4, 6])
b = np.array([1, 3, 5])

print("جمع:", a + b)
print("ضرب:", a * b)
```

---

## 📐 آرایه‌های چندبعدی و شکل‌دهی

```python
m = np.array([[1, 2], [3, 4]])
print("شکل آرایه:", m.shape)
print("تغییر شکل:", m.reshape(4))
```

---

## 📊 توابع آماری

```python
data = np.array([1, 2, 3, 4, 5])

print("میانگین:", np.mean(data))
print("انحراف معیار:", np.std(data))
print("حداکثر:", np.max(data))
```

---

## 🔀 فیلتر کردن و ایندکس‌گذاری

```python
x = np.array([5, 10, 15, 20])
print("بیشتر از 10:", x[x > 10])
```

---

## 📦 تولید آرایه‌های خاص

```python
print("آرایه صفر:", np.zeros((2, 3)))
print("آرایه یک:", np.ones((3, 3)))
print("آرایه تصادفی:", np.random.rand(4))
```

---

## 🧩 عملیات ماتریسی

```python
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

print("ضرب ماتریسی:", np.dot(A, B))
```

---

## 🛠 ابزارهای کاربردی در NumPy

### توابع linspace و arange

```python
print(np.arange(0, 10, 2))      # [0 2 4 6 8]
print(np.linspace(0, 1, 5))     # [0.  0.25 0.5 0.75 1.]
```

### مقداردهی جایگزین و شرطی

```python
arr = np.array([1, 2, 3])
arr[arr < 2] = 100
```

---

## 🧪 نمونه‌های کاربردی در دنیای واقعی

- پردازش تصاویر  
- تحلیل داده‌های علمی و آزمایشگاهی  
- یادگیری ماشین  
- مدل‌سازی آماری  
- تجزیه‌وتحلیل سری‌های زمانی

---

## 🎯 مقایسه با لیست‌های پایتون

| ویژگی‌ها        | NumPy ndarray | لیست پایتون |
|------------------|----------------|--------------|
| سرعت              | بسیار بالا     | معمولی       |
| حافظه             | کمتر           | بیشتر         |
| عملیات برداری     | دارد            | ندارد         |
| محاسبات عددی     | پیشرفته        | محدود         |

---

## 🔗 منابع یادگیری

- [مستندات رسمی NumPy](https://numpy.org/doc/)
- [Real Python NumPy Guide](https://realpython.com/numpy-array-programming/)
- [کتاب “Python for Data Analysis”]

---

## 🔚 نتیجه‌گیری

NumPy یکی از ضروری‌ترین ابزارها در علم داده، هوش مصنوعی، پردازش سیگنال و تحلیل داده است. اگر پایتون را برای کارهای علمی یا آماری انتخاب کرده‌اید، یادگیری NumPy قدم اول و حیاتی در مسیر حرفه‌ای شماست.