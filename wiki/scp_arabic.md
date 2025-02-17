# [لينكس] Bash scp الاستخدام: نقل الملفات بأمان بين الأنظمة

## Overview
يستخدم أمر `scp` (Secure Copy Protocol) لنقل الملفات بشكل آمن بين الأنظمة عبر الشبكة. يعتمد `scp` على بروتوكول SSH لضمان أمان البيانات أثناء النقل.

## Usage
تكون الصيغة الأساسية لأمر `scp` كما يلي:

```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: لنقل المجلدات بشكل متكرر.
- `-P`: لتحديد رقم منفذ SSH (يجب أن يكون الحرف كبيرًا).
- `-i`: لتحديد ملف المفتاح الخاص عند الاتصال.
- `-v`: لتفعيل وضع التتبع للحصول على معلومات إضافية حول عملية النقل.

## Common Examples
- لنقل ملف من النظام المحلي إلى نظام بعيد:
  ```bash
  scp /path/to/local/file username@remote_host:/path/to/remote/directory
  ```

- لنقل ملف من نظام بعيد إلى النظام المحلي:
  ```bash
  scp username@remote_host:/path/to/remote/file /path/to/local/directory
  ```

- لنقل مجلد كامل من النظام المحلي إلى نظام بعيد:
  ```bash
  scp -r /path/to/local/directory username@remote_host:/path/to/remote/directory
  ```

- لنقل ملف باستخدام منفذ SSH مخصص:
  ```bash
  scp -P 2222 /path/to/local/file username@remote_host:/path/to/remote/directory
  ```

## Tips
- تأكد من أن لديك الأذونات اللازمة على كلا النظامين قبل النقل.
- استخدم الخيار `-v` لتشخيص أي مشاكل قد تواجهها أثناء النقل.
- إذا كنت تستخدم `scp` بشكل متكرر، يمكنك إعداد مفتاح SSH لتسهيل الاتصال بدون الحاجة إلى إدخال كلمة المرور في كل مرة.