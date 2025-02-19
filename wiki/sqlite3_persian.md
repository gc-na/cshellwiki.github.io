# [سیستم‌عامل] C Shell (csh) sqlite3 استفاده: اجرای دستورات SQL در پایگاه داده SQLite

## Overview
دستورات `sqlite3` برای تعامل با پایگاه داده SQLite استفاده می‌شوند. این ابزار به شما اجازه می‌دهد تا به راحتی داده‌ها را جستجو، ویرایش و مدیریت کنید.

## Usage
سینتکس پایه دستور `sqlite3` به صورت زیر است:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-header`: نمایش هدرها در نتایج.
- `-csv`: خروجی را به فرمت CSV تبدیل می‌کند.
- `-init <file>`: اجرای دستورات SQL موجود در فایل مشخص شده.
- `-version`: نمایش نسخه sqlite3.

## Common Examples
- **ایجاد یک پایگاه داده جدید:**
  ```bash
  sqlite3 mydatabase.db
  ```

- **اجرای یک دستور SQL:**
  ```bash
  sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
  ```

- **وارد کردن داده‌ها از یک فایل CSV:**
  ```bash
  sqlite3 -csv mydatabase.db ".import mydata.csv users"
  ```

- **نمایش داده‌ها از یک جدول:**
  ```bash
  sqlite3 mydatabase.db "SELECT * FROM users;"
  ```

## Tips
- همیشه از گزینه `-header` برای نمایش هدرها استفاده کنید تا نتایج خواناتر باشند.
- برای ذخیره‌سازی دستورات SQL خود، از گزینه `-init` استفاده کنید.
- قبل از اجرای دستورات تغییرات، از پایگاه داده خود نسخه پشتیبان تهیه کنید.