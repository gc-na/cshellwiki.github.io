# [لينكس] Bash flatpak الاستخدام: إدارة التطبيقات بسهولة

## Overview
أداة `flatpak` هي نظام لتوزيع التطبيقات يسمح بتثبيت التطبيقات وإدارتها بشكل معزول عن النظام الأساسي. يتيح لك `flatpak` تشغيل التطبيقات في بيئة مستقلة، مما يسهل عملية التثبيت والتحديث.

## Usage
التركيب الأساسي لأمر `flatpak` هو:

```bash
flatpak [options] [arguments]
```

## Common Options
- `install`: لتثبيت تطبيق.
- `remove`: لإزالة تطبيق.
- `update`: لتحديث التطبيقات المثبتة.
- `list`: لعرض التطبيقات المثبتة.
- `run`: لتشغيل تطبيق مثبت.

## Common Examples
- لتثبيت تطبيق:
```bash
flatpak install flathub org.example.AppName
```

- لإزالة تطبيق:
```bash
flatpak remove org.example.AppName
```

- لتحديث التطبيقات المثبتة:
```bash
flatpak update
```

- لعرض التطبيقات المثبتة:
```bash
flatpak list
```

- لتشغيل تطبيق:
```bash
flatpak run org.example.AppName
```

## Tips
- تأكد من إضافة مستودعات `flatpak` المناسبة مثل `flathub` للحصول على مجموعة واسعة من التطبيقات.
- استخدم الأمر `flatpak info` للحصول على معلومات تفصيلية حول تطبيق معين.
- تحقق من تحديثات التطبيقات بانتظام لضمان الحصول على أحدث الميزات والإصلاحات.