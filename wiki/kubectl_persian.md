# [لینوکس] Bash kubectl استفاده: مدیریت کلاسترهای Kubernetes

## Overview
دستور `kubectl` ابزاری است برای مدیریت کلاسترهای Kubernetes. با استفاده از این دستور، می‌توانید منابع مختلفی مانند پادها، سرویس‌ها و دیپلویمنت‌ها را ایجاد، مشاهده، به‌روزرسانی و حذف کنید.

## Usage
سینتکس پایه دستور `kubectl` به صورت زیر است:

```bash
kubectl [options] [arguments]
```

## Common Options
- `get`: برای مشاهده منابع موجود در کلاستر.
- `create`: برای ایجاد منابع جدید.
- `delete`: برای حذف منابع.
- `apply`: برای به‌روزرسانی منابع با استفاده از فایل‌های YAML.
- `describe`: برای مشاهده جزئیات یک منبع خاص.

## Common Examples
- مشاهده تمام پادها در namespace پیش‌فرض:
  ```bash
  kubectl get pods
  ```

- ایجاد یک پاد جدید از یک فایل YAML:
  ```bash
  kubectl create -f pod.yaml
  ```

- حذف یک سرویس خاص:
  ```bash
  kubectl delete service my-service
  ```

- به‌روزرسانی یک دیپلویمنت:
  ```bash
  kubectl apply -f deployment.yaml
  ```

- مشاهده جزئیات یک پاد خاص:
  ```bash
  kubectl describe pod my-pod
  ```

## Tips
- همیشه از گزینه `--namespace` برای کار با منابع در namespace‌های خاص استفاده کنید.
- برای مشاهده لاگ‌های یک پاد، از دستور `kubectl logs [pod-name]` استفاده کنید.
- از `kubectl get all` برای مشاهده تمام منابع در namespace فعلی استفاده کنید.