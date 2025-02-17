# [لينكس] Bash dig الاستخدام: استعلام عن معلومات DNS

## Overview
أداة `dig` هي اختصار لـ "Domain Information Groper"، وتستخدم لاستعلام معلومات نظام أسماء النطاقات (DNS). تتيح لك `dig` الحصول على معلومات مفصلة حول النطاقات، بما في ذلك عناوين IP، سجلات MX، وسجلات TXT.

## Usage
الصيغة الأساسية لأمر `dig` هي:

```bash
dig [options] [arguments]
```

## Common Options
- `@server`: تحديد خادم DNS معين للاستعلام.
- `-t type`: تحديد نوع السجل المطلوب (مثل A، MX، TXT).
- `+short`: عرض النتائج بشكل مختصر.
- `+trace`: تتبع مسار الاستعلام عبر خوادم DNS.

## Common Examples
- **استعلام عن عنوان IP لنطاق معين:**
  ```bash
  dig example.com
  ```

- **استعلام عن سجلات MX لنطاق:**
  ```bash
  dig example.com -t MX
  ```

- **استعلام عن سجل TXT:**
  ```bash
  dig example.com -t TXT
  ```

- **استخدام خادم DNS محدد:**
  ```bash
  dig @8.8.8.8 example.com
  ```

- **عرض النتائج بشكل مختصر:**
  ```bash
  dig example.com +short
  ```

## Tips
- استخدم الخيار `+trace` لفهم كيفية استعلام DNS عبر الخوادم المختلفة.
- تأكد من استخدام خادم DNS موثوق للحصول على نتائج دقيقة.
- يمكنك دمج `dig` مع أدوات أخرى مثل `grep` لتصفية النتائج حسب الحاجة.