# [ระบบปฏิบัติการ] C Shell (csh) kubectl การใช้งาน: คำสั่งสำหรับจัดการ Kubernetes

## Overview
คำสั่ง `kubectl` เป็นเครื่องมือที่ใช้ในการจัดการและควบคุม Kubernetes clusters ซึ่งช่วยให้ผู้ใช้สามารถสร้าง แก้ไข และลบทรัพยากรต่าง ๆ ใน Kubernetes ได้อย่างมีประสิทธิภาพ

## Usage
รูปแบบพื้นฐานของคำสั่ง `kubectl` คือ:

```bash
kubectl [options] [arguments]
```

## Common Options
- `get`: ใช้เพื่อดึงข้อมูลทรัพยากรใน Kubernetes
- `apply`: ใช้เพื่อปรับใช้การเปลี่ยนแปลงในทรัพยากร
- `delete`: ใช้เพื่อลบทรัพยากร
- `describe`: ใช้เพื่อแสดงรายละเอียดของทรัพยากร
- `logs`: ใช้เพื่อดูบันทึกของ pod

## Common Examples
- ดึงข้อมูล pods ทั้งหมดใน namespace ปัจจุบัน:
  ```bash
  kubectl get pods
  ```

- ปรับใช้การเปลี่ยนแปลงจากไฟล์ YAML:
  ```bash
  kubectl apply -f deployment.yaml
  ```

- ลบ pod ที่ชื่อว่า my-pod:
  ```bash
  kubectl delete pod my-pod
  ```

- แสดงรายละเอียดของ service ชื่อ my-service:
  ```bash
  kubectl describe service my-service
  ```

- ดูบันทึกของ pod ชื่อ my-pod:
  ```bash
  kubectl logs my-pod
  ```

## Tips
- ใช้ `kubectl get all` เพื่อดูทรัพยากรทั้งหมดใน namespace ปัจจุบัน
- ใช้ `-n [namespace]` เพื่อระบุ namespace ที่ต้องการทำงานด้วย
- ใช้ `--help` เพื่อดูความช่วยเหลือและตัวเลือกเพิ่มเติมสำหรับคำสั่งต่าง ๆ