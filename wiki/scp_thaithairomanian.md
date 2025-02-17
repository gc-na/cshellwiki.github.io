# [Linux] Bash scp: การคัดลอกไฟล์ระหว่างโฮสต์

## Overview
คำสั่ง `scp` (Secure Copy Protocol) ใช้สำหรับการคัดลอกไฟล์หรือไดเรกทอรีระหว่างโฮสต์ที่เชื่อมต่อกันผ่าน SSH โดยมีความปลอดภัยในการส่งข้อมูล

## Usage
การใช้งานพื้นฐานของคำสั่ง `scp` มีรูปแบบดังนี้:
```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: คัดลอกไดเรกทอรีและเนื้อหาทั้งหมดภายใน
- `-P`: ระบุหมายเลขพอร์ตที่ไม่ใช่พอร์ตเริ่มต้น (22)
- `-i`: ใช้ไฟล์คีย์ส่วนตัวสำหรับการตรวจสอบตัวตน
- `-v`: แสดงข้อมูลการทำงานเพื่อการดีบัก

## Common Examples
- คัดลอกไฟล์จากเครื่องท้องถิ่นไปยังเซิร์ฟเวอร์:
  ```bash
  scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
  ```

- คัดลอกไฟล์จากเซิร์ฟเวอร์ไปยังเครื่องท้องถิ่น:
  ```bash
  scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
  ```

- คัดลอกไดเรกทอรีทั้งหมดจากเครื่องท้องถิ่นไปยังเซิร์ฟเวอร์:
  ```bash
  scp -r /path/to/local/directory/ user@remote_host:/path/to/remote/directory/
  ```

- คัดลอกไฟล์โดยระบุพอร์ตที่ไม่ใช่พอร์ตเริ่มต้น:
  ```bash
  scp -P 2222 /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
  ```

## Tips
- ตรวจสอบให้แน่ใจว่า SSH ทำงานอยู่บนเซิร์ฟเวอร์ที่คุณต้องการเชื่อมต่อ
- ใช้ `-v` เพื่อดูข้อมูลการทำงานเมื่อเกิดปัญหา
- คัดลอกไฟล์ในขนาดเล็กก่อนเพื่อทดสอบการเชื่อมต่อและการตั้งค่าก่อนการคัดลอกไฟล์ขนาดใหญ่