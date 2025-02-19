# [ระบบปฏิบัติการ] C Shell (csh) scp การใช้งาน: การถ่ายโอนไฟล์ระหว่างโฮสต์

## Overview
คำสั่ง `scp` (Secure Copy Protocol) ใช้สำหรับการถ่ายโอนไฟล์ระหว่างโฮสต์ในเครือข่ายอย่างปลอดภัย โดยใช้ SSH (Secure Shell) เพื่อเข้ารหัสข้อมูลระหว่างการส่ง

## Usage
รูปแบบพื้นฐานของคำสั่ง `scp` มีดังนี้:
```
scp [options] [arguments]
```

## Common Options
- `-r`: คัดลอกไฟล์และไดเรกทอรีทั้งหมด (recursive)
- `-P port`: ระบุพอร์ตที่ใช้ในการเชื่อมต่อ (พอร์ต SSH มักจะเป็น 22)
- `-i identity_file`: ใช้ไฟล์คีย์ส่วนตัวสำหรับการตรวจสอบตัวตน
- `-v`: แสดงข้อมูลการทำงานอย่างละเอียด (verbose)

## Common Examples
1. คัดลอกไฟล์จากเครื่องท้องถิ่นไปยังเซิร์ฟเวอร์:
   ```bash
   scp /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

2. คัดลอกไฟล์จากเซิร์ฟเวอร์ไปยังเครื่องท้องถิ่น:
   ```bash
   scp username@remote_host:/path/to/remote/file /path/to/local/directory
   ```

3. คัดลอกไดเรกทอรีทั้งหมดไปยังเซิร์ฟเวอร์:
   ```bash
   scp -r /path/to/local/directory username@remote_host:/path/to/remote/directory
   ```

4. คัดลอกไฟล์โดยระบุพอร์ตที่ไม่ใช่ค่าเริ่มต้น:
   ```bash
   scp -P 2222 /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

## Tips
- ตรวจสอบให้แน่ใจว่า SSH ทำงานอยู่บนเซิร์ฟเวอร์ที่คุณต้องการเชื่อมต่อ
- ใช้ตัวเลือก `-v` เพื่อช่วยในการแก้ไขปัญหาหากการเชื่อมต่อไม่สำเร็จ
- หากคุณใช้คีย์ส่วนตัวในการตรวจสอบตัวตน ควรตั้งค่าให้ไฟล์คีย์มีสิทธิ์การเข้าถึงที่เหมาะสม (เช่น 600)