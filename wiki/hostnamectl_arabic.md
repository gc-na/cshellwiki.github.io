# [لينكس] Bash hostnamectl الاستخدام: إدارة أسماء المضيفين

## Overview
يستخدم الأمر `hostnamectl` لإدارة معلومات النظام المتعلقة باسم المضيف. يمكن من خلاله عرض وتغيير اسم المضيف، بالإضافة إلى إعدادات أخرى مثل اسم النظام ونوع النظام.

## Usage
تكون الصيغة الأساسية للأمر كالتالي:

```bash
hostnamectl [options] [arguments]
```

## Common Options
- `set-hostname`: لتغيير اسم المضيف.
- `status`: لعرض معلومات اسم المضيف الحالي.
- `set-icon-name`: لتعيين اسم أيقونة النظام.
- `set-chassis`: لتحديد نوع الهيكل (مثل "desktop" أو "laptop").
- `set-deployment`: لتحديد نوع النشر (مثل "production" أو "test").

## Common Examples
- **عرض معلومات اسم المضيف الحالي:**
  ```bash
  hostnamectl status
  ```

- **تغيير اسم المضيف إلى "my-new-host":**
  ```bash
  hostnamectl set-hostname my-new-host
  ```

- **تعيين نوع الهيكل إلى "laptop":**
  ```bash
  hostnamectl set-chassis laptop
  ```

- **تعيين اسم أيقونة النظام إلى "computer":**
  ```bash
  hostnamectl set-icon-name computer
  ```

## Tips
- تأكد من أن لديك صلاحيات الجذر (root) عند تغيير اسم المضيف.
- بعد تغيير اسم المضيف، قد تحتاج إلى إعادة تشغيل النظام لتطبيق التغييرات بشكل كامل.
- استخدم الأمر `hostname` بعد التغيير للتحقق من الاسم الجديد.