# 🇩🇪 Abschnitt Vier: Datenverarbeitung in Python (Python Datenverarbeitung)

In der heutigen digitalen Welt sind Daten der Treibstoff für intelligente Entscheidungen. Von der Analyse des Nutzerverhaltens bis zur Verkaufsprognose hängt alles von Daten ab. Python ist mit seinen leistungsstarken Bibliotheken eine der besten Sprachen für die Datenverarbeitung.

---

## 🧠 Was ist Datenverarbeitung und warum ist sie wichtig?

Datenverarbeitung bedeutet, Rohdaten in verständliche und nutzbare Informationen umzuwandeln. Dieser Prozess umfasst folgende Schritte:

- **Datenerfassung**: Aus verschiedenen Quellen wie Dateien, Datenbanken, APIs, Webseiten und Sensoren  
- **Datenbereinigung**: Entfernen unvollständiger Daten, Korrektur von Fehlern, Standardisierung von Formaten  
- **Datenumwandlung**: Umwandlung in analysierbare Formate wie Tabellen oder JSON  
- **Datenanalyse**: Mustererkennung, statistische Berechnungen, Visualisierung  
- **Speichern oder Präsentieren der Ergebnisse**: Speicherung in Dateien, Datenbanken oder Anzeige in Dashboards

### 🎯 Anwendungsbeispiele der Datenverarbeitung:

- Analyse des Kundenverhaltens in Online-Shops  
- Bewertung der finanziellen Leistung von Unternehmen  
- Wettervorhersage mit Sensordaten  
- Analyse von sozialen Netzwerken und Trends  
- Aufbau von Machine-Learning-Modellen zur Krankheitsdiagnose

---

## 🧰 Datenverarbeitungs-Tools in Python

Python bietet eine Vielzahl von Tools zur Datenverarbeitung. Die folgende Tabelle zeigt die wichtigsten Bibliotheken und ihre Einsatzbereiche:

| Bibliothek       | Zweck                                  | Niveau       |
|------------------|-----------------------------------------|--------------|
| `csv`            | Lesen und Schreiben von CSV-Dateien     | Basis        |
| `json`           | Verarbeitung von JSON-Daten             | Basis        |
| `pandas`         | Tabellarische und analytische Datenverarbeitung | Fortgeschritten |
| `numpy`          | Numerische und Matrixberechnungen       | Fortgeschritten |
| `matplotlib` / `seaborn` | Datenvisualisierung             | Mittelstufe  |
| `openpyxl`       | Arbeiten mit Excel-Dateien              | Mittelstufe  |
| `sqlite3`        | Verbindung zu SQLite-Datenbanken        | Mittelstufe  |
| `requests`       | Datenabruf von APIs                     | Mittelstufe  |
| `beautifulsoup4` | Datenextraktion aus Webseiten (Web Scraping) | Fortgeschritten |

---

## 📂 Daten aus verschiedenen Quellen lesen

### 1. Textdatei:

```python
with open("data.txt", "r", encoding="utf-8") as file:
    lines = file.readlines()
    for line in lines:
        print(line.strip())
```

🔹 Tipp: Für große Dateien verwende `readline()` oder zeilenweise Verarbeitung, um den Speicherverbrauch zu reduzieren.

### 2. CSV-Datei mit pandas:

```python
import pandas as pd

df = pd.read_csv("data.csv")
print(df.head())
```

🔹 Tipp: Parameter wie `sep`, `encoding`, `usecols` ermöglichen eine genauere Steuerung beim Einlesen.

### 3. Excel-Datei:

```python
df = pd.read_excel("data.xlsx", sheet_name="Sheet1")
```

🔹 Tipp: Für Dateien mit mehreren Sheets verwende `sheet_name=None`, um alle Sheets zu laden.

### 4. JSON-Datei:

```python
import json

with open("data.json", "r") as file:
    data = json.load(file)
```

🔹 Tipp: JSON-Daten sind oft verschachtelt; verwende `json_normalize`, um sie in ein DataFrame umzuwandeln.

### 5. Daten von einer API abrufen:

```python
import requests

response = requests.get("https://api.example.com/data")
data = response.json()
```

🔹 Tipp: Für APIs mit Authentifizierung verwende `headers` oder `token`.

---

## 🧹 Datenbereinigung

Die Datenbereinigung ist einer der wichtigsten Schritte der Verarbeitung. Reale Daten sind oft unvollständig, fehlerhaft oder inkonsistent.

### Fehlende Werte prüfen:

```python
print(df.isnull().sum())
```

### Unvollständige Zeilen entfernen:

```python
df = df.dropna()
```

🔹 Tipp: Du kannst nur Zeilen entfernen, bei denen bestimmte Spalten fehlen:

```python
df = df[df["Email"].notnull()]
```

### Fehlende Werte ersetzen:

```python
df["City"] = df["City"].fillna("Unbekannt")
```

### Doppelte Daten entfernen:

```python
df = df.drop_duplicates()
```

### Datentypen konvertieren:

```python
df["Date"] = pd.to_datetime(df["Date"])
df["Price"] = df["Price"].astype(float)
```

🔹 Tipp: Die Konvertierung von Datentypen ist für statistische Analysen und Diagramme unerlässlich.

---

## ✂️ Daten auswählen und filtern

### Spalte auswählen:

```python
names = df["Name"]
```

### Mehrere Spalten auswählen:

```python
subset = df[["Name", "Age", "City"]]
```

### Filtern mit Bedingungen:

```python
adults = df[df["Age"] >= 18]
```

### Kombiniertes Filtern:

```python
filtered = df[(df["Age"] > 25) & (df["City"] == "Teheran")]
```

🔹 Tipp: Verwende Funktionen wie `isin`, `str.contains`, `between` für komplexere Filter.

---

## 📈 Gruppierung und statistische Analyse

### Gruppierung:

```python
grouped = df.groupby("Category")
print(grouped["Price"].mean())
```

### Statistische Berechnungen:

```python
print(df["Price"].mean())
print(df["Price"].median())
print(df["Price"].std())
```

### Werte zählen:

```python
print(df["City"].value_counts())
```

🔹 Tipp: Verwende `describe()`, um die Datenverteilung zu analysieren:

```python
print(df.describe())
```

---

## 📊 Datenvisualisierung

### Balkendiagramm:

```python
import matplotlib.pyplot as plt

df["City"].value_counts().plot(kind="bar", color="skyblue")
plt.title("Anzahl der Kunden pro Stadt")
plt.xlabel("Stadt")
plt.ylabel("Anzahl")
plt.grid(True)
plt.show()
```

### Kreisdiagramm:

```python
df["Category"].value_counts().plot(kind="pie", autopct="%1.1f%%")
plt.title("Anteil der Kategorien")
plt.ylabel("")
plt.show()
```

🔹 Tipp: Für professionellere Diagramme verwende `seaborn`:

```python
import seaborn as sns

sns.boxplot(x="Category", y="Price", data=df)
```

---

## 🛒 Praxisprojekt: Verkaufsanalyse im Geschäft

### Die Datei `sales.csv` enthält:

- `Product`  
- `Category`  
- `Price`  
- `Quantity`  
- `Date`

### Projektschritte:

1. Datei einlesen  
2. Gesamtumsatz pro Produkt berechnen  
3. Nach Kategorie gruppieren  
4. Monatliche Verkäufe analysieren  
5. Verkäufe visualisieren  
6. Ergebnisse in neuer Datei speichern

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("sales.csv")
df["Total"] = df["Price"] * df["Quantity"]
df["Date"] = pd.to_datetime(df["Date"])

monthly_sales = df.groupby(df["Date"].dt.to_period("M"))["Total"].sum()
monthly_sales.plot(kind="line", marker="o", color="green")
plt.title("Monatliche Verkäufe")
plt.ylabel("Toman")
plt.xlabel("Monat")
plt.grid(True)
plt.show()

df.to_csv("sales_clean.csv", index=False)
```

---

## 🧪 Fortgeschrittene Übungen

1. Saisonale Verkäufe mit `dt.month` analysieren  
2. Korrelation zwischen Preis und verkaufter Menge mit `corr()` prüfen  
3. Einfaches Dashboard mit Streamlit erstellen  
4. Verbindung zu SQLite-Datenbank herstellen und Abfragen ausführen  
5. Live-Wetterdaten von einer API abrufen und Temperatur darstellen  
6. Daten aus HTML mit BeautifulSoup extrahieren  
7. Heatmap für Korrelationsmatrix erstellen

---

## 📚 Weiterführende Lernressourcen

Um ein Profi in der Datenverarbeitung mit Python zu werden, empfehle ich folgende Ressourcen. Sie eignen sich sowohl für Einsteiger als auch für Fortgeschrittene.

### 🔹 Empfohlene Bücher

- **Python for Data Analysis** von Wes McKinney  
  Ein Klassiker und sehr praxisnahes Buch vom Erfinder von pandas. Enthält reale Beispiele, praktische Projekte und klare Erklärungen.

- **Data Science from Scratch** von Joel Grus  
  Ideal zum Erlernen der Grundlagen der Datenwissenschaft mit Python. Behandelt Statistik, Visualisierung und Machine-Learning-Algorithmen.

- **Effective Pandas** von Matt Harrison  
  Ein Leitfaden für sauberen, schnellen und effizienten pandas-Code. Perfekt für Fortgeschrittene.

---

### 🔹 Offizielle Dokumentation und Online-Ressourcen

- [pandas Dokumentation](https://pandas.pydata.org/docs)  
  Die umfassendste Quelle für pandas-Funktionen, Klassen und Methoden mit Beispielen.

- [NumPy Dokumentation](https://numpy.org/doc)  
  Ideal für numerische Berechnungen, Matrizen und Arrays.

- [matplotlib Dokumentation](https://matplotlib.org/stable/contents.html)  
  Für professionelle Diagramme und deren Anpassung.

- [Python Dokumentation](https://docs.python.org/3/)  
  Die Hauptreferenz für die Programmiersprache Python und alle Standardbibliotheken.

---

### 🔹 Online-Lernplattformen

- **DataCamp**  
  Interaktive Kurse zu pandas, NumPy, Visualisierung und Projekten. Ideal für schrittweises Lernen.

- **Coursera – Python for Data Science von IBM**  
  Umfassender Kurs mit praktischen Übungen, Projekten und anerkanntem Zertifikat.

- **Udemy – Complete Python Data Science Bootcamp**  
  Vollständiger Kurs von Anfänger bis Fortgeschrittene mit pandas, matplotlib, seaborn und Praxisprojekten.

- **Kaggle Learn**  
  Kostenlose Plattform mit kurzen Übungen und echten Datensätzen. Du kannst auch an Wettbewerben teilnehmen.

---

### 🔹 Übungs- und Projektplattformen

- [Google Colab](https://colab.research.google.com)  
  Kostenloses Cloud-Umfeld zum Ausführen von Python-Code. Ideal für Übung, Teilen und große Projekte ohne Installation.

- [Jupyter Notebook](https://jupyter.org)  
  Interaktive Umgebung für Code, Erklärungen und Visualisierungen in einer Datei. Sehr beliebt in der Datenwissenschaft.

- [Streamlit](https://streamlit.io)  
  Tool zum Erstellen von Dashboards und datengetriebenen Apps mit wenigen Codezeilen.

---

## ❓ Fragen zu Abschnitt Vier: Datenverarbeitung in Python

In diesem Abschnitt haben wir Konzepte und Tools zur Datenverarbeitung mit Python kennengelernt. Zur Vertiefung beantworte bitte folgende Fragen:

### 1️⃣ Was ist der Unterschied zwischen Python-Listen und NumPy-Arrays?
- Nenne Unterschiede in Leistung, Geschwindigkeit und Datentypen.

### 2️⃣ Wie kann man Daten aus einer CSV-Datei mit pandas laden und filtern?
- Gib ein Beispiel mit `read_csv()` und einem Filter mit `DataFrame`.

### 3️⃣ Was ist der Unterschied zwischen den Methoden `apply()` und `map()` in pandas?
- Erkläre die Verwendung beider mit einem Beispiel.

### 4️⃣ Wie erkennt und behandelt man fehlende Werte in pandas?
- Nenne Methoden wie `isnull()`, `dropna()` und `fillna()`.

### 5️⃣ In welchen Situationen ist NumPy besser geeignet als pandas für die Datenverarbeitung?
- Nenne Aspekte wie Datentypen, Datenvolumen und numerische Operationen.

---

## ✅ Abschließendes Fazit

Datenverarbeitung mit Python ist nicht nur eine technische Fähigkeit – sie ist die Brücke zwischen Rohdaten und intelligenten Entscheidungen. Mit Tools wie `pandas`, `numpy`, `matplotlib` und `json` kannst du Daten lesen, bereinigen, analysieren und in aussagekräftige Erkenntnisse verwandeln.

In diesem Artikel haben wir gelernt:

- Wie man Daten aus verschiedenen Quellen liest und speichert  
- Wie man unvollständige oder fehlerhafte Daten bereinigt  
- Wie man Datensätze filtert, gruppiert und analysiert  
- Wie man Ergebnisse durch klare und informative Diagramme visualisiert  
- Wie man Python auf reale Projekte wie Verkaufsanalysen anwendet

🔍 Die wichtigste Erkenntnis: Meisterschaft in der Datenverarbeitung kommt durch Übung und Erfahrung. Jeder Datensatz enthält eine verborgene Geschichte – und mit den Tools von Python kannst du sie entdecken und erzählen.

Wenn du gerade erst anfängst, keine Sorge. Die Reise zum Lernen von Python für die Datenverarbeitung ist voller großartiger Ressourcen, spannender Projekte und einer lebendigen Community. Alles, was du brauchst, ist Neugier – und die Bereitschaft, jeden Tag einen Schritt weiterzugehen.




---




# 🇬🇧 Section Four: Data Processing in Python (Python Datenverarbeitung)

In today’s digital world, data is the fuel that powers decision-making. From analyzing user behavior to forecasting sales, everything depends on data. Python, with its powerful libraries, is one of the best languages for data processing.

---

## 🧠 What Is Data Processing and Why Is It Important?

Data processing means transforming raw data into understandable and usable information. This process includes the following steps:

- **Data Collection**: From various sources such as files, databases, APIs, web pages, and sensors  
- **Data Cleaning**: Removing incomplete data, correcting errors, standardizing formats  
- **Data Transformation**: Converting data into analyzable formats like tables or JSON  
- **Data Analysis**: Extracting patterns, statistical calculations, visualization  
- **Storing or Presenting Results**: Saving to files, databases, or displaying in dashboards

### 🎯 Real-World Applications of Data Processing:

- Analyzing customer behavior in online stores  
- Evaluating financial performance of companies  
- Weather forecasting using sensor data  
- Analyzing social media and trends  
- Building machine learning models for disease detection

---

## 🧰 Data Processing Tools in Python

Python offers a wide range of tools for data processing. The table below shows the most important libraries and their use cases:

| Library         | Purpose                            | Level     |
|----------------|-------------------------------------|-----------|
| `csv`           | Reading and writing CSV files       | Basic     |
| `json`          | Processing JSON data                | Basic     |
| `pandas`        | Tabular and analytical data handling| Advanced  |
| `numpy`         | Numerical and matrix computations   | Advanced  |
| `matplotlib` / `seaborn` | Data visualization         | Intermediate |
| `openpyxl`      | Working with Excel files            | Intermediate |
| `sqlite3`       | Connecting to SQLite databases      | Intermediate |
| `requests`      | Fetching data from APIs             | Intermediate |
| `beautifulsoup4`| Extracting data from web pages (Web Scraping) | Advanced |

---

## 📂 Reading Data from Various Sources

### 1. Text File:

```python
with open("data.txt", "r", encoding="utf-8") as file:
    lines = file.readlines()
    for line in lines:
        print(line.strip())
```

🔹 Tip: For large files, use `readline()` or line-by-line processing to reduce memory usage.

### 2. CSV File with pandas:

```python
import pandas as pd

df = pd.read_csv("data.csv")
print(df.head())
```

🔹 Tip: You can use parameters like `sep`, `encoding`, `usecols` for more control over reading.

### 3. Excel File:

```python
df = pd.read_excel("data.xlsx", sheet_name="Sheet1")
```

🔹 Tip: For multi-sheet files, use `sheet_name=None` to read all sheets.

### 4. JSON File:

```python
import json

with open("data.json", "r") as file:
    data = json.load(file)
```

🔹 Tip: JSON data often has nested structures; use `json_normalize` to convert it into a DataFrame.

### 5. Fetching Data from an API:

```python
import requests

response = requests.get("https://api.example.com/data")
data = response.json()
```

🔹 Tip: For APIs requiring authentication, use `headers` or `token`.

---

## 🧹 Data Cleaning

Data cleaning is one of the most important steps in processing. Real-world data is often incomplete, incorrect, or inconsistent.

### Checking for Missing Values:

```python
print(df.isnull().sum())
```

### Removing Incomplete Rows:

```python
df = df.dropna()
```

🔹 Tip: You can remove rows only where specific columns are missing:

```python
df = df[df["Email"].notnull()]
```

### Replacing Missing Values:

```python
df["City"] = df["City"].fillna("Unknown")
```

### Removing Duplicate Data:

```python
df = df.drop_duplicates()
```

### Converting Data Types:

```python
df["Date"] = pd.to_datetime(df["Date"])
df["Price"] = df["Price"].astype(float)
```

🔹 Tip: Converting data types is essential for statistical analysis and charting.

---

## ✂️ Selecting and Filtering Data

### Selecting a Column:

```python
names = df["Name"]
```

### Selecting Multiple Columns:

```python
subset = df[["Name", "Age", "City"]]
```

### Filtering with Conditions:

```python
adults = df[df["Age"] >= 18]
```

### Combined Filtering:

```python
filtered = df[(df["Age"] > 25) & (df["City"] == "Tehran")]
```

🔹 Tip: Use conditional functions like `isin`, `str.contains`, `between` for more complex filters.

---

## 📈 Grouping and Statistical Analysis

### Grouping:

```python
grouped = df.groupby("Category")
print(grouped["Price"].mean())
```

### Statistical Calculations:

```python
print(df["Price"].mean())
print(df["Price"].median())
print(df["Price"].std())
```

### Counting Values:

```python
print(df["City"].value_counts())
```

🔹 Tip: Use `describe()` to analyze data distribution:

```python
print(df.describe())
```

---

## 📊 Data Visualization

### Bar Chart:

```python
import matplotlib.pyplot as plt

df["City"].value_counts().plot(kind="bar", color="skyblue")
plt.title("Number of Customers per City")
plt.xlabel("City")
plt.ylabel("Count")
plt.grid(True)
plt.show()
```

### Pie Chart:

```python
df["Category"].value_counts().plot(kind="pie", autopct="%1.1f%%")
plt.title("Category Share")
plt.ylabel("")
plt.show()
```

🔹 Tip: For more professional charts, use `seaborn`:

```python
import seaborn as sns

sns.boxplot(x="Category", y="Price", data=df)
```

---

## 🛒 Practical Project: Store Sales Analysis

### The `sales.csv` file includes:

- `Product`  
- `Category`  
- `Price`  
- `Quantity`  
- `Date`

### Project Steps:

1. Read the file  
2. Calculate total sales per product  
3. Group by category  
4. Analyze monthly sales  
5. Visualize sales  
6. Save results to a new file

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("sales.csv")
df["Total"] = df["Price"] * df["Quantity"]
df["Date"] = pd.to_datetime(df["Date"])

monthly_sales = df.groupby(df["Date"].dt.to_period("M"))["Total"].sum()
monthly_sales.plot(kind="line", marker="o", color="green")
plt.title("Monthly Sales")
plt.ylabel("Toman")
plt.xlabel("Month")
plt.grid(True)
plt.show()

df.to_csv("sales_clean.csv", index=False)
```

---

## 🧪 Advanced Exercises

1. Analyze seasonal sales using `dt.month`  
2. Check correlation between price and quantity sold using `corr()`  
3. Build a simple dashboard with Streamlit  
4. Connect to an SQLite database and run queries  
5. Fetch live weather data from an API and plot temperature  
6. Extract data from HTML using BeautifulSoup  
7. Create a heatmap for the correlation matrix

---

## 📚 Further Learning Resources

To become a professional in data processing with Python, I recommend the following resources. These are suitable for both beginners and those aiming for advanced levels.

### 🔹 Recommended Books

- **Python for Data Analysis** by Wes McKinney  
  A classic and highly practical book written by the creator of pandas. Includes real-world examples, hands-on projects, and clear explanations of data processing concepts.

- **Data Science from Scratch** by Joel Grus  
  Perfect for learning data science fundamentals with Python. Covers statistics, visualization, and machine learning algorithms.

- **Effective Pandas** by Matt Harrison  
  A guide to writing clean, fast, and efficient pandas code. Ideal for those familiar with pandas who want to level up.

---

### 🔹 Official Documentation and Online Resources

- [pandas documentation](https://pandas.pydata.org/docs)  
  The most complete source for learning pandas functions, classes, and methods with detailed examples.

- [NumPy documentation](https://numpy.org/doc)  
  Great for numerical computations, matrices, and arrays.

- [matplotlib documentation](https://matplotlib.org/stable/contents.html)  
  For creating professional charts and customizing them.

- [Python documentation](https://docs.python.org/3/)  
  The main reference for the Python language, including all standard libraries.

---

### 🔹 Online Learning Platforms

- **DataCamp**  
  Interactive courses on pandas, NumPy, visualization, and real-world projects. Great for step-by-step learning.

- **Coursera – Python for Data Science by IBM**  
  A comprehensive course with hands-on exercises, real projects, and a recognized certificate.

- **Udemy – Complete Python Data Science Bootcamp**  
  A full course from beginner to advanced, covering pandas, matplotlib, seaborn, and practical projects.

- **Kaggle Learn**  
  A free platform for learning with short exercises and real datasets. You can also compete with others using real data.

---

### 🔹 Practice Tools and Project-Based Platforms

- [Google Colab](https://colab.research.google.com)  
  A free cloud-based environment for running Python code. Great for practice, sharing, and running heavy projects without installation.

- [Jupyter Notebook](https://jupyter.org)  
  An interactive environment for writing code, explanations, and visualizations in one file. Very popular in data science.

- [Streamlit](https://streamlit.io)  
  A tool for building dashboards and data-driven apps with Python using just a few lines of code.

---

## ❓ Section Four Questions: Data Processing in Python

In this section, we explored the concepts and tools for data processing in Python. To reinforce your learning, answer the following questions:

### 1️⃣ What is the difference between Python lists and NumPy arrays?
- Mention differences in performance, speed, and data types.

### 2️⃣ How can you load and filter data from a CSV file using pandas?
- Provide an example using `read_csv()` and `DataFrame` with a filter condition.

### 3️⃣ What is the difference between `apply()` and `map()` methods in pandas?
- Explain the use of each with an example.

### 4️⃣ How can you detect and handle missing values in pandas?
- Refer to methods like `isnull()`, `dropna()`, and `fillna()`.

### 5️⃣ In what situations is using NumPy better than pandas for data processing?
- Mention data types, data volume, and need for numerical operations.

---

## ✅ Final Conclusion

Data processing in Python is not just a technical skill; it’s a bridge between raw data and intelligent decision-making. By learning tools like `pandas`, `numpy`, `matplotlib`, and `json`, you can read, clean, analyze, and transform data into meaningful insights.

In this article, we learned:

- How to read and store data from various sources  
- How to clean incomplete or incorrect data  
- How to filter, group, and analyze datasets  
- How to visualize results through clear and informative charts  
- How to apply Python to real-world projects like sales analysis

🔍 The key takeaway is that mastering data processing comes through practice and deep experience. Every dataset you open holds a hidden story—and with Python’s tools, you can uncover and tell that story.

If you’re just starting out, don’t worry. The journey of learning Python for data processing is full of great resources, exciting projects, and a vibrant community. All you need is curiosity—and the commitment to take one step forward each day.



---



# 🇮🇷 بخش چهارم: پردازش داده‌ها در پایتون (Python Datenverarbeitung)

در دنیای دیجیتال امروز، داده‌ها مثل سوخت موتور تصمیم‌گیری هستند. از تحلیل رفتار کاربران گرفته تا پیش‌بینی فروش، همه‌چیز به داده وابسته است. پایتون با کتابخانه‌های قدرتمندش، یکی از بهترین زبان‌ها برای پردازش داده‌هاست.

---

## 🧠 پردازش داده چیست و چرا اهمیت دارد؟

پردازش داده یعنی تبدیل داده‌های خام به اطلاعات قابل فهم و قابل استفاده. این فرآیند شامل مراحل زیر است:

- **جمع‌آوری داده‌ها**: از منابع مختلف مثل فایل‌ها، پایگاه داده‌ها، APIها، صفحات وب و حسگرها  
- **پاک‌سازی داده‌ها**: حذف داده‌های ناقص، اصلاح خطاها، استانداردسازی فرمت‌ها  
- **تغییر ساختار داده‌ها**: تبدیل داده‌ها به فرمت‌های قابل تحلیل مثل جدول یا JSON  
- **تحلیل داده‌ها**: استخراج الگوها، محاسبات آماری، مصورسازی  
- **ذخیره‌سازی یا ارائه نتایج**: ذخیره در فایل، پایگاه داده یا نمایش در داشبورد

### 🎯 کاربردهای واقعی پردازش داده:
 
- تحلیل رفتار مشتریان در فروشگاه‌های آنلاین  
- بررسی عملکرد مالی شرکت‌ها  
- پیش‌بینی آب‌وهوا با داده‌های سنسورها  
- تحلیل شبکه‌های اجتماعی و ترندها  
- ساخت مدل‌های یادگیری ماشین برای تشخیص بیماری‌ها

---

## 🧰 ابزارهای پردازش داده در پایتون

پایتون ابزارهای متنوعی برای پردازش داده دارد. در جدول زیر، مهم‌ترین کتابخانه‌ها را با کاربردشان می‌بینی:

| کتابخانه | کاربرد | سطح |
|----------|--------|------|
| `csv` | خواندن و نوشتن فایل‌های CSV | پایه |
| `json` | پردازش داده‌های JSON | پایه |
| `pandas` | پردازش داده‌های جدولی و تحلیلی | پیشرفته |
| `numpy` | محاسبات عددی و ماتریسی | پیشرفته |
| `matplotlib` / `seaborn` | مصورسازی داده‌ها | متوسط |
| `openpyxl` | کار با فایل‌های Excel | متوسط |
| `sqlite3` | اتصال به پایگاه داده SQLite | متوسط |
| `requests` | دریافت داده از API | متوسط |
| `beautifulsoup4` | استخراج داده از صفحات وب (Web Scraping) | پیشرفته |

---

## 📂 خواندن داده‌ها از منابع مختلف

### 1. فایل متنی:

```python
with open("data.txt", "r", encoding="utf-8") as file:
    lines = file.readlines()
    for line in lines:
        print(line.strip())
```

🔹 نکته: برای فایل‌های بزرگ، بهتر است از `readline()` یا پردازش خط‌به‌خط استفاده شود تا حافظه مصرفی کاهش یابد.

### 2. فایل CSV با pandas:

```python
import pandas as pd

df = pd.read_csv("data.csv")
print(df.head())
```

🔹 نکته: می‌توان از پارامترهایی مثل `sep`, `encoding`, `usecols` برای کنترل دقیق‌تر خواندن استفاده کرد.

### 3. فایل Excel:

```python
df = pd.read_excel("data.xlsx", sheet_name="Sheet1")
```

🔹 نکته: برای فایل‌های چند شیت، می‌توان از `sheet_name=None` استفاده کرد تا همه‌ی شیت‌ها خوانده شوند.

### 4. فایل JSON:

```python
import json

with open("data.json", "r") as file:
    data = json.load(file)
```

🔹 نکته: داده‌های JSON معمولاً ساختار تو در تو دارند؛ برای تبدیل آن‌ها به DataFrame باید از `json_normalize` استفاده کرد.

### 5. دریافت داده از API:

```python
import requests

response = requests.get("https://api.example.com/data")
data = response.json()
```

🔹 نکته: برای APIهایی که نیاز به احراز هویت دارند، باید از `headers` یا `token` استفاده کرد.

---

## 🧹 پاک‌سازی داده‌ها

پاک‌سازی داده‌ها یکی از مهم‌ترین مراحل پردازش است. داده‌های واقعی معمولاً ناقص، نادرست یا ناسازگار هستند.

### بررسی مقادیر خالی:

```python
print(df.isnull().sum())
```

### حذف ردیف‌های ناقص:

```python
df = df.dropna()
```

🔹 نکته: می‌توان فقط ردیف‌هایی را حذف کرد که مقدار خاصی خالی دارند:

```python
df = df[df["Email"].notnull()]
```

### جایگزینی مقادیر خالی:

```python
df["City"] = df["City"].fillna("نامشخص")
```

### حذف داده‌های تکراری:

```python
df = df.drop_duplicates()
```

### تبدیل نوع داده‌ها:

```python
df["Date"] = pd.to_datetime(df["Date"])
df["Price"] = df["Price"].astype(float)
```

🔹 نکته: تبدیل نوع داده‌ها برای تحلیل آماری و رسم نمودار ضروری است.

---

## ✂️ انتخاب و فیلتر داده‌ها

### انتخاب ستون:

```python
names = df["Name"]
```

### انتخاب چند ستون:

```python
subset = df[["Name", "Age", "City"]]
```

### فیلتر با شرط:

```python
adults = df[df["Age"] >= 18]
```

### فیلتر ترکیبی:

```python
filtered = df[(df["Age"] > 25) & (df["City"] == "تهران")]
```

🔹 نکته: می‌توان از توابع شرطی مثل `isin`, `str.contains`, `between` برای فیلترهای پیچیده‌تر استفاده کرد.

---

## 📈 گروه‌بندی و تحلیل آماری

### گروه‌بندی:

```python
grouped = df.groupby("Category")
print(grouped["Price"].mean())
```

### محاسبات آماری:

```python
print(df["Price"].mean())
print(df["Price"].median())
print(df["Price"].std())
```

### شمارش مقادیر:

```python
print(df["City"].value_counts())
```

🔹 نکته: برای تحلیل توزیع داده‌ها، می‌توان از `describe()` استفاده کرد:

```python
print(df.describe())
```

---

## 📊 مصورسازی داده‌ها

### نمودار میله‌ای:

```python
import matplotlib.pyplot as plt

df["City"].value_counts().plot(kind="bar", color="skyblue")
plt.title("تعداد مشتریان در هر شهر")
plt.xlabel("شهر")
plt.ylabel("تعداد")
plt.grid(True)
plt.show()
```

### نمودار دایره‌ای:

```python
df["Category"].value_counts().plot(kind="pie", autopct="%1.1f%%")
plt.title("سهم دسته‌بندی‌ها")
plt.ylabel("")
plt.show()
```

🔹 نکته: برای نمودارهای حرفه‌ای‌تر، از `seaborn` استفاده کنید:

```python
import seaborn as sns

sns.boxplot(x="Category", y="Price", data=df)
```

---

## 🛒 پروژه‌ی عملی: تحلیل فروش فروشگاه

### فایل `sales.csv` شامل:

- `Product`  
- `Category`  
- `Price`  
- `Quantity`  
- `Date`

### مراحل پروژه:

1. خواندن فایل  
2. محاسبه مجموع فروش هر محصول  
3. گروه‌بندی بر اساس دسته‌بندی  
4. تحلیل فروش ماهانه  
5. مصورسازی فروش  
6. ذخیره نتایج در فایل جدید

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("sales.csv")
df["Total"] = df["Price"] * df["Quantity"]
df["Date"] = pd.to_datetime(df["Date"])

monthly_sales = df.groupby(df["Date"].dt.to_period("M"))["Total"].sum()
monthly_sales.plot(kind="line", marker="o", color="green")
plt.title("فروش ماهانه")
plt.ylabel("تومان")
plt.xlabel("ماه")
plt.grid(True)
plt.show()

df.to_csv("sales_clean.csv", index=False)
```

---

## 🧪 تمرین‌های پیشرفته

1. تحلیل فروش بر اساس فصل با استفاده از `dt.month`  
2. بررسی همبستگی بین قیمت و تعداد فروش با `corr()`  
3. ساخت داشبورد ساده با Streamlit  
4. اتصال به پایگاه داده SQLite و اجرای کوئری‌ها  
5. دریافت داده‌های زنده از API هواشناسی و رسم نمودار دما  
6. استخراج داده از HTML با BeautifulSoup  
7. ساخت نمودار حرارتی (heatmap) برای ماتریس همبستگی

---


## 📚 منابع یادگیری بیشتر

برای اینکه در پردازش داده‌ها با پایتون حرفه‌ای بشی، پیشنهاد می‌کنم از منابع زیر استفاده کنی. این منابع هم برای مبتدی‌ها مناسب هستن، هم برای کسانی که می‌خوان وارد سطح پیشرفته بشن.

### 🔹 کتاب‌های پیشنهادی

- **Python for Data Analysis** نوشته‌ی Wes McKinney  
  کتابی کلاسیک و بسیار کاربردی که توسط خالق کتابخانه‌ی pandas نوشته شده. شامل مثال‌های واقعی، پروژه‌های عملی، و توضیح دقیق مفاهیم پردازش داده.

- **Data Science from Scratch** نوشته‌ی Joel Grus  
  اگر می‌خوای مفاهیم علم داده رو از پایه با پایتون یاد بگیری، این کتاب عالیه. شامل مباحث آماری، مصورسازی، و الگوریتم‌های یادگیری ماشین.

- **Effective Pandas** نوشته‌ی Matt Harrison  
  راهنمایی برای نوشتن کدهای تمیز، سریع و مؤثر با pandas. مناسب برای کسانی که با pandas کار کرده‌اند و می‌خوان حرفه‌ای‌تر بشن.

---

### 🔹 مستندات رسمی و منابع آنلاین

- [مستندات pandas](https://pandas.pydata.org/docs)  
  کامل‌ترین منبع برای یادگیری توابع، کلاس‌ها، و روش‌های pandas با مثال‌های دقیق.

- [مستندات NumPy](https://numpy.org/doc)  
  برای محاسبات عددی، ماتریس‌ها، و آرایه‌ها بسیار مفید است.

- [مستندات matplotlib](https://matplotlib.org/stable/contents.html)  
  برای رسم نمودارهای حرفه‌ای و سفارشی‌سازی آن‌ها.

- [مستندات Python](https://docs.python.org/3/)  
  مرجع اصلی برای زبان پایتون، شامل همه‌ی کتابخانه‌های استاندارد.

---

### 🔹 دوره‌های آموزشی آنلاین

- **DataCamp**  
  دوره‌های تعاملی در زمینه‌ی pandas، NumPy، مصورسازی، و پروژه‌های واقعی. مناسب برای یادگیری مرحله‌به‌مرحله.

- **Coursera – Python for Data Science by IBM**  
  دوره‌ای جامع با تمرین‌های عملی، پروژه‌های واقعی، و گواهی معتبر.

- **Udemy – Complete Python Data Science Bootcamp**  
  دوره‌ای کامل از مقدمات تا پیشرفته، شامل pandas، matplotlib، seaborn، و پروژه‌های کاربردی.

- **Kaggle Learn**  
  پلتفرمی رایگان برای یادگیری با تمرین‌های کوتاه و پروژه‌های واقعی. همچنین می‌تونی با داده‌های واقعی رقابت کنی.

---

### 🔹 ابزارهای تمرینی و پروژه‌محور

- [Google Colab](https://colab.research.google.com)  
  محیط رایگان برای اجرای کدهای پایتون در فضای ابری. مناسب برای تمرین، اشتراک‌گذاری، و اجرای پروژه‌های سنگین بدون نیاز به نصب.

- [Jupyter Notebook](https://jupyter.org)  
  محیطی تعاملی برای نوشتن کد، توضیح، و مصورسازی در یک فایل واحد. بسیار محبوب در علم داده.

- [Streamlit](https://streamlit.io)  
  ابزار ساخت داشبورد و اپلیکیشن‌های داده‌محور با پایتون، فقط با چند خط کد.

---

## ❓ سوالات بخش چهارم: پردازش داده‌ها در پایتون (Python Datenverarbeitung)

در این بخش، با مفاهیم و ابزارهای پردازش داده در پایتون آشنا شدیم. برای تثبیت یادگیری، به سوالات زیر پاسخ دهید:

### 1️⃣ تفاوت بین لیست‌های پایتونی و آرایه‌های NumPy چیست؟
- به تفاوت‌های عملکردی، سرعت، و نوع داده‌ها اشاره کنید.

### 2️⃣ چگونه می‌توان داده‌های یک فایل CSV را با استفاده از کتابخانه‌ی pandas بارگذاری و فیلتر کرد؟
- مثالی از استفاده‌ی `read_csv()` و `DataFrame` با شرط فیلتر ارائه دهید.

### 3️⃣ چه تفاوتی بین متدهای `apply()` و `map()` در pandas وجود دارد؟
- کاربرد هرکدام را با مثال توضیح دهید.

### 4️⃣ چگونه می‌توان داده‌های گمشده (missing values) را در pandas شناسایی و مدیریت کرد؟
- به متدهایی مثل `isnull()`, `dropna()`, و `fillna()` اشاره کنید.

### 5️⃣ در چه شرایطی استفاده از کتابخانه‌ی `NumPy` برای پردازش داده‌ها بهتر از `pandas` است؟
- به نوع داده‌ها، حجم داده‌ها، و نیاز به عملیات عددی اشاره کنید.

---

## ✅ نتیجه‌گیری نهایی

پردازش داده‌ها در پایتون فقط یک مهارت فنی نیست؛ بلکه پلی است بین داده‌های خام و تصمیم‌گیری‌های هوشمندانه. با یادگیری ابزارهایی مثل `pandas`, `numpy`, `matplotlib`, و `json`، می‌تونی داده‌ها رو بخونی، پاک‌سازی کنی، تحلیل کنی، و نتایج قابل فهم تولید کنی.

در این مقاله یاد گرفتیم:

- چطور داده‌ها رو از منابع مختلف بخونیم و ذخیره کنیم  
- چطور داده‌های ناقص یا نادرست رو پاک‌سازی کنیم  
- چطور داده‌ها رو فیلتر، گروه‌بندی و تحلیل کنیم  
- چطور نتایج رو به‌صورت نمودارهای قابل فهم نمایش بدیم  
- چطور پروژه‌های واقعی مثل تحلیل فروش رو با پایتون انجام بدیم

🔍 نکته‌ی مهم اینه که پردازش داده‌ها فقط با تمرین و تجربه عمیق می‌شه. هر فایل داده‌ای که باز می‌کنی، یه داستان پنهان داره—و تو با ابزارهای پایتون می‌تونی اون داستان رو کشف کنی.

اگر تازه شروع کردی، نگران نباش. مسیر یادگیری پایتون در پردازش داده‌ها پر از منابع خوب، پروژه‌های جذاب، و جامعه‌ی فعال هست. فقط کافیه کنجکاو باشی و هر روز یه قدم برداری.

---