# [لینوکس] C Shell (csh) lvextend استفاده: افزایش اندازه لایه منطقی

## Overview
دستور `lvextend` برای افزایش اندازه لایه‌های منطقی (Logical Volumes) در سیستم‌های مدیریت حجم منطقی (LVM) استفاده می‌شود. این دستور به کاربران این امکان را می‌دهد که فضای بیشتری به لایه‌های منطقی خود اضافه کنند.

## Usage
سینتکس پایه دستور `lvextend` به صورت زیر است:

```csh
lvextend [options] [arguments]
```

## Common Options
- `-L +size`: افزایش اندازه لایه منطقی به اندازه مشخص شده.
- `-l +number`: افزایش اندازه لایه منطقی بر اساس تعداد واحدهای منطقی.
- `-r`: پس از افزایش اندازه، سیستم فایل را به طور خودکار گسترش می‌دهد.

## Common Examples
- افزایش اندازه لایه منطقی به 10 گیگابایت:
  ```csh
  lvextend -L +10G /dev/vgname/lvname
  ```

- افزایش اندازه لایه منطقی به 5 واحد منطقی:
  ```csh
  lvextend -l +5 /dev/vgname/lvname
  ```

- افزایش اندازه لایه منطقی و گسترش سیستم فایل به طور خودکار:
  ```csh
  lvextend -r -L +10G /dev/vgname/lvname
  ```

## Tips
- قبل از استفاده از `lvextend`، حتماً از لایه منطقی خود نسخه پشتیبان تهیه کنید.
- بررسی کنید که فضای کافی در گروه حجم (Volume Group) برای افزایش اندازه لایه منطقی وجود دارد.
- پس از افزایش اندازه، از دستور `df -h` برای بررسی فضای جدید استفاده کنید.