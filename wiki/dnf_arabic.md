# [لينكس] Bash dnf الاستخدام: إدارة الحزم في توزيعات لينكس

## Overview
يعتبر أمر `dnf` (Dandified YUM) أداة قوية لإدارة الحزم في توزيعات لينكس، حيث يتيح للمستخدمين تثبيت، تحديث، وإزالة الحزم بسهولة. يُستخدم بشكل أساسي في توزيعات مثل Fedora وRHEL وCentOS.

## Usage
تكون الصيغة الأساسية لأمر `dnf` كما يلي:

```bash
dnf [options] [arguments]
```

## Common Options
- `install`: لتثبيت حزمة جديدة.
- `remove`: لإزالة حزمة مثبتة.
- `update`: لتحديث الحزم المثبتة إلى أحدث إصدار.
- `search`: للبحث عن حزمة معينة.
- `list`: لعرض قائمة الحزم المثبتة أو المتاحة.

## Common Examples
- لتثبيت حزمة:
  ```bash
  dnf install package_name
  ```

- لإزالة حزمة:
  ```bash
  dnf remove package_name
  ```

- لتحديث جميع الحزم المثبتة:
  ```bash
  dnf update
  ```

- للبحث عن حزمة:
  ```bash
  dnf search package_name
  ```

- لعرض قائمة الحزم المثبتة:
  ```bash
  dnf list installed
  ```

## Tips
- تأكد من تحديث قاعدة بيانات الحزم بانتظام باستخدام `dnf update`.
- استخدم `dnf info package_name` للحصول على معلومات تفصيلية حول حزمة معينة.
- يمكنك استخدام `dnf history` لمراجعة العمليات السابقة التي تم تنفيذها بواسطة `dnf`.