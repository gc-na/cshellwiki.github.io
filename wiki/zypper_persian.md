# [لینوکس] Bash zypper استفاده: مدیریت بسته‌ها در سیستم‌های OpenSUSE

## Overview
دستورات zypper برای مدیریت بسته‌ها در توزیع‌های لینوکس OpenSUSE و SUSE Linux Enterprise استفاده می‌شود. این ابزار به کاربران اجازه می‌دهد تا نرم‌افزارها را نصب، حذف، به‌روزرسانی و مدیریت کنند.

## Usage
سینتکس پایه دستور zypper به شکل زیر است:

```bash
zypper [options] [arguments]
```

## Common Options
- `install`: نصب یک یا چند بسته.
- `remove`: حذف یک یا چند بسته.
- `update`: به‌روزرسانی بسته‌های نصب‌شده.
- `search`: جستجوی بسته‌ها بر اساس نام یا توضیحات.
- `info`: نمایش اطلاعات مربوط به یک بسته خاص.
- `refresh`: به‌روزرسانی فهرست بسته‌ها از مخازن.

## Common Examples
- نصب یک بسته:
  ```bash
  zypper install package-name
  ```

- حذف یک بسته:
  ```bash
  zypper remove package-name
  ```

- به‌روزرسانی همه بسته‌ها:
  ```bash
  zypper update
  ```

- جستجوی یک بسته:
  ```bash
  zypper search package-name
  ```

- نمایش اطلاعات یک بسته:
  ```bash
  zypper info package-name
  ```

- به‌روزرسانی فهرست بسته‌ها:
  ```bash
  zypper refresh
  ```

## Tips
- همیشه قبل از نصب یا به‌روزرسانی بسته‌ها، از گزینه `refresh` استفاده کنید تا مطمئن شوید فهرست بسته‌ها به‌روز است.
- برای حذف بسته‌ها، از گزینه `remove` با احتیاط استفاده کنید تا از حذف بسته‌های وابسته جلوگیری شود.
- می‌توانید از گزینه `-y` برای تأیید خودکار عملیات استفاده کنید، به عنوان مثال:
  ```bash
  zypper install -y package-name
  ```