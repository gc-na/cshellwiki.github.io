# [لینوکس] Bash timedatectl استفاده: تنظیم و مشاهده تاریخ و زمان سیستم

## Overview
دستور `timedatectl` برای مشاهده و تنظیم تاریخ و زمان سیستم در سیستم‌عامل‌های مبتنی بر لینوکس استفاده می‌شود. این ابزار به کاربران این امکان را می‌دهد که زمان محلی، زمان جهانی (UTC) و تنظیمات ناحیه زمانی را مدیریت کنند.

## Usage
سینتکس پایه دستور `timedatectl` به صورت زیر است:

```bash
timedatectl [options] [arguments]
```

## Common Options
- `status`: نمایش وضعیت فعلی تاریخ و زمان.
- `set-time <time>`: تنظیم تاریخ و زمان به مقدار مشخص شده.
- `set-timezone <zone>`: تنظیم ناحیه زمانی به مقدار مشخص شده.
- `list-timezones`: نمایش لیست تمام نواحی زمانی قابل دسترسی.
- `set-ntp <boolean>`: فعال یا غیرفعال کردن همگام‌سازی زمان با سرور NTP.

## Common Examples
- **نمایش وضعیت فعلی تاریخ و زمان:**
  ```bash
  timedatectl status
  ```

- **تنظیم تاریخ و زمان:**
  ```bash
  timedatectl set-time '2023-10-01 12:00:00'
  ```

- **تنظیم ناحیه زمانی:**
  ```bash
  timedatectl set-timezone Asia/Tehran
  ```

- **نمایش لیست نواحی زمانی:**
  ```bash
  timedatectl list-timezones
  ```

- **فعال کردن همگام‌سازی NTP:**
  ```bash
  timedatectl set-ntp true
  ```

## Tips
- همیشه قبل از تنظیم تاریخ و زمان، وضعیت فعلی را با `timedatectl status` بررسی کنید.
- برای جلوگیری از مشکلات همگام‌سازی، بهتر است NTP را فعال کنید.
- در صورت نیاز به تغییر ناحیه زمانی، از گزینه `list-timezones` برای یافتن ناحیه مناسب استفاده کنید.