# [لینوکس] Bash cryptsetup استفاده: مدیریت رمزگذاری دیسک

## Overview
دستورات `cryptsetup` برای مدیریت رمزگذاری دیسک‌ها و پارتیشن‌ها در سیستم‌های لینوکسی استفاده می‌شود. این ابزار به کاربران این امکان را می‌دهد که دیسک‌های رمزگذاری شده را ایجاد، باز و مدیریت کنند.

## Usage
سینتکس پایه دستور `cryptsetup` به شکل زیر است:

```
cryptsetup [options] [arguments]
```

## Common Options
- `luksFormat`: فرمت کردن یک پارتیشن به فرمت LUKS.
- `luksOpen`: باز کردن یک پارتیشن رمزگذاری شده.
- `luksClose`: بستن یک پارتیشن رمزگذاری شده.
- `status`: نمایش وضعیت یک دیسک رمزگذاری شده.
- `luksAddKey`: افزودن کلید جدید به یک دیسک رمزگذاری شده.

## Common Examples
### فرمت کردن یک پارتیشن به LUKS
```bash
cryptsetup luksFormat /dev/sdX
```

### باز کردن یک دیسک رمزگذاری شده
```bash
cryptsetup luksOpen /dev/sdX my_encrypted_disk
```

### بستن یک دیسک رمزگذاری شده
```bash
cryptsetup luksClose my_encrypted_disk
```

### نمایش وضعیت یک دیسک رمزگذاری شده
```bash
cryptsetup status my_encrypted_disk
```

### افزودن کلید جدید به دیسک رمزگذاری شده
```bash
cryptsetup luksAddKey /dev/sdX
```

## Tips
- همیشه قبل از فرمت کردن یک دیسک، از داده‌های مهم خود پشتیبان تهیه کنید.
- از کلیدهای قوی برای رمزگذاری استفاده کنید تا امنیت داده‌های خود را افزایش دهید.
- برای مدیریت بهتر، نام‌های معناداری برای دیسک‌های رمزگذاری شده انتخاب کنید.