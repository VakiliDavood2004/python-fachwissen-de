# Django Quiz – Kapitel 9

## Fragen

1. Was ist der Hauptzweck von Django-Templates?
2. Was ist der Unterschied zwischen `render()` und `HttpResponse()`?
3. Wie zeigt man Variablen in Django-Templates an?
4. Wozu dient das `{% for %}`-Tag in Templates?
5. Wie schreibt man Bedingungen in Django-Templates?
6. Was macht das `{% include %}`-Tag?
7. Wie verwendet man den `date`-Filter in Templates?
8. Was ist der Unterschied zwischen `{{ variable }}` und `{% tag %}`?
9. Wie definiert man ein Basis-Template in Django?
10. Wozu dient das `{% block %}`-Tag?
11. Wie verwendet man verschachtelte Templates in Django?
12. Was macht der `length`-Filter in Templates?
13. Wie verwendet man `ifchanged` in einem Template?
14. Welche Rolle spielt `{% csrf_token %}` in Formularen?
15. Wie rendert man ein Formular als HTML in einem Template?
16. Was ist der Unterschied zwischen `{{ form.as_p }}` und `{{ form.as_table }}`?
17. Wie fügt man CSS-Klassen zu Django-Formularen hinzu?
18. Wie zeigt man Formularfehler im Template an?
19. Wozu dient das `{% url %}`-Tag?
20. Wie verwendet man Kontextvariablen in Templates?
21. Was macht der `default`-Filter?
22. Wie verwendet man `extends` für Template-Vererbung?
23. Wozu dient das `{% comment %}`-Tag?
24. Wie verwendet man `forloop.counter` in einer Schleife?
25. Was macht der `truncatechars`-Filter?
26. Wie verwendet man `safe`, um HTML nicht zu escapen?
27. Welche Rolle spielt `{% static %}` in Templates?
28. Wie lädt man CSS- und JS-Dateien in einem Template?
29. Wie verwendet man `if` mit `and` und `or` in Templates?
30. Was macht der `join`-Filter?
31. Wie verwendet man `with`, um temporäre Variablen zu definieren?
32. Wozu dient das `{% cycle %}`-Tag?
33. Wie verwendet man `add`, um Zahlen zu addieren?
34. Was macht der `slice`-Filter?
35. Wie verwendet man `pluralize` für Singular/Plural?
36. Was macht das `{% regroup %}`-Tag?
37. Wie verwendet man `widthratio`, um Prozentsätze zu berechnen?
38. Was macht der `filesizeformat`-Filter?
39. Wie verwendet man `yesno`, um boolesche Werte darzustellen?
40. Wie verwendet man `dictsort`, um Dictionaries zu sortieren?
41. Was macht das `{% firstof %}`-Tag?
42. Wie verwendet man `linebreaksbr`, um Zeilenumbrüche in `<br>` umzuwandeln?
43. Was macht der `wordcount`-Filter?
44. Wie verwendet man `random`, um ein zufälliges Element auszuwählen?
45. Was macht der `title`-Filter?
46. Wie verwendet man `capfirst`, um den ersten Buchstaben zu kapitalisieren?
47. Was machen die Filter `lower` und `upper`?
48. Wie verwendet man `length_is`, um die genaue Länge zu prüfen?
49. Wozu dient `{% autoescape off %}`?
50. Wie verwendet man `divisibleby`, um Teilbarkeit zu prüfen?
51. Was macht der `time`-Filter?
52. Wie verwendet man `unordered_list`, um Listen darzustellen?
53. Was macht der `urlize`-Filter?
54. Wie verwendet man `phone2numeric`, um Telefonnummern umzuwandeln?
55. Was macht der `striptags`-Filter?
56. Wie verwendet man `truncatewords`, um Text zu kürzen?
57. Was macht der `iriencode`-Filter?
58. Wie verwendet man `make_list`, um Strings in Listen umzuwandeln?
59. Was macht der `addslashes`-Filter?
60. Wie verwendet man `escapejs`, um JavaScript zu sichern?
61. Was macht der `json_script`-Filter?
62. Wie verwendet man `removetags`, um HTML-Tags zu entfernen?
63. Was macht der `urlencode`-Filter?
64. Wie verwendet man `stringformat`, um Strings zu formatieren?
65. Was macht der `floatformat`-Filter?
66. Wie verwendet man `filesizeformat`, um lesbare Dateigrößen darzustellen?
67. Was macht der `linenumbers`-Filter?
68. Wie verwendet man `default_if_none` für Standardwerte?
69. Wie funktioniert der `slice`-Filter mit Listen?
70. Wie verwendet man `dictsortreversed`, um Dictionaries rückwärts zu sortieren?
71. Was macht der `wordwrap`-Filter?
72. Wie verwendet man `truncatewords_html`, um HTML-Inhalte zu kürzen?
73. Was macht der `timeuntil`-Filter?
74. Wie verwendet man `timesince`, um vergangene Zeit zu berechnen?
75. Was macht der `center`-Filter?
76. Wie verwendet man `rjust` und `ljust` für Abstand?
77. Was macht der `cut`-Filter?
78. Wie verwendet man `length_is`, um die Listenlänge zu validieren?
79. Wie funktioniert der `random`-Filter mit Listen?
80. Wie verwendet man `filesizeformat`, um menschenlesbare Größen darzustellen?





# Django Quiz – Chapter 9

## Questions

1. What is the main purpose of using Django templates?
2. What is the difference between `render()` and `HttpResponse()`?
3. How can you display variables in Django templates?
4. What is the purpose of the `{% for %}` tag in templates?
5. How can you write conditional statements in Django templates?
6. What does the `{% include %}` tag do?
7. How do you use the `date` filter in templates?
8. What is the difference between `{{ variable }}` and `{% tag %}`?
9. How do you define a base template in Django?
10. What is the purpose of the `{% block %}` tag?
11. How can you use nested templates in Django?
12. What does the `length` filter do in templates?
13. How do you use `ifchanged` in a template?
14. What is the role of `{% csrf_token %}` in forms?
15. How can you render a form as HTML in a template?
16. What is the difference between `{{ form.as_p }}` and `{{ form.as_table }}`?
17. How can you apply CSS classes to Django forms?
18. How do you display form errors in a template?
19. What is the purpose of the `{% url %}` tag?
20. How do you use context variables in templates?
21. What does the `default` filter do?
22. How do you use `extends` for template inheritance?
23. What is the purpose of the `{% comment %}` tag?
24. How do you use `forloop.counter` in a loop?
25. What does the `truncatechars` filter do?
26. How do you use `safe` to prevent HTML escaping?
27. What is the role of `{% static %}` in templates?
28. How do you load CSS and JS files in a template?
29. How can you use `if` with `and` and `or` in templates?
30. What does the `join` filter do?
31. How do you use `with` to define temporary variables?
32. What is the purpose of the `{% cycle %}` tag?
33. How do you use `add` to sum numbers in templates?
34. What does the `slice` filter do?
35. How do you use `pluralize` for singular/plural forms?
36. What does the `{% regroup %}` tag do?
37. How do you use `widthratio` to calculate percentages?
38. What does the `filesizeformat` filter do?
39. How do you use `yesno` to display boolean values?
40. How do you use `dictsort` to sort dictionaries?
41. What does the `{% firstof %}` tag do?
42. How do you use `linebreaksbr` to convert newlines to `<br>`?
43. What does the `wordcount` filter do?
44. How do you use `random` to select a random item?
45. What does the `title` filter do?
46. How do you use `capfirst` to capitalize the first letter?
47. What do the `lower` and `upper` filters do?
48. How do you use `length_is` to check exact length?
49. What is the purpose of `{% autoescape off %}`?
50. How do you use `divisibleby` to check divisibility?
51. What does the `time` filter do?
52. How do you use `unordered_list` to display lists?
53. What does the `urlize` filter do?
54. How do you use `phone2numeric` to convert phone numbers?
55. What does the `striptags` filter do?
56. How do you use `truncatewords` to shorten text?
57. What does the `iriencode` filter do?
58. How do you use `make_list` to convert strings to lists?
59. What does the `addslashes` filter do?
60. How do you use `escapejs` to secure JavaScript?
61. What does the `json_script` filter do?
62. How do you use `removetags` to remove HTML tags?
63. What does the `urlencode` filter do?
64. How do you use `stringformat` to format strings?
65. What does the `floatformat` filter do?
66. How do you use `filesizeformat` to display readable file sizes?
67. What does the `linenumbers` filter do?
68. How do you use `default_if_none` for fallback values?
69. How does the `slice` filter work with lists?
70. How do you use `dictsortreversed` to reverse sort dictionaries?
71. What does the `wordwrap` filter do?
72. How do you use `truncatewords_html` to shorten HTML content?
73. What does the `timeuntil` filter do?
74. How do you use `timesince` to calculate elapsed time?
75. What does the `center` filter do?
76. How do you use `rjust` and `ljust` for spacing?
77. What does the `cut` filter do?
78. How do you use `length_is` to validate list length?
79. How does the `random` filter work with lists?
80. How do you use `filesizeformat` to show human-readable sizes?















# Django Quiz - فصل نهم

## سوالات

1. هدف اصلی استفاده از قالب‌های Django چیست؟
2. تفاوت بین `render()` و `HttpResponse()` در چیست؟
3. چگونه می‌توان متغیرها را در قالب‌های Django نمایش داد؟
4. تگ `{% for %}` در قالب‌ها چه کاربردی دارد؟
5. چگونه می‌توان شرطی در قالب Django نوشت؟
6. تگ `{% include %}` چه کاری انجام می‌دهد؟
7. چگونه می‌توان از فیلتر `date` در قالب استفاده کرد؟
8. تفاوت بین `{{ variable }}` و `{% tag %}` چیست؟
9. چگونه می‌توان قالب پایه (base template) تعریف کرد؟
10. تگ `{% block %}` چه کاربردی دارد؟
11. چگونه می‌توان قالب‌ها را تو در تو استفاده کرد؟
12. فیلتر `length` در قالب‌ها چه کاری انجام می‌دهد؟
13. چگونه می‌توان از `ifchanged` در قالب استفاده کرد؟
14. تگ `{% csrf_token %}` در فرم‌ها چه کاربردی دارد؟
15. چگونه می‌توان فرم را در قالب به‌صورت HTML نمایش داد؟
16. تفاوت بین `{{ form.as_p }}` و `{{ form.as_table }}` چیست؟
17. چگونه می‌توان از کلاس‌های CSS در فرم‌های Django استفاده کرد؟
18. چگونه می‌توان خطاهای فرم را در قالب نمایش داد؟
19. تگ `{% url %}` برای چه استفاده می‌شود؟
20. چگونه می‌توان از متغیرهای context در قالب استفاده کرد؟
21. فیلتر `default` در قالب‌ها چه کاربردی دارد؟
22. چگونه می‌توان از `extends` برای ارث‌بری قالب استفاده کرد؟
23. تگ `{% comment %}` چه کاربردی دارد؟
24. چگونه می‌توان از حلقه `forloop.counter` استفاده کرد؟
25. فیلتر `truncatechars` چه کاری انجام می‌دهد؟
26. چگونه می‌توان از `safe` برای جلوگیری از escape شدن HTML استفاده کرد؟
27. تگ `{% static %}` در قالب‌ها چه کاربردی دارد؟
28. چگونه می‌توان فایل‌های CSS و JS را در قالب بارگذاری کرد؟
29. چگونه می‌توان از شرط `if` با `and` و `or` استفاده کرد؟
30. فیلتر `join` در قالب‌ها چه کاربردی دارد؟
31. چگونه می‌توان از `with` برای تعریف متغیر موقت استفاده کرد؟
32. تگ `{% cycle %}` چه کاربردی دارد؟
33. چگونه می‌توان از `add` برای جمع کردن عددها استفاده کرد؟
34. فیلتر `slice` در قالب‌ها چه کاری انجام می‌دهد؟
35. چگونه می‌توان از `pluralize` برای جمع و مفرد استفاده کرد؟
36. تگ `{% regroup %}` چه کاربردی دارد؟
37. چگونه می‌توان از `widthratio` برای محاسبه درصد استفاده کرد؟
38. فیلتر `filesizeformat` چه کاری انجام می‌دهد؟
39. چگونه می‌توان از `yesno` برای نمایش مقدار بولی استفاده کرد؟
40. چگونه می‌توان از `dictsort` برای مرتب‌سازی دیکشنری استفاده کرد؟
41. تگ `{% firstof %}` چه کاربردی دارد؟
42. چگونه می‌توان از `linebreaksbr` برای تبدیل خط جدید به `<br>` استفاده کرد؟
43. فیلتر `wordcount` چه کاری انجام می‌دهد؟
44. چگونه می‌توان از `random` برای انتخاب تصادفی استفاده کرد؟
45. فیلتر `title` چه کاربردی دارد؟
46. چگونه می‌توان از `capfirst` برای بزرگ کردن حرف اول استفاده کرد؟
47. فیلتر `lower` و `upper` چه کاری انجام می‌دهند؟
48. چگونه می‌توان از `length_is` برای بررسی طول استفاده کرد؟
49. تگ `{% autoescape off %}` چه کاربردی دارد؟
50. چگونه می‌توان از `divisibleby` برای بررسی بخش‌پذیری استفاده کرد؟
51. فیلتر `time` چه کاری انجام می‌دهد؟
52. چگونه می‌توان از `unordered_list` برای نمایش لیست استفاده کرد؟
53. فیلتر `urlize` چه کاربردی دارد؟
54. چگونه می‌توان از `phone2numeric` برای تبدیل شماره تلفن استفاده کرد؟
55. فیلتر `striptags` چه کاری انجام می‌دهد؟
56. چگونه می‌توان از `truncatewords` برای کوتاه کردن متن استفاده کرد؟
57. فیلتر `iriencode` چه کاربردی دارد؟
58. چگونه می‌توان از `make_list` برای تبدیل رشته به لیست استفاده کرد؟
59. فیلتر `addslashes` چه کاری انجام می‌دهد؟
60. چگونه می‌توان از `escapejs` برای امن‌سازی JavaScript استفاده کرد؟
61. فیلتر `json_script` چه کاربردی دارد؟
62. چگونه می‌توان از `removetags` برای حذف تگ‌ها استفاده کرد؟
63. فیلتر `urlencode` چه کاری انجام می‌دهد؟
64. چگونه می‌توان از `stringformat` برای قالب‌بندی رشته استفاده کرد؟
65. فیلتر `floatformat` چه کاربردی دارد؟
66. چگونه می‌توان از `filesizeformat` برای نمایش حجم فایل استفاده کرد؟
67. فیلتر `linenumbers` چه کاری انجام می‌دهد؟
68. چگونه می‌توان از `default_if_none` برای مقداردهی پیش‌فرض استفاده کرد؟
69. فیلتر `slice` چگونه با لیست‌ها کار می‌کند؟
70. چگونه می‌توان از `dictsortreversed` برای مرتب‌سازی معکوس استفاده کرد؟
71. فیلتر `wordwrap` چه کاربردی دارد؟
72. چگونه می‌توان از `truncatewords_html` برای کوتاه کردن HTML استفاده کرد؟
73. فیلتر `timeuntil` چه کاری انجام می‌دهد؟
74. چگونه می‌توان از `timesince` برای محاسبه زمان گذشته استفاده کرد؟
75. فیلتر `center` چه کاربردی دارد؟
76. چگونه می‌توان از `rjust` و `ljust` برای تنظیم فاصله استفاده کرد؟
77. فیلتر `cut` چه کاری انجام می‌دهد؟
78. چگونه می‌توان از `length_is` برای بررسی دقیق طول استفاده کرد؟
79. فیلتر `random` چگونه با لیست‌ها کار می‌کند؟
80. چگونه می‌توان از `filesizeformat` برای نمایش حجم به‌صورت خوانا استفاده کرد؟
