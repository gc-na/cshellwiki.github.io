# [ระบบปฏิบัติการ] Bash hostnamectl การใช้งาน: จัดการชื่อโฮสต์ในระบบ

## Overview
คำสั่ง `hostnamectl` ใช้สำหรับจัดการชื่อโฮสต์ของระบบ Linux รวมถึงการแสดงข้อมูลเกี่ยวกับระบบและการตั้งค่าชื่อโฮสต์ใหม่ได้อย่างง่ายดาย

## Usage
คำสั่งพื้นฐานของ `hostnamectl` มีรูปแบบดังนี้:
```bash
hostnamectl [options] [arguments]
```

## Common Options
- `set-hostname`: ใช้เพื่อเปลี่ยนชื่อโฮสต์
- `status`: แสดงสถานะปัจจุบันของชื่อโฮสต์และข้อมูลระบบ
- `set-icon-name`: ตั้งชื่อไอคอนสำหรับโฮสต์
- `set-chassis`: ตั้งประเภทของโฮสต์ เช่น desktop, laptop, server เป็นต้น

## Common Examples
- แสดงสถานะของชื่อโฮสต์:
```bash
hostnamectl status
```
- เปลี่ยนชื่อโฮสต์เป็น "my-new-host":
```bash
sudo hostnamectl set-hostname my-new-host
```
- ตั้งชื่อไอคอนเป็น "computer":
```bash
sudo hostnamectl set-icon-name computer
```
- ตั้งประเภทของโฮสต์เป็น "laptop":
```bash
sudo hostnamectl set-chassis laptop
```

## Tips
- ใช้คำสั่ง `sudo` เมื่อคุณต้องการเปลี่ยนแปลงชื่อโฮสต์หรือการตั้งค่าอื่น ๆ ที่ต้องการสิทธิ์ผู้ดูแลระบบ
- ตรวจสอบสถานะของชื่อโฮสต์หลังจากทำการเปลี่ยนแปลงเพื่อให้แน่ใจว่าการตั้งค่าได้ถูกต้อง
- ควรเลือกชื่อโฮสต์ที่มีความหมายและง่ายต่อการจดจำเพื่อความสะดวกในการจัดการระบบในอนาคต