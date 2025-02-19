# [ระบบปฏิบัติการ] C Shell (csh) helm การใช้งาน: คำสั่งสำหรับจัดการแพ็กเกจ

## Overview
คำสั่ง `helm` ใช้ในการจัดการแพ็กเกจสำหรับ Kubernetes โดยช่วยให้ผู้ใช้สามารถติดตั้ง อัปเกรด และจัดการแอปพลิเคชันที่ทำงานบน Kubernetes ได้อย่างง่ายดาย

## Usage
รูปแบบพื้นฐานของคำสั่ง helm คือ:

```
helm [options] [arguments]
```

## Common Options
- `install`: ใช้เพื่อติดตั้งแพ็กเกจใหม่
- `upgrade`: ใช้เพื่ออัปเกรดแพ็กเกจที่มีอยู่
- `uninstall`: ใช้เพื่อลบแพ็กเกจที่ติดตั้งแล้ว
- `list`: แสดงรายการแพ็กเกจที่ติดตั้งอยู่ใน Kubernetes
- `repo`: ใช้ในการจัดการแหล่งที่มาของแพ็กเกจ

## Common Examples
ตัวอย่างการใช้งานคำสั่ง helm มีดังนี้:

### ติดตั้งแพ็กเกจ
```bash
helm install my-release stable/my-chart
```

### อัปเกรดแพ็กเกจ
```bash
helm upgrade my-release stable/my-chart
```

### ลบแพ็กเกจ
```bash
helm uninstall my-release
```

### แสดงรายการแพ็กเกจที่ติดตั้ง
```bash
helm list
```

### เพิ่มแหล่งที่มาของแพ็กเกจ
```bash
helm repo add my-repo https://example.com/charts
```

## Tips
- ควรตรวจสอบเวอร์ชันของ helm และ Kubernetes ให้ตรงกันเพื่อหลีกเลี่ยงปัญหาในการติดตั้ง
- ใช้ `helm repo update` เพื่ออัปเดตแหล่งที่มาของแพ็กเกจเป็นประจำ
- อ่านเอกสารของแต่ละแพ็กเกจเพื่อทำความเข้าใจการตั้งค่าและตัวเลือกที่มีให้