# [لينكس] Bash sqlite3 الاستخدام: إدارة قواعد البيانات SQLite

## Overview
أداة `sqlite3` هي واجهة سطر الأوامر لقاعدة بيانات SQLite. تتيح لك هذه الأداة إنشاء قواعد بيانات جديدة، وإجراء استعلامات، وتعديل البيانات، وإدارة الجداول، وكل ذلك من خلال سطر الأوامر.

## Usage
تكون الصيغة الأساسية لاستخدام الأمر `sqlite3` كما يلي:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: عرض قائمة بجميع الخيارات المتاحة.
- `-version`: عرض إصدار SQLite المثبت.
- `-init <file>`: تنفيذ الأوامر الموجودة في ملف محدد عند بدء تشغيل sqlite3.
- `-batch`: تشغيل sqlite3 في وضع الدفعة، مما يعني عدم انتظار إدخال المستخدم.

## Common Examples
- **إنشاء قاعدة بيانات جديدة:**
```bash
sqlite3 mydatabase.db
```

- **تنفيذ استعلام SQL:**
```bash
sqlite3 mydatabase.db "SELECT * FROM mytable;"
```

- **إنشاء جدول جديد:**
```bash
sqlite3 mydatabase.db "CREATE TABLE mytable (id INTEGER PRIMARY KEY, name TEXT);"
```

- **إدخال بيانات في الجدول:**
```bash
sqlite3 mydatabase.db "INSERT INTO mytable (name) VALUES ('Alice');"
```

- **عرض جميع البيانات من الجدول:**
```bash
sqlite3 mydatabase.db "SELECT * FROM mytable;"
```

## Tips
- تأكد من استخدام الأوامر الصحيحة لتجنب الأخطاء، خاصة عند التعامل مع البيانات الحساسة.
- استخدم خيار `-init` لتحميل إعدادات أو بيانات أولية عند بدء قاعدة البيانات.
- من الجيد دائمًا إجراء نسخ احتياطية من قواعد البيانات قبل إجراء تغييرات كبيرة.