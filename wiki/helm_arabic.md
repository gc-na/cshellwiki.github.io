# [لينكس] Bash helm الاستخدام: إدارة تطبيقات Kubernetes

## Overview
يعتبر أمر helm أداة قوية لإدارة التطبيقات على Kubernetes. يساعد المستخدمين في تثبيت وتحديث وحذف التطبيقات بسهولة من خلال حزم تُعرف باسم "المخططات" (charts). يوفر helm طريقة منظمة لإدارة التطبيقات المعقدة.

## Usage
تكون الصيغة الأساسية لأمر helm كما يلي:
```bash
helm [options] [arguments]
```

## Common Options
- `install`: لتثبيت مخطط جديد.
- `upgrade`: لتحديث مخطط موجود.
- `delete`: لحذف مخطط مثبت.
- `list`: لعرض المخططات المثبتة.
- `repo`: لإدارة مستودعات المخططات.

## Common Examples
- لتثبيت مخطط جديد:
```bash
helm install my-release my-chart
```

- لتحديث مخطط موجود:
```bash
helm upgrade my-release my-chart
```

- لحذف مخطط مثبت:
```bash
helm delete my-release
```

- لعرض المخططات المثبتة:
```bash
helm list
```

- لإضافة مستودع مخططات جديد:
```bash
helm repo add my-repo https://example.com/charts
```

## Tips
- تأكد من تحديث مستودعات المخططات بانتظام باستخدام `helm repo update`.
- استخدم `helm search` للبحث عن المخططات المتاحة في المستودعات.
- قم بقراءة الوثائق الخاصة بالمخططات للحصول على معلومات دقيقة حول الخيارات المتاحة.