# [لینوکس] Bash minikube استفاده: مدیریت خوشه‌های Kubernetes محلی

## Overview
دستورات `minikube` برای راه‌اندازی و مدیریت خوشه‌های محلی Kubernetes طراحی شده‌اند. این ابزار به توسعه‌دهندگان این امکان را می‌دهد که به سادگی یک خوشه Kubernetes را در سیستم محلی خود ایجاد و آزمایش کنند.

## Usage
سینتکس پایه دستور `minikube` به صورت زیر است:
```
minikube [options] [arguments]
```

## Common Options
- `start`: برای راه‌اندازی یک خوشه جدید.
- `stop`: برای متوقف کردن خوشه فعلی.
- `status`: برای بررسی وضعیت خوشه.
- `delete`: برای حذف خوشه.
- `dashboard`: برای باز کردن داشبورد Kubernetes در مرورگر.

## Common Examples
- **راه‌اندازی یک خوشه جدید:**
  ```bash
  minikube start
  ```

- **متوقف کردن خوشه فعلی:**
  ```bash
  minikube stop
  ```

- **بررسی وضعیت خوشه:**
  ```bash
  minikube status
  ```

- **حذف خوشه:**
  ```bash
  minikube delete
  ```

- **باز کردن داشبورد Kubernetes:**
  ```bash
  minikube dashboard
  ```

## Tips
- قبل از استفاده از `minikube`، اطمینان حاصل کنید که Virtualization در سیستم شما فعال است.
- برای بهبود عملکرد، می‌توانید از درایورهای مختلف مجازی‌سازی مانند VirtualBox یا Docker استفاده کنید.
- از گزینه `--memory` برای تخصیص حافظه بیشتر به خوشه استفاده کنید، مثلاً:
  ```bash
  minikube start --memory=4096
  ```