# [لینوکس] C Shell (csh) yum استفاده: [مدیریت بسته‌ها]

## Overview
دستورات `yum` (Yellowdog Updater Modified) برای مدیریت بسته‌ها در سیستم‌های مبتنی بر RPM (Red Hat Package Manager) استفاده می‌شود. این ابزار به کاربران اجازه می‌دهد تا نرم‌افزارها را نصب، حذف و به‌روزرسانی کنند.

## Usage
سینتکس پایه دستور `yum` به صورت زیر است:

```
yum [options] [arguments]
```

## Common Options
- `install`: برای نصب یک بسته جدید.
- `remove`: برای حذف یک بسته.
- `update`: برای به‌روزرسانی بسته‌های نصب‌شده.
- `search`: برای جستجوی بسته‌ها.
- `list`: برای نمایش لیست بسته‌های موجود.

## Common Examples
- نصب یک بسته:
  ```bash
  yum install package-name
  ```
  
- حذف یک بسته:
  ```bash
  yum remove package-name
  ```

- به‌روزرسانی یک بسته:
  ```bash
  yum update package-name
  ```

- جستجوی یک بسته:
  ```bash
  yum search package-name
  ```

- نمایش لیست بسته‌های نصب‌شده:
  ```bash
  yum list installed
  ```

## Tips
- همیشه قبل از نصب یا به‌روزرسانی بسته‌ها، از گزینه `check-update` استفاده کنید تا از وجود نسخه‌های جدید مطلع شوید.
- برای به‌روزرسانی تمام بسته‌ها به صورت همزمان، می‌توانید از دستور `yum update` بدون نام بسته استفاده کنید.
- در صورت بروز مشکلات، از گزینه `--skip-broken` برای نادیده گرفتن بسته‌های خراب استفاده کنید.