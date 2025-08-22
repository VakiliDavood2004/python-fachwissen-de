# Django Quiz – Kapitel 9: Lösungen

## Antworten

1. Django-Templates dienen dazu, HTML mit dynamischen Daten zu kombinieren.
2. `render()` erstellt eine vollständige HTTP-Antwort mit Template, während `HttpResponse()` nur rohen Text zurückgibt.
3. Mit `{{ variable }}` kann man Variablen direkt im Template anzeigen.
4. `{% for %}` wird verwendet, um über Listen oder QuerySets zu iterieren.
5. Mit `{% if %}` kann man Bedingungen im Template schreiben.
6. `{% include %}` fügt ein anderes Template in das aktuelle ein.
7. Der `date`-Filter formatiert Datumswerte, z. B. `{{ date|date:"d.m.Y" }}`.
8. `{{ variable }}` zeigt Daten an, `{% tag %}` führt Logik aus.
9. Ein Basis-Template enthält gemeinsame Layouts und wird mit `{% extends "base.html" %}` verwendet.
10. `{% block %}` definiert Bereiche, die von untergeordneten Templates überschrieben werden können.
11. Man kann Templates verschachteln, indem man `extends` und `include` kombiniert.
12. `length` gibt die Anzahl der Elemente in einer Liste oder Zeichen in einem String zurück.
13. `ifchanged` prüft, ob sich ein Wert im Loop geändert hat.
14. `{% csrf_token %}` schützt Formulare vor Cross-Site-Request-Forgery.
15. Mit `{{ form.as_p }}` oder `{{ form.as_table }}` wird das Formular als HTML gerendert.
16. `as_p` zeigt Felder in `<p>`-Tags, `as_table` in Tabellenform.
17. CSS-Klassen können über Widgets im Formularfeld definiert werden.
18. Mit `{{ form.errors }}` oder `{{ field.errors }}` zeigt man Fehler an.
19. `{% url 'name' %}` erzeugt eine URL basierend auf dem Namen der View.
20. Kontextvariablen werden beim Rendern des Templates übergeben.
21. `default` zeigt einen Ersatzwert, wenn die Variable leer ist.
22. `extends` erlaubt es, von einem Basis-Template zu erben.
23. `{% comment %}` ignoriert den Inhalt im Template.
24. `forloop.counter` zählt die aktuelle Iteration ab 1.
25. `truncatechars` kürzt einen String auf eine bestimmte Anzahl von Zeichen.
26. `safe` verhindert das automatische Escaping von HTML.
27. `{% static %}` wird verwendet, um den Pfad zu statischen Dateien zu erzeugen.
28. CSS/JS-Dateien werden mit `{% load static %}` und `<link>`/`<script>` eingebunden.
29. Bedingungen mit `and`/`or` werden innerhalb von `{% if %}` geschrieben.
30. `join` verbindet Listenelemente zu einem String.
31. `with` definiert temporäre Variablen im Template.
32. `cycle` wechselt zwischen Werten, z. B. für abwechselnde Farben.
33. `add` addiert Zahlen oder Strings.
34. `slice` schneidet Listen oder Strings, z. B. `{{ list|slice:":3" }}`.
35. `pluralize` hängt ein Suffix an, wenn die Anzahl > 1 ist.
36. `regroup` gruppiert Objekte nach einem gemeinsamen Attribut.
37. `widthratio` berechnet ein Verhältnis, z. B. für Balkendiagramme.
38. `filesizeformat` zeigt Dateigrößen in lesbarem Format (z. B. MB).
39. `yesno` zeigt unterschiedliche Texte für `True`/`False`.
40. `dictsort` sortiert Dictionaries nach einem Schlüssel.
41. `firstof` zeigt den ersten nicht-leeren Wert aus einer Liste.
42. `linebreaksbr` ersetzt Zeilenumbrüche durch `<br>`-Tags.
43. `wordcount` zählt die Wörter in einem String.
44. `random` wählt ein zufälliges Element aus einer Liste.
45. `title` wandelt einen String in Titel-Schreibweise um.
46. `capfirst` macht den ersten Buchstaben eines Strings groß.
47. `lower` wandelt in Kleinbuchstaben, `upper` in Großbuchstaben.
48. `length_is` prüft, ob die Länge einem bestimmten Wert entspricht.
49. `autoescape off` deaktiviert das automatische HTML-Escaping.
50. `divisibleby` prüft, ob eine Zahl durch eine andere teilbar ist.
51. `time` formatiert Zeitwerte.
52. `unordered_list` zeigt verschachtelte Listen als HTML.
53. `urlize` wandelt URLs im Text in klickbare Links um.
54. `phone2numeric` ersetzt Buchstaben in Telefonnummern durch Zahlen.
55. `striptags` entfernt alle HTML-Tags aus einem String.
56. `truncatewords` kürzt Text auf eine bestimmte Anzahl von Wörtern.
57. `iriencode` kodiert URLs für internationale Zeichen.
58. `make_list` wandelt einen String in eine Liste von Zeichen um.
59. `addslashes` fügt Escape-Zeichen hinzu.
60. `escapejs` sichert Strings für die Verwendung in JavaScript.
61. `json_script` bettet JSON-Daten sicher in HTML ein.
62. `removetags` entfernt bestimmte HTML-Tags.
63. `urlencode` kodiert einen String für die Verwendung in URLs.
64. `stringformat` formatiert Zahlen oder Strings nach einem Muster.
65. `floatformat` rundet Dezimalzahlen auf eine bestimmte Anzahl von Stellen.
66. `filesizeformat` zeigt Dateigrößen in MB/KB an.
67. `linenumbers` fügt Zeilennummern zu einem Text hinzu.
68. `default_if_none` ersetzt `None` durch einen Standardwert.
69. `slice` funktioniert mit Listen wie bei Strings.
70. `dictsortreversed` sortiert Dictionaries in umgekehrter Reihenfolge.
71. `wordwrap` bricht lange Texte nach einer bestimmten Breite um.
72. `truncatewords_html` kürzt HTML-Inhalte ohne Tags zu zerstören.
73. `timeuntil` zeigt die verbleibende Zeit bis zu einem Datum.
74. `timesince` zeigt die vergangene Zeit seit einem Datum.
75. `center` zentriert einen String mit Leerzeichen.
76. `rjust` und `ljust` richten Strings rechts oder links aus.
77. `cut` entfernt bestimmte Zeichen aus einem String.
78. `length_is` prüft die exakte Länge einer Liste oder eines Strings.
79. `random` funktioniert mit Listen und gibt ein zufälliges Element zurück.
80. `filesizeformat` zeigt Dateigrößen in menschenlesbarem Format.







# Django Quiz – Chapter 9: Answers

## Answers

1. Django templates are used to combine HTML with dynamic data.
2. `render()` returns a complete HTTP response with a template, while `HttpResponse()` returns plain text.
3. You can display variables directly in the template using `{{ variable }}`.
4. `{% for %}` is used to iterate over lists or QuerySets.
5. `{% if %}` is used to write conditional logic in templates.
6. `{% include %}` inserts another template into the current one.
7. The `date` filter formats date values, e.g., `{{ date|date:"d.m.Y" }}`.
8. `{{ variable }}` displays data, `{% tag %}` executes logic.
9. A base template contains shared layouts and is used with `{% extends "base.html" %}`.
10. `{% block %}` defines sections that can be overridden by child templates.
11. Templates can be nested by combining `extends` and `include`.
12. `length` returns the number of items in a list or characters in a string.
13. `ifchanged` checks if a value has changed during a loop.
14. `{% csrf_token %}` protects forms from cross-site request forgery.
15. Forms are rendered as HTML using `{{ form.as_p }}` or `{{ form.as_table }}`.
16. `as_p` displays fields in `<p>` tags, `as_table` in table format.
17. CSS classes can be defined via widgets in the form field.
18. Errors are displayed using `{{ form.errors }}` or `{{ field.errors }}`.
19. `{% url 'name' %}` generates a URL based on the view name.
20. Context variables are passed when rendering the template.
21. `default` provides a fallback value if the variable is empty.
22. `extends` allows inheritance from a base template.
23. `{% comment %}` ignores the content inside the tag.
24. `forloop.counter` counts the current iteration starting from 1.
25. `truncatechars` shortens a string to a specific number of characters.
26. `safe` prevents automatic HTML escaping.
27. `{% static %}` is used to generate the path to static files.
28. CSS/JS files are included using `{% load static %}` and `<link>`/`<script>` tags.
29. Conditions with `and`/`or` are written inside `{% if %}`.
30. `join` combines list elements into a string.
31. `with` defines temporary variables in the template.
32. `cycle` alternates between values, e.g., for alternating colors.
33. `add` adds numbers or strings.
34. `slice` slices lists or strings, e.g., `{{ list|slice:":3" }}`.
35. `pluralize` appends a suffix if the count is greater than 1.
36. `regroup` groups objects by a common attribute.
37. `widthratio` calculates a ratio, e.g., for bar charts.
38. `filesizeformat` displays file sizes in readable format (e.g., MB).
39. `yesno` displays different text for `True`/`False`.
40. `dictsort` sorts dictionaries by a key.
41. `firstof` displays the first non-empty value from a list.
42. `linebreaksbr` replaces line breaks with `<br>` tags.
43. `wordcount` counts the words in a string.
44. `random` selects a random item from a list.
45. `title` converts a string to title case.
46. `capfirst` capitalizes the first letter of a string.
47. `lower` converts to lowercase, `upper` to uppercase.
48. `length_is` checks if the length matches a specific value.
49. `autoescape off` disables automatic HTML escaping.
50. `divisibleby` checks if a number is divisible by another.
51. `time` formats time values.
52. `unordered_list` displays nested lists as HTML.
53. `urlize` converts URLs in text into clickable links.
54. `phone2numeric` replaces letters in phone numbers with digits.
55. `striptags` removes all HTML tags from a string.
56. `truncatewords` shortens text to a specific number of words.
57. `iriencode` encodes URLs for international characters.
58. `make_list` converts a string into a list of characters.
59. `addslashes` adds escape characters.
60. `escapejs` secures strings for use in JavaScript.
61. `json_script` safely embeds JSON data into HTML.
62. `removetags` removes specific HTML tags.
63. `urlencode` encodes a string for use in URLs.
64. `stringformat` formats numbers or strings using a pattern.
65. `floatformat` rounds decimal numbers to a specific number of places.
66. `filesizeformat` displays file sizes in MB/KB.
67. `linenumbers` adds line numbers to a text.
68. `default_if_none` replaces `None` with a default value.
69. `slice` works with lists just like with strings.
70. `dictsortreversed` sorts dictionaries in reverse order.
71. `wordwrap` wraps long text after a specific width.
72. `truncatewords_html` shortens HTML content without breaking tags.
73. `timeuntil` shows the remaining time until a date.
74. `timesince` shows the time passed since a date.
75. `center` centers a string with spaces.
76. `rjust` and `ljust` align strings to the right or left.
77. `cut` removes specific characters from a string.
78. `length_is` checks the exact length of a list or string.
79. `random` works with lists and returns a random element.
80. `filesizeformat` displays file sizes in a human-readable format.






# آزمون Django – فصل نهم: پاسخ‌ها

## پاسخ‌ها

1. قالب‌های Django برای ترکیب HTML با داده‌های پویا استفاده می‌شوند.
2. `render()` یک پاسخ کامل HTTP همراه با قالب تولید می‌کند، در حالی که `HttpResponse()` فقط متن خام را برمی‌گرداند.
3. با استفاده از `{{ variable }}` می‌توان متغیرها را مستقیماً در قالب نمایش داد.
4. از `{% for %}` برای پیمایش لیست‌ها یا QuerySetها استفاده می‌شود.
5. با `{% if %}` می‌توان شرط‌ها را در قالب نوشت.
6. `{% include %}` یک قالب دیگر را در قالب فعلی وارد می‌کند.
7. فیلتر `date` برای قالب‌بندی تاریخ‌ها استفاده می‌شود، مثلاً `{{ date|date:"d.m.Y" }}`.
8. `{{ variable }}` برای نمایش داده‌ها و `{% tag %}` برای اجرای منطق استفاده می‌شود.
9. قالب پایه شامل ساختار مشترک است و با `{% extends "base.html" %}` استفاده می‌شود.
10. `{% block %}` بخش‌هایی را تعریف می‌کند که قالب‌های فرزند می‌توانند آن‌ها را بازنویسی کنند.
11. قالب‌های تو در تو با ترکیب `extends` و `include` ساخته می‌شوند.
12. `length` تعداد عناصر یک لیست یا تعداد کاراکترهای یک رشته را برمی‌گرداند.
13. `ifchanged` بررسی می‌کند که آیا مقدار در طول حلقه تغییر کرده است یا نه.
14. `{% csrf_token %}` فرم‌ها را در برابر حملات CSRF محافظت می‌کند.
15. فرم‌ها با استفاده از `{{ form.as_p }}` یا `{{ form.as_table }}` به HTML تبدیل می‌شوند.
16. `as_p` فیلدها را در تگ‌های `<p>` و `as_table` در قالب جدول نمایش می‌دهد.
17. کلاس‌های CSS از طریق ویجت‌ها در فیلدهای فرم تعریف می‌شوند.
18. خطاها با استفاده از `{{ form.errors }}` یا `{{ field.errors }}` نمایش داده می‌شوند.
19. `{% url 'name' %}` یک URL بر اساس نام view تولید می‌کند.
20. متغیرهای context هنگام رندر قالب ارسال می‌شوند.
21. `default` مقدار پیش‌فرض را در صورت خالی بودن متغیر ارائه می‌دهد.
22. `extends` امکان ارث‌بری از قالب پایه را فراهم می‌کند.
23. `{% comment %}` محتوای داخل تگ را نادیده می‌گیرد.
24. `forloop.counter` شماره حلقه را از ۱ شروع می‌کند.
25. `truncatechars` رشته را به تعداد مشخصی از کاراکترها کوتاه می‌کند.
26. `safe` از escape شدن HTML جلوگیری می‌کند.
27. `{% static %}` برای تولید مسیر فایل‌های ایستا استفاده می‌شود.
28. فایل‌های CSS و JS با `{% load static %}` و تگ‌های `<link>` یا `<script>` بارگذاری می‌شوند.
29. شرط‌های ترکیبی با `and` و `or` درون `{% if %}` نوشته می‌شوند.
30. `join` عناصر لیست را به یک رشته تبدیل می‌کند.
31. `with` متغیرهای موقت را در قالب تعریف می‌کند.
32. `cycle` بین مقادیر مختلف جابه‌جا می‌شود، مثلاً برای رنگ‌های متناوب.
33. `add` برای جمع کردن اعداد یا رشته‌ها استفاده می‌شود.
34. `slice` برای بریدن لیست‌ها یا رشته‌ها استفاده می‌شود، مثلاً `{{ list|slice:":3" }}`.
35. `pluralize` در صورت بیشتر بودن تعداد، پسوند جمع اضافه می‌کند.
36. `regroup` اشیاء را بر اساس ویژگی مشترک گروه‌بندی می‌کند.
37. `widthratio` نسبت‌ها را محاسبه می‌کند، مثلاً برای نمودارهای میله‌ای.
38. `filesizeformat` اندازه فایل را به صورت خوانا (مثلاً MB) نمایش می‌دهد.
39. `yesno` متن‌های متفاوتی برای `True` و `False` نمایش می‌دهد.
40. `dictsort` دیکشنری‌ها را بر اساس کلید مرتب می‌کند.
41. `firstof` اولین مقدار غیرخالی را از لیست نمایش می‌دهد.
42. `linebreaksbr` خط‌های جدید را به تگ `<br>` تبدیل می‌کند.
43. `wordcount` تعداد کلمات یک رشته را می‌شمارد.
44. `random` یک عنصر تصادفی از لیست انتخاب می‌کند.
45. `title` رشته را به حالت عنوان تبدیل می‌کند.
46. `capfirst` حرف اول رشته را بزرگ می‌کند.
47. `lower` رشته را به حروف کوچک و `upper` به حروف بزرگ تبدیل می‌کند.
48. `length_is` بررسی می‌کند که طول دقیقاً برابر مقدار مشخصی باشد.
49. `autoescape off` escape خودکار HTML را غیرفعال می‌کند.
50. `divisibleby` بررسی می‌کند که آیا عددی بر عدد دیگر بخش‌پذیر است.
51. `time` زمان را قالب‌بندی می‌کند.
52. `unordered_list` لیست‌های تو در تو را به صورت HTML نمایش می‌دهد.
53. `urlize` لینک‌های موجود در متن را قابل کلیک می‌کند.
54. `phone2numeric` حروف موجود در شماره تلفن را به عدد تبدیل می‌کند.
55. `striptags` تمام تگ‌های HTML را از رشته حذف می‌کند.
56. `truncatewords` متن را به تعداد مشخصی از کلمات کوتاه می‌کند.
57. `iriencode` URLها را برای کاراکترهای بین‌المللی رمزگذاری می‌کند.
58. `make_list` رشته را به لیستی از کاراکترها تبدیل می‌کند.
59. `addslashes` کاراکترهای escape را اضافه می‌کند.
60. `escapejs` رشته‌ها را برای استفاده در JavaScript امن می‌کند.
61. `json_script` داده‌های JSON را به‌صورت امن در HTML قرار می‌دهد.
62. `removetags` تگ‌های خاص HTML را حذف می‌کند.
63. `urlencode` رشته را برای استفاده در URL رمزگذاری می‌کند.
64. `stringformat` رشته یا عدد را طبق الگو قالب‌بندی می‌کند.
65. `floatformat` اعداد اعشاری را به تعداد مشخصی از رقم‌ها گرد می‌کند.
66. `filesizeformat` اندازه فایل را به صورت KB یا MB نمایش می‌دهد.
67. `linenumbers` شماره خط را به متن اضافه می‌کند.
68. `default_if_none` مقدار `None` را با مقدار پیش‌فرض جایگزین می‌کند.
69. `slice` با لیست‌ها همانند رشته‌ها کار می‌کند.
70. `dictsortreversed` دیکشنری‌ها را به صورت معکوس مرتب می‌کند.
71. `wordwrap` متن‌های طولانی را پس از عرض مشخصی می‌شکند.
72. `truncatewords_html` محتوای HTML را بدون آسیب به تگ‌ها کوتاه می‌کند.
73. `timeuntil` زمان باقی‌مانده تا یک تاریخ را نمایش می‌دهد.
74. `timesince` زمان گذشته از یک تاریخ را نمایش می‌دهد.
75. `center` رشته را با فاصله در وسط قرار می‌دهد.
76. `rjust` و `ljust` رشته را به راست یا چپ تراز می‌کنند.
77. `cut` کاراکترهای خاص را از رشته حذف می‌کند.
78. `length_is` طول دقیق لیست یا رشته را بررسی می‌کند.
79. `random` با لیست‌ها کار می‌کند و یک عنصر تصادفی برمی‌گرداند.
80. `filesizeformat` اندازه فایل را به صورت قابل خواندن برای انسان نمایش می‌دهد.
