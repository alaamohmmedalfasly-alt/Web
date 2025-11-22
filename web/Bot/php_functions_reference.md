# دليل شامل لدوال PHP

سيتم تنظيم الدليل كالتالي:
- دوال النصوص (String Functions)
- دوال المصفوفات (Array Functions)
- دوال الملفات (File Functions)
- دوال التاريخ والوقت (Date & Time)
- دوال قواعد البيانات
- دوال الشبكات (cURL)
- دوال JSON
- دوال الجلسات (Sessions)
- دوال الصور (GD)
- دوال النظام
- دوال البرمجة الكائنية OOP
- دوال وأوامر الامتدادات (mysqli, PDO, curl, mbstring, intl…)

---

## ✨ دوال النصوص (String Functions)

### **strlen()**
ترجع طول النص.

**مثال:**
```php
echo strlen("Hello"); // 5
```

### **strtoupper()**
تحويل الحروف إلى كبيرة.
```php
echo strtoupper("php"); // PHP
```

### **strtolower()**
تحويل الحروف إلى صغيرة.
```php
echo strtolower("PHP"); // php
```

### **substr()**
إرجاع جزء من نص.
```php
echo substr("Hello", 1, 3); // ell
```

### **str_replace()**
استبدال جزء من نص.
```php
echo str_replace("Hi", "Hello", "Hi Alaa");
```

### **strpos()**
البحث عن أول ظهور لنص داخل نص.
```php
echo strpos("Hello", "l"); // 2
```

### **trim()**
إزالة المسافات الزائدة من البداية والنهاية.
```php
trim("  hi  "); // "hi"
```

---

## 🧩 دوال المصفوفات (Array Functions)

### **count()**
عدد عناصر المصفوفة.
```php
echo count([1,2,3]);
```

### **array_push()**
إضافة عنصر لنهاية المصفوفة.
```php
$arr = [1,2];
array_push($arr, 3);
```

### **array_pop()**
حذف آخر عنصر.
```php
array_pop($arr);
```

### **array_merge()**
دمج المصفوفات.
```php
array_merge([1,2], [3,4]);
```

### **array_keys()**
إرجاع المفاتيح فقط.
```php
array_keys(["name"=>"Alaa"]);
```

### **array_values()**
إرجاع القيم فقط.
```php
array_values(["name"=>"Alaa"]);
```

### **in_array()**
فحص وجود قيمة داخل المصفوفة.
```php
in_array(3, [1,2,3]);
```

---

## 📁 دوال الملفات (File Handling)

### **fopen()**
فتح ملف.
### **fwrite()**
الكتابة في ملف.
### **fread()**
القراءة من ملف.
### **file_get_contents()**
قراءة ملف بالكامل.
### **file_put_contents()**
كتابة ملف بالكامل.
### **unlink()**
حذف ملف.

مثال:
```php
file_put_contents("test.txt", "Hello World");
```

---

## 🕒 دوال التاريخ والوقت

### **date()**
إرجاع تاريخ بصيغة معينة.
```php
echo date("Y-m-d H:i:s");
```

### **time()**
الوقت الحالي (ثوانٍ UNIX).
```php
echo time();
```

### **strtotime()**
تحويل نص تاريخ إلى timestamp.
```php
strtotime("next Monday");
```

---

## 🗄️ دوال قواعد البيانات (mysqli & PDO)

### mysqli:
- mysqli_connect()
- mysqli_query()
- mysqli_fetch_assoc()
- mysqli_prepare()
- mysqli_stmt_bind_param()

### PDO:
- new PDO()
- prepare()
- execute()
- fetch()
- fetchAll()

مثال PDO:
```php
$db = new PDO("mysql:host=localhost;dbname=test","root","");
$stmt = $db->prepare("SELECT * FROM users");
$stmt->execute();
$data = $stmt->fetchAll();
```

---

## 🌐 دوال الشبكات (cURL)

### أهم الدوال:
- curl_init()
- curl_setopt()
- curl_exec()
- curl_close()

مثال:
```php
$ch = curl_init("https://example.com");
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
$res = curl_exec($ch);
curl_close($ch);
```

---

## 🧾 دوال JSON

### json_encode()
تحويل مصفوفة إلى JSON.
### json_decode()
تحويل JSON إلى مصفوفة.

```php
json_encode(["name"=>"Alaa"]);
```

---

## 🔐 دوال الجلسات (Sessions)

### session_start()
بدء الجلسة.
### $_SESSION
تخزين بيانات.

```php
session_start();
$_SESSION['name'] = 'Alaa';
```

---

## 🖼️ دوال الصور (GD Library)

- imagecreate()
- imagecolorallocate()
- imagestring()
- imagepng()
- imagedestroy()

---

## 🖥️ دوال النظام

- exec()
- shell_exec()
- phpinfo()
- memory_get_usage()

---

## 🧱 دوال البرمجة الكائنية (OOP)

- class
- public / private / protected
- __construct()
- __destruct()
- inheritance
- interfaces
- traits

مثال:
```php
class User {
    public $name;
    function __construct($n){ $this->name = $n; }
}
```

---

## 📦 دوال الامتدادات (Extensions)

### mysqli
- mysqli_connect
- mysqli_query
- mysqli_fetch_row

### PDO
- prepare
- exec
- fetch

### curl
- curl_init
- curl_setopt

### mbstring
- mb_strlen
- mb_substr

### intl
- Collator
- NumberFormatter

---

## 📌 ملاحظة
إذا رغبت أن أقوم بتوسيع **كل قسم** لتشمل *كل دالة موجودة رسميًا في PHP* مع **شرح مفصل + مثال** — أخبرني وسأكمل لك.

