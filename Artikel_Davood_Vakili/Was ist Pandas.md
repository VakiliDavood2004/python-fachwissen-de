# 🇩🇪 Beschreibung auf Deutsch
---
## 🐼 Umfassende Anleitung zu Pandas — Die Datenanalyse-Bibliothek für Python

---

## 📍 Einführung

Pandas ist eine Open-Source-Bibliothek in Python für die Datenmanipulation und -analyse. Die zwei Hauptstrukturen von Pandas sind:

- **Series**: Eine eindimensionale Datenreihe mit Beschriftungen  
- **DataFrame**: Eine zweidimensionale Tabelle mit mehreren Datentypen  

---

## 🔧 Installation

```bash
pip install pandas
```

Oder mit conda:

```bash
conda install pandas
```

---

## 🧠 Datenstrukturen in Pandas

### Series

```python
import pandas as pd

s = pd.Series([100, 200, 300], index=['a', 'b', 'c'])
print(s)
```

### DataFrame

```python
data = {'Name': ['Ali', 'Sara', 'Reza'], 'Alter': [25, 30, 28]}
df = pd.DataFrame(data)
print(df)
```

---

## 📂 Daten einlesen

- CSV-Dateien  
- Excel-Dateien  
- JSON  
- SQL-Datenbanken

```python
df = pd.read_csv('data.csv')
df = pd.read_excel('data.xlsx')
df = pd.read_json('data.json')
```

---

## 🔍 Erste Datenerkundung

```python
df.head()
df.tail()
df.info()
df.describe()
```

---

## 🔎 Datenzugriff und Indexierung

```python
df['Name']
df[['Name', 'Alter']]

df.loc[0]
df.iloc[2]

df[df['Alter'] > 27]
```

---

## ✏️ Daten bearbeiten

- Spalten hinzufügen  
- Umbenennen oder löschen  
- Werte modifizieren mit `apply`

```python
df['Land'] = ['Iran', 'Deutschland', 'USA']
df.rename(columns={'Name': 'Vollständiger Name'}, inplace=True)
df.drop('Land', axis=1, inplace=True)
df['Alter'] = df['Alter'].apply(lambda x: x + 5)
```

---

## 🔁 Umgang mit fehlenden Werten

```python
df.fillna(0)
df.dropna()
```

---

## 📊 Gruppierung und Aggregation

```python
df.groupby('Land').mean()
df.groupby('Land')['Alter'].sum()
```

---

## 🔀 Sortieren von Daten

```python
df.sort_values(by='Alter', ascending=False)
```

---

## 🧩 Daten zusammenführen

- `concat`  
- `merge`  
- `join`

```python
pd.concat([df1, df2])
pd.merge(df1, df2, on='ID')
```

---

## 🕒 Arbeiten mit Datum und Zeit

```python
df['Datum'] = pd.to_datetime(df['Datum'])
df['Jahr'] = df['Datum'].dt.year
```

---

## 📐 Pivot-Tabellen

```python
df.pivot_table(values='Umsatz', index='Region', columns='Monat', aggfunc='sum')
```

---

## 📈 Visualisierung mit Pandas

```python
df.plot(kind='bar')
df.plot(kind='line')
df.plot(kind='hist')
```

---

## 📊 Beispiel: Titanic-Datensatz

```python
df = pd.read_csv('https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv')

df.groupby('Pclass')['Survived'].mean()
df['Age'].plot.hist(bins=30)
```

---

## ⚙️ Fortgeschrittene Funktionen

- Mehrstufige Indizes (MultiIndex)  
- Fensterfunktionen (`rolling`, `expanding`)  
- Kategorische Daten  
- Speicheroptimierung  
- Verarbeitung großer Datenmengen (mit `chunks`)  

---

## 🧪 Praktische Übung

> Verwende den Titanic-Datensatz und berechne:
>
> - Durchschnittsalter der Überlebenden pro Klasse  
> - Überlebensrate für Passagiere unter 18 Jahren  
> - Gesamte Fahrpreise pro Einstiegsort (Embarked)  

---

## 🎯 Pandas vs Excel

| Merkmal               | Pandas              | Excel           |
|----------------------|---------------------|-----------------|
| Automatisierung       | Ja                  | Eingeschränkt   |
| Datenvolumen          | Sehr hoch           | ~1 Mio Zeilen   |
| Programmierbarkeit    | Hoch                | Gering          |
| Verarbeitungsgeschw.  | Schnell             | Mittel          |
| Ökosystem             | Python              | Office/Excel    |

---

## 🔗 Nützliche Ressourcen

- [Offizielle Dokumentation von Pandas](https://pandas.pydata.org/docs/)
- [Pandas-Tutorials bei Real Python](https://realpython.com/pandas-python-explore-dataset/)
- [Pandas-Übungen auf Kaggle](https://www.kaggle.com/learn/pandas)

---

## 🧠 Fazit

Pandas ist ein unverzichtbares Werkzeug in der modernen Datenanalyse, sei es in Data Science, Machine Learning oder Business Intelligence. Mit Pandas kannst du Daten bereinigen, umstrukturieren, analysieren und visualisieren — alles mit nur wenigen Zeilen Code.



---



# 🇬🇧 Description in English
---
## 🐼 Comprehensive Guide to Pandas — Python’s Data Analysis Powerhouse

---

## 📍 Introduction

Pandas is an open-source library in Python designed for data manipulation and analysis. It offers two main data structures:

- **Series**: A one-dimensional labeled array  
- **DataFrame**: A two-dimensional tabular structure with columns and rows  

---

## 🔧 Installation

```bash
pip install pandas
```

Or with conda:

```bash
conda install pandas
```

---

## 🧠 Core Data Structures

### Series

```python
import pandas as pd

s = pd.Series([100, 200, 300], index=['a', 'b', 'c'])
print(s)
```

### DataFrame

```python
data = {'Name': ['Ali', 'Sara', 'Reza'], 'Age': [25, 30, 28]}
df = pd.DataFrame(data)
print(df)
```

---

## 📂 Reading Data Files

Supports various formats:

- CSV  
- Excel  
- JSON  
- SQL Databases  

```python
df = pd.read_csv('data.csv')
df = pd.read_excel('data.xlsx')
df = pd.read_json('data.json')
```

---

## 🔍 Exploring Data

```python
df.head()
df.tail()
df.info()
df.describe()
```

---

## 🔎 Selecting and Filtering Data

```python
df['Name']
df[['Name', 'Age']]

df.loc[0]
df.iloc[2]

df[df['Age'] > 27]
```

---

## ✏️ Editing Data

- Add columns  
- Rename or drop  
- Modify values using `apply`

```python
df['Country'] = ['Iran', 'Germany', 'USA']
df.rename(columns={'Name': 'Full Name'}, inplace=True)
df.drop('Country', axis=1, inplace=True)
df['Age'] = df['Age'].apply(lambda x: x + 5)
```

---

## 🔁 Handling Missing Values

```python
df.fillna(0)
df.dropna()
```

---

## 📊 Grouping and Aggregating

```python
df.groupby('Country').mean()
df.groupby('Country')['Age'].sum()
```

---

## 🔀 Sorting Data

```python
df.sort_values(by='Age', ascending=False)
```

---

## 🧩 Combining DataFrames

- `concat`  
- `merge`  
- `join`

```python
pd.concat([df1, df2])
pd.merge(df1, df2, on='ID')
```

---

## 🕒 Working with Dates and Times

```python
df['Date'] = pd.to_datetime(df['Date'])
df['Year'] = df['Date'].dt.year
```

---

## 📐 Pivot Tables

```python
df.pivot_table(values='Sales', index='Region', columns='Month', aggfunc='sum')
```

---

## 📈 Plotting with Pandas

```python
df.plot(kind='bar')
df.plot(kind='line')
df.plot(kind='hist')
```

---

## 📊 Real Dataset Example: Titanic

```python
df = pd.read_csv('https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv')

df.groupby('Pclass')['Survived'].mean()
df['Age'].plot.hist(bins=30)
```

---

## ⚙️ Advanced Features

- MultiIndex  
- Rolling and expanding windows  
- Categorical data  
- Memory optimization  
- Processing large datasets (chunking)

---

## 🧪 Practice Tasks

> Using the Titanic dataset, try:
>
> - Calculating average age of survivors by class  
> - Survival rate for passengers under 18  
> - Total fare by embarkation point  

---

## 🎯 Pandas vs Excel

| Feature              | Pandas              | Excel           |
|---------------------|---------------------|-----------------|
| Automation           | Yes                 | Limited         |
| Data Volume          | Millions of rows    | ~1 million rows |
| Programming Power    | High                | Low             |
| Speed                | Fast                | Medium          |
| Ecosystem Integration| Python tools        | Microsoft Office|

---

## 🔗 Learning Resources

- [Pandas Official Docs](https://pandas.pydata.org/docs/)
- [Real Python Pandas Tutorial](https://realpython.com/pandas-python-explore-dataset/)
- [Kaggle Pandas Exercises](https://www.kaggle.com/learn/pandas)

---

## 🧠 Final Thoughts

Pandas is an essential tool for anyone working with data. Whether you’re cleaning messy files, performing complex transformations, or building a full data pipeline, Pandas gives you the clarity, power, and flexibility to do it efficiently—all in Python.



---



# 🇮🇷 توضیحات به زبان فارسی
---
## 🐼 راهنمای جامع Pandas — کتابخانه‌ی قدرتمند تحلیل داده در پایتون

---

## 📍 مقدمه

Pandas یک کتابخانه‌ی متن‌باز در پایتون برای تحلیل و دست‌کاری داده‌هاست. دو ساختار داده‌ی اصلی در Pandas عبارتند از:

- **Series**: آرایه‌ای یک‌بعدی با اندیس مشخص  
- **DataFrame**: جدول داده‌ای دوبعدی که می‌تونه شامل انواع داده‌ها باشه

---

## 🔧 نصب Pandas

```bash
pip install pandas
```

یا از طریق conda:

```bash
conda install pandas
```

---

## 🧠 ساختارهای اصلی داده در Pandas

### Series (سری)

```python
import pandas as pd

s = pd.Series([100, 200, 300], index=['a', 'b', 'c'])
print(s)
```

### DataFrame (دیتافریم)

```python
data = {'نام': ['علی', 'سارا', 'رضا'], 'سن': [25, 30, 28]}
df = pd.DataFrame(data)
print(df)
```

---

## 📂 خواندن داده‌ها

- فایل CSV  
- فایل Excel  
- JSON  
- بانک‌های SQL

```python
df = pd.read_csv('data.csv')
df = pd.read_excel('data.xlsx')
df = pd.read_json('data.json')
```

---

## 🔍 بررسی اولیه داده‌ها

```python
df.head()
df.tail()
df.info()
df.describe()
```

---

## 🔎 انتخاب داده‌ها و اندیس‌گذاری

```python
df['نام']
df[['نام', 'سن']]

df.loc[0]
df.iloc[2]

df[df['سن'] > 27]
```

---

## ✏️ تغییر داده‌ها

- افزودن ستون  
- حذف یا تغییر نام  
- تغییر اندیس  
- تغییر مقادیر با تابع apply

```python
df['کشور'] = ['ایران', 'آلمان', 'آمریکا']
df.rename(columns={'نام': 'نام کامل'}, inplace=True)
df.drop('کشور', axis=1, inplace=True)
df['سن'] = df['سن'].apply(lambda x: x + 5)
```

---

## 🔁 مدیریت داده‌های گم‌شده

```python
df.fillna(0)
df.dropna()
```

---

## 📊 گروه‌بندی و تجمیع داده‌ها

```python
df.groupby('کشور').mean()
df.groupby('کشور')['سن'].sum()
```

---

## 🔀 مرتب‌سازی داده‌ها

```python
df.sort_values(by='سن', ascending=False)
```

---

## 🧩 ترکیب دیتاها

- اتصال (concat)  
- ادغام (merge)  
- پیوستن (join)

```python
pd.concat([df1, df2])
pd.merge(df1, df2, on='کد')
```

---

## 🕒 کار با تاریخ و زمان

```python
df['تاریخ'] = pd.to_datetime(df['تاریخ'])
df['سال'] = df['تاریخ'].dt.year
```

---

## 📐 جداول محوری (Pivot Table)

```python
df.pivot_table(values='فروش', index='منطقه', columns='ماه', aggfunc='sum')
```

---

## 📈 رسم نمودار با Pandas

```python
df.plot(kind='bar')
df.plot(kind='line')
df.plot(kind='hist')
```

---

## 📊 مثال کاربردی: دیتاست Titanic

```python
df = pd.read_csv('https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv')

# نرخ بقا بر اساس کلاس مسافری
df.groupby('Pclass')['Survived'].mean()

# هیستوگرام سن
df['Age'].plot.hist(bins=30)
```

---

## ⚙️ عملیات‌های پیشرفته

- داده‌های چندسطحی (MultiIndex)  
- توابع پنجره‌ای (rolling, expanding)  
- داده‌های نوع categoricals  
- بهینه‌سازی حافظه  
- پردازش فایل‌های بزرگ (با chunks)

---

## 🧪 تمرین کاربردی

> با استفاده از دیتاست Titanic موارد زیر را محاسبه کن:
>
> - میانگین سن مسافران نجات‌یافته بر اساس کلاس  
> - نرخ بقا برای مسافران زیر ۱۸ سال  
> - مجموع کرایه‌ها بر اساس محل سوار شدن (Embarked)

---

## 🎯 مقایسه Pandas با Excel

| ویژگی                 | Pandas            | Excel         |
|----------------------|-------------------|---------------|
| خودکارسازی           | دارد              | محدود         |
| حجم داده قابل پردازش | بالا (میلیون‌ها)  | تا حدود ۱ میلیون |
| قابلیت برنامه‌نویسی | قوی               | ضعیف          |
| سرعت پردازش          | بالا              | متوسط         |
| سازگاری با ابزارها   | Python کامل       | اکسل و آفیس    |

---

## 🔗 منابع یادگیری

- [مستند رسمی Pandas](https://pandas.pydata.org/docs/)
- [آموزش Pandas در Real Python](https://realpython.com/pandas-python-explore-dataset/)
- [تمرین‌های Pandas در Kaggle](https://www.kaggle.com/learn/pandas)

---

## 🔚 نتیجه‌گیری

کتابخانه Pandas یکی از ابزارهای کلیدی در علم داده، یادگیری ماشین، و تحلیل آماری به‌شمار می‌ره. با یادگیری Pandas می‌تونی داده‌ها رو تمیز، خلاصه، تجسم و تحلیل کنی و گام بزرگی در مسیر تبدیل شدن به متخصص داده برداری.