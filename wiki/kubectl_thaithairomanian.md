# [ระบบปฏิบัติการ] Bash kubectl การใช้งาน: คำสั่งสำหรับจัดการ Kubernetes

## Overview
คำสั่ง `kubectl` เป็นเครื่องมือที่ใช้ในการจัดการและควบคุมคลัสเตอร์ Kubernetes โดยช่วยให้ผู้ใช้สามารถทำการสร้าง, แก้ไข, และลบทรัพยากรต่างๆ ในคลัสเตอร์ได้อย่างง่ายดาย

## Usage
รูปแบบพื้นฐานของคำสั่ง `kubectl` คือ:

```
kubectl [options] [arguments]
```

## Common Options
- `get`: ใช้เพื่อดึงข้อมูลทรัพยากรในคลัสเตอร์
- `apply`: ใช้เพื่อปรับใช้การเปลี่ยนแปลงจากไฟล์ YAML
- `delete`: ใช้เพื่อลบทรัพยากร
- `describe`: ใช้เพื่อแสดงรายละเอียดของทรัพยากร
- `logs`: ใช้เพื่อดูบันทึกของ Pod

## Common Examples
- ดึงข้อมูล Pod ทั้งหมดใน namespace ปัจจุบัน:
  ```bash
  kubectl get pods
  ```

- ปรับใช้การเปลี่ยนแปลงจากไฟล์ YAML:
  ```bash
  kubectl apply -f deployment.yaml
  ```

- ลบ Pod ที่ชื่อว่า my-pod:
  ```bash
  kubectl delete pod my-pod
  ```

- แสดงรายละเอียดของ Deployment ที่ชื่อว่า my-deployment:
  ```bash
  kubectl describe deployment my-deployment
  ```

- ดูบันทึกของ Pod ที่ชื่อว่า my-pod:
  ```bash
  kubectl logs my-pod
  ```

## Tips
- ใช้ `kubectl get all` เพื่อดูทรัพยากรทั้งหมดใน namespace ปัจจุบัน
- ใช้ `-n <namespace>` เพื่อระบุ namespace ที่ต้องการทำงานด้วย
- ใช้ `--help` เพื่อดูรายละเอียดเพิ่มเติมเกี่ยวกับคำสั่งและตัวเลือกต่างๆ