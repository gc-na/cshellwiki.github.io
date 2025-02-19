# [ระบบปฏิบัติการ] C Shell (csh) timedatectl การใช้งาน: จัดการวันที่และเวลา

## Overview
คำสั่ง `timedatectl` ใช้สำหรับจัดการและตรวจสอบการตั้งค่าเวลาและวันที่ในระบบ Linux โดยสามารถปรับเปลี่ยนเวลาโซนและตั้งค่าเวลาได้อย่างง่ายดาย

## Usage
รูปแบบพื้นฐานของคำสั่งคือ:
```csh
timedatectl [options] [arguments]
```

## Common Options
- `status` - แสดงสถานะปัจจุบันของวันที่และเวลา
- `set-time` - ตั้งค่าเวลาใหม่
- `set-timezone` - เปลี่ยนโซนเวลา
- `list-timezones` - แสดงรายการโซนเวลาที่สามารถเลือกได้
- `set-ntp` - เปิดหรือปิดการซิงค์เวลาอัตโนมัติ

## Common Examples
- แสดงสถานะวันที่และเวลา:
```csh
timedatectl status
```

- ตั้งค่าเวลาใหม่เป็น 15:30:00:
```csh
timedatectl set-time '15:30:00'
```

- เปลี่ยนโซนเวลาเป็น Asia/Bangkok:
```csh
timedatectl set-timezone Asia/Bangkok
```

- แสดงรายการโซนเวลาทั้งหมด:
```csh
timedatectl list-timezones
```

- เปิดการซิงค์เวลาอัตโนมัติ:
```csh
timedatectl set-ntp true
```

## Tips
- ตรวจสอบให้แน่ใจว่าได้ใช้สิทธิ์ผู้ดูแลระบบเมื่อทำการเปลี่ยนแปลงเวลาและวันที่
- ใช้ `timedatectl list-timezones` เพื่อค้นหาโซนเวลาที่ถูกต้องก่อนที่จะตั้งค่า
- การเปิดการซิงค์เวลาอัตโนมัติจะช่วยให้เวลาของระบบถูกต้องและอัปเดตอยู่เสมอ