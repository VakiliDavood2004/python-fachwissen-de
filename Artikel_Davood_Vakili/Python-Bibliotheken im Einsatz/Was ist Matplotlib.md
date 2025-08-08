# 🇩🇪 Beschreibung auf Deutsch
---
## 🎨 Comprehensive Guide to Matplotlib — Python’s Data Visualization Library

---

## ✨ Introduction

Matplotlib is one of the most powerful and widely used data visualization libraries in Python. It enables the creation of a wide range of plots such as line charts, bar graphs, pie charts, scatter plots, and more. Developed in 2003, it’s a staple in scientific, engineering, financial, and educational projects.

This article aims to thoroughly explore Matplotlib’s capabilities — from installation to advanced visualization techniques.

---

## 🔧 Installing Matplotlib

Install via pip:

```bash
pip install matplotlib
```

Or inside a Jupyter Notebook:

```python
!pip install matplotlib
```

---

## 🧱 Library Structure

Matplotlib includes two main interfaces:

- **Pyplot:** A quick and simple interface for plotting
- **Object-Oriented API:** Lower-level control over plot elements

### Simple Example Using `pyplot`

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [10, 20, 25, 30]

plt.plot(x, y)
plt.title("Simple Chart")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.grid(True)
plt.show()
```

---

## 📊 Types of Plots in Matplotlib

### 1. Line Plot

```python
plt.plot([1, 2, 3], [2, 4, 1])
```

### 2. Bar Chart

```python
plt.bar(['A', 'B', 'C'], [10, 20, 15])
```

### 3. Pie Chart

```python
labels = ['Python', 'C++', 'Java']
sizes = [45, 30, 25]
plt.pie(sizes, labels=labels, autopct='%1.1f%%')
```

### 4. Scatter Plot

```python
plt.scatter([1, 2, 3], [10, 15, 13])
```

### 5. Histogram

```python
data = [1, 3, 2, 5, 7, 2, 3, 5, 6]
plt.hist(data, bins=5)
```

---

## 🎨 Customizing Plots

### Color and Line Styles

```python
plt.plot(x, y, color='green', linestyle='--', marker='o')
```

### Change Figure Size

```python
plt.figure(figsize=(10, 5))
```

### Add Text Annotations

```python
plt.text(2, 25, "Key Point", fontsize=12)
```

---

## 📁 Saving Plots

```python
plt.savefig('diagram.png')
```

Supports various formats such as PNG, JPG, SVG, etc.

---

## 🧠 Combining Plots with Subplot

```python
plt.subplot(1, 2, 1)
plt.plot(x, y)

plt.subplot(1, 2, 2)
plt.bar(x, y)
```

---

## 🧪 Real-World Applications

- **Financial Analysis:** Stock prices, moving averages, and trading volumes
- **Scientific Visualization:** Experimental results and distribution curves
- **Statistical Reporting:** Histograms and pie charts for data summaries

---

## 🧩 Comparison with Seaborn and Plotly

| Feature              | Matplotlib | Seaborn | Plotly |
|----------------------|------------|---------|--------|
| Ease of Use          | High       | Medium  | Medium |
| Interactivity        | Low        | Low     | High   |
| Visual Style         | Moderate   | High    | Very High |
| Statistical Tools    | Basic      | Advanced| Moderate |
| Web Output           | No         | No      | Yes    |

---

## 🛠 Advanced Tips

### Set Font (e.g., Persian Support)

```python
plt.rcParams['font.family'] = 'B Nazanin'
```

### Apply Global Styles

```python
plt.style.use('ggplot')
```

### 3D Plotting with `mpl_toolkits`

```python
from mpl_toolkits.mplot3d import Axes3D
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot([1,2,3], [4,5,6], [7,8,9])
```

---

## 📚 Learning Resources

- [Matplotlib Official Documentation](https://matplotlib.org/stable/index.html)
- [Real Python Tutorials](https://realpython.com/)
- [YouTube Channels: Corey Schafer, Sentdex]
- [Book: Python Data Science Handbook]

---

## 🔚 Conclusion

Matplotlib is a foundational tool for any Python programmer looking to visualize data effectively. Mastering it enables better communication of insights, deeper analysis, and more professional presentations. Even with alternatives like Seaborn and Plotly, Matplotlib remains a central pillar in many production and research environments.



---



# 🇬🇧 Description in English
---
# 🎨 Comprehensive Guide to Matplotlib — Python’s Data Visualization Library

---

## ✨ Introduction

Matplotlib is one of the most powerful and widely used data visualization libraries in Python. It enables the creation of a wide range of plots such as line charts, bar graphs, pie charts, scatter plots, and more. Developed in 2003, it’s a staple in scientific, engineering, financial, and educational projects.

This article aims to thoroughly explore Matplotlib’s capabilities — from installation to advanced visualization techniques.

---

## 🔧 Installing Matplotlib

Install via pip:

```bash
pip install matplotlib
```

Or inside a Jupyter Notebook:

```python
!pip install matplotlib
```

---

## 🧱 Library Structure

Matplotlib includes two main interfaces:

- **Pyplot:** A quick and simple interface for plotting
- **Object-Oriented API:** Lower-level control over plot elements

### Simple Example Using `pyplot`

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [10, 20, 25, 30]

plt.plot(x, y)
plt.title("Simple Chart")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.grid(True)
plt.show()
```

---

## 📊 Types of Plots in Matplotlib

### 1. Line Plot

```python
plt.plot([1, 2, 3], [2, 4, 1])
```

### 2. Bar Chart

```python
plt.bar(['A', 'B', 'C'], [10, 20, 15])
```

### 3. Pie Chart

```python
labels = ['Python', 'C++', 'Java']
sizes = [45, 30, 25]
plt.pie(sizes, labels=labels, autopct='%1.1f%%')
```

### 4. Scatter Plot

```python
plt.scatter([1, 2, 3], [10, 15, 13])
```

### 5. Histogram

```python
data = [1, 3, 2, 5, 7, 2, 3, 5, 6]
plt.hist(data, bins=5)
```

---

## 🎨 Customizing Plots

### Color and Line Styles

```python
plt.plot(x, y, color='green', linestyle='--', marker='o')
```

### Change Figure Size

```python
plt.figure(figsize=(10, 5))
```

### Add Text Annotations

```python
plt.text(2, 25, "Key Point", fontsize=12)
```

---

## 📁 Saving Plots

```python
plt.savefig('diagram.png')
```

Supports various formats such as PNG, JPG, SVG, etc.

---

## 🧠 Combining Plots with Subplot

```python
plt.subplot(1, 2, 1)
plt.plot(x, y)

plt.subplot(1, 2, 2)
plt.bar(x, y)
```

---

## 🧪 Real-World Applications

- **Financial Analysis:** Stock prices, moving averages, and trading volumes
- **Scientific Visualization:** Experimental results and distribution curves
- **Statistical Reporting:** Histograms and pie charts for data summaries

---

## 🧩 Comparison with Seaborn and Plotly

| Feature              | Matplotlib | Seaborn | Plotly |
|----------------------|------------|---------|--------|
| Ease of Use          | High       | Medium  | Medium |
| Interactivity        | Low        | Low     | High   |
| Visual Style         | Moderate   | High    | Very High |
| Statistical Tools    | Basic      | Advanced| Moderate |
| Web Output           | No         | No      | Yes    |

---

## 🛠 Advanced Tips

### Set Font (e.g., Persian Support)

```python
plt.rcParams['font.family'] = 'B Nazanin'
```

### Apply Global Styles

```python
plt.style.use('ggplot')
```

### 3D Plotting with `mpl_toolkits`

```python
from mpl_toolkits.mplot3d import Axes3D
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot([1,2,3], [4,5,6], [7,8,9])
```

---

## 📚 Learning Resources

- [Matplotlib Official Documentation](https://matplotlib.org/stable/index.html)
- [Real Python Tutorials](https://realpython.com/)
- [YouTube Channels: Corey Schafer, Sentdex]
- [Book: Python Data Science Handbook]

---

## 🔚 Conclusion

Matplotlib is a foundational tool for any Python programmer looking to visualize data effectively. Mastering it enables better communication of insights, deeper analysis, and more professional presentations. Even with alternatives like Seaborn and Plotly, Matplotlib remains a central pillar in many production and research environments.



---



# 🇮🇷 توضیحات به زبان فارسی
---
## 🎨 مقاله کامل درباره Matplotlib — کتابخانه مصورسازی داده در پایتون

---

## ✨ مقدمه

Matplotlib یکی از قدرتمندترین و گسترده‌ترین کتابخانه‌های مصورسازی داده در زبان پایتون است. این کتابخانه، امکان رسم انواع نمودارها را از جمله نمودارهای خطی، میله‌ای، دایره‌ای، پراکندگی و ... فراهم می‌کند. از سال ۲۰۰۳ توسعه یافته و تا امروز در اکثر پروژه‌های علمی، مهندسی، مالی و آموزشی مورد استفاده قرار گرفته است.

هدف این مقاله، بررسی دقیق و جامع تمام قابلیت‌های این کتابخانه است؛ از نصب تا رسم نمودارهای پیچیده.

---

## 🔧 نصب Matplotlib

برای نصب، فقط کافی است از pip استفاده کنید:

```bash
pip install matplotlib
```

یا اگر از jupyter notebook استفاده می‌کنید:

```python
!pip install matplotlib
```

---

## 🧱 ساختار کتابخانه

Matplotlib دو بخش اصلی دارد:

- **Pyplot:** رابط ساده و سریع برای رسم نمودارها.
- **Object-Oriented API:** سطح پایین‌تر برای کنترل بیشتر روی عناصر نمودار.

### مثالی ساده با `pyplot`

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [10, 20, 25, 30]

plt.plot(x, y)
plt.title("نمودار ساده")
plt.xlabel("محور X")
plt.ylabel("محور Y")
plt.grid(True)
plt.show()
```

---

## 📊 انواع نمودارها در Matplotlib

### ۱. نمودار خطی (Line Plot)
برای نمایش روند تغییرات:

```python
plt.plot([1, 2, 3], [2, 4, 1])
```

### ۲. نمودار میله‌ای (Bar Chart)

```python
plt.bar(['A', 'B', 'C'], [10, 20, 15])
```

### ۳. نمودار دایره‌ای (Pie Chart)

```python
labels = ['Python', 'C++', 'Java']
sizes = [45, 30, 25]
plt.pie(sizes, labels=labels, autopct='%1.1f%%')
```

### ۴. نمودار پراکندگی (Scatter Plot)

```python
plt.scatter([1, 2, 3], [10, 15, 13])
```

### ۵. نمودار هیستوگرام (Histogram)

```python
data = [1, 3, 2, 5, 7, 2, 3, 5, 6]
plt.hist(data, bins=5)
```

---

## 🎨 سفارشی‌سازی نمودارها

### تنظیم رنگ و سبک خط

```python
plt.plot(x, y, color='green', linestyle='--', marker='o')
```

### تغییر اندازه شکل

```python
plt.figure(figsize=(10, 5))
```

### افزودن توضیحات

```python
plt.text(2, 25, "نقطه مهم", fontsize=12)
```

---

## 📁 ذخیره‌سازی نمودارها

```python
plt.savefig('diagram.png')
```

می‌توانید فرمت‌های مختلف مانند PNG, JPG, SVG استفاده کنید.

---

## 🧠 ترکیب نمودارها

استفاده از `subplot` برای رسم چند نمودار در یک پنجره:

```python
plt.subplot(1, 2, 1)
plt.plot(x, y)

plt.subplot(1, 2, 2)
plt.bar(x, y)
```

---

## 🧪 کاربردهای واقعی

### تحلیل داده‌های مالی
نمایش روند قیمت سهام، میانگین متحرک و حجم معاملات.

### تجسم نتایج علمی
نمایش خروجی آزمایش‌ها، منحنی‌ها و نمودارهای انتشار.

### مصورسازی داده‌های آماری
استفاده از هیستوگرام و نمودار دایره‌ای برای گزارش داده‌ها.

---

## 🧩 مقایسه با Seaborn و Plotly

| ویژگی‌ها       | Matplotlib | Seaborn | Plotly |
|----------------|------------|---------|--------|
| سادگی          | زیاد       | متوسط   | متوسط |
| قابلیت تعامل  | کم         | کم       | زیاد  |
| ظاهر گرافیکی  | متوسط      | بالا     | خیلی بالا |
| قابلیت‌های آماری | کم         | زیاد     | متوسط |
| خروجی وب      | ندارد      | ندارد    | دارد  |

---

## 🛠 نکات پیشرفته

### تنظیم فونت فارسی

```python
plt.rcParams['font.family'] = 'B Nazanin'
```

### اعمال Style جهانی

```python
plt.style.use('ggplot')
```

### ترسیم نمودار سه‌بعدی با mpl_toolkits

```python
from mpl_toolkits.mplot3d import Axes3D
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot([1,2,3], [4,5,6], [7,8,9])
```

---

## 📚 منابع یادگیری بیشتر

- [مستندات رسمی Matplotlib](https://matplotlib.org/stable/index.html)
- [دوره‌های آموزشی در Real Python](https://realpython.com/)
- [کانال‌های یوتیوب مانند Corey Schafer و Sentdex]
- [کتاب “Python Data Science Handbook”]

---

## 🔚 نتیجه‌گیری

Matplotlib یکی از بنیادی‌ترین ابزارها برای هر برنامه‌نویس پایتون است که با یادگیری آن، امکان تجسم داده‌ها، تحلیل بهتر و ارائه حرفه‌ای‌تر اطلاعات را خواهید داشت. با وجود کتابخانه‌های جانبی مانند Seaborn و Plotly، هنوز Matplotlib در بسیاری از پروژه‌های حرفه‌ای نقش مرکزی دارد.
