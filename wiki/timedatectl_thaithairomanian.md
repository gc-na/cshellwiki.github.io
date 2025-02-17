# [ระบบปฏิบัติการ] Bash timedatectl การใช้งาน: จัดการวันและเวลาของระบบ

## Overview
คำสั่ง `timedatectl` ใช้สำหรับจัดการและแสดงข้อมูลเกี่ยวกับวันและเวลาของระบบปฏิบัติการ Linux โดยสามารถตั้งค่าเวลา โซนเวลา และการซิงโครไนซ์เวลากับ NTP (Network Time Protocol) ได้

## Usage
รูปแบบพื้นฐานของคำสั่งคือ:
```bash
timedatectl [options] [arguments]
```

## Common Options
- `status`: แสดงสถานะปัจจุบันของวันและเวลา
- `set-time`: ตั้งค่าเวลาใหม่
- `set-timezone`: เปลี่ยนโซนเวลา
- `set-ntp`: เปิดหรือปิดการซิงโครไนซ์เวลา NTP
- `list-timezones`: แสดงรายการโซนเวลาที่สามารถเลือกได้

## Common Examples
- แสดงสถานะวันและเวลา:
  ```bash
  timedatectl status
  ```
  
- ตั้งค่าเวลาใหม่เป็น 2023-10-01 12:00:00:
  ```bash
  timedatectl set-time '2023-10-01 12:00:00'
  ```

- เปลี่ยนโซนเวลาเป็น Asia/Bangkok:
  ```bash
  timedatectl set-timezone Asia/Bangkok
  ```

- เปิดการซิงโครไนซ์เวลา NTP:
  ```bash
  timedatectl set-ntp true
  ```

- แสดงรายการโซนเวลาที่สามารถเลือกได้:
  ```bash
  timedatectl list-timezones
  ```

## Tips
- ตรวจสอบให้แน่ใจว่าได้ตั้งค่า NTP เพื่อให้เวลาในระบบถูกต้องเสมอ
- ใช้คำสั่ง `list-timezones` เพื่อค้นหาโซนเวลาที่เหมาะสมกับพื้นที่ของคุณ
- หากเปลี่ยนโซนเวลา ควรตรวจสอบให้แน่ใจว่าแอปพลิเคชันที่ใช้งานอยู่รองรับการเปลี่ยนแปลงนี้