# [لينكس] Bash systemctl الاستخدام: إدارة الخدمات في النظام

## Overview
يعتبر أمر `systemctl` أداة قوية لإدارة الخدمات والعمليات في أنظمة التشغيل التي تعتمد على نظام `systemd`. يتيح لك هذا الأمر بدء وإيقاف وتفعيل وتعطيل الخدمات، وكذلك التحقق من حالة النظام.

## Usage
تتمثل الصيغة الأساسية لأمر `systemctl` في:

```bash
systemctl [options] [arguments]
```

## Common Options
- `start`: بدء خدمة معينة.
- `stop`: إيقاف خدمة معينة.
- `restart`: إعادة تشغيل خدمة معينة.
- `status`: عرض حالة خدمة معينة.
- `enable`: تفعيل خدمة لتبدأ تلقائيًا عند تشغيل النظام.
- `disable`: تعطيل خدمة بحيث لا تبدأ تلقائيًا عند تشغيل النظام.

## Common Examples
- لبدء خدمة `nginx`:
    ```bash
    systemctl start nginx
    ```

- لإيقاف خدمة `nginx`:
    ```bash
    systemctl stop nginx
    ```

- لإعادة تشغيل خدمة `nginx`:
    ```bash
    systemctl restart nginx
    ```

- للتحقق من حالة خدمة `nginx`:
    ```bash
    systemctl status nginx
    ```

- لتفعيل خدمة `nginx` عند بدء تشغيل النظام:
    ```bash
    systemctl enable nginx
    ```

- لتعطيل خدمة `nginx` من البدء تلقائيًا:
    ```bash
    systemctl disable nginx
    ```

## Tips
- تأكد من استخدام الأمر `systemctl` مع صلاحيات الجذر (root) عند إدارة الخدمات.
- استخدم الأمر `status` بشكل دوري للتحقق من حالة الخدمات المهمة.
- يمكنك استخدام `systemctl list-units --type=service` لعرض جميع الخدمات المتاحة وحالتها.