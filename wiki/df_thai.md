# [ระบบปฏิบัติการ] C Shell (csh) df การใช้งาน: แสดงข้อมูลการใช้ดิสก์

## Overview
คำสั่ง `df` ใช้เพื่อแสดงข้อมูลเกี่ยวกับการใช้พื้นที่ดิสก์ในระบบ โดยจะแสดงขนาดของระบบไฟล์ที่ติดตั้งอยู่และพื้นที่ที่ยังว่างอยู่

## Usage
รูปแบบพื้นฐานของคำสั่งคือ:
```csh
df [options] [arguments]
```

## Common Options
- `-h`: แสดงขนาดในรูปแบบที่อ่านง่าย (เช่น KB, MB, GB)
- `-T`: แสดงประเภทของระบบไฟล์
- `-i`: แสดงข้อมูลเกี่ยวกับจำนวน inode ที่ใช้และว่างอยู่

## Common Examples
- แสดงข้อมูลการใช้ดิสก์ทั้งหมดในรูปแบบที่อ่านง่าย:
```csh
df -h
```

- แสดงข้อมูลการใช้ดิสก์พร้อมประเภทของระบบไฟล์:
```csh
df -T
```

- แสดงข้อมูลเกี่ยวกับ inode:
```csh
df -i
```

## Tips
- ใช้ `df -h` เป็นประจำเพื่อให้เห็นข้อมูลที่เข้าใจง่าย
- ตรวจสอบพื้นที่ว่างก่อนที่จะติดตั้งซอฟต์แวร์ใหม่เพื่อหลีกเลี่ยงปัญหาดิสก์เต็ม
- ใช้คำสั่ง `df` ร่วมกับ `grep` เพื่อค้นหาข้อมูลเฉพาะเจาะจง เช่น:
```csh
df -h | grep /dev/sda1
```