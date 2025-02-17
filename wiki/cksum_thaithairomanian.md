# [Linux] Bash cksum: คำนวณค่า checksum ของไฟล์

## Overview
คำสั่ง `cksum` ใช้ในการคำนวณค่า checksum ของไฟล์ ซึ่งจะให้ค่า CRC (Cyclic Redundancy Check) และขนาดของไฟล์ในไบต์ คำสั่งนี้มีประโยชน์ในการตรวจสอบความถูกต้องของข้อมูลและการเปรียบเทียบไฟล์ต่าง ๆ

## Usage
ไวยากรณ์พื้นฐานของคำสั่ง `cksum` คือ:

```bash
cksum [options] [arguments]
```

## Common Options
- `-a, --algorithm=ALGORITHM` : กำหนดอัลกอริธึม checksum ที่จะใช้
- `-h, --help` : แสดงข้อความช่วยเหลือ
- `-V, --version` : แสดงเวอร์ชันของคำสั่ง

## Common Examples
1. คำนวณ checksum ของไฟล์เดียว:
   ```bash
   cksum filename.txt
   ```

2. คำนวณ checksum ของหลายไฟล์:
   ```bash
   cksum file1.txt file2.txt
   ```

3. ใช้ตัวเลือกเพื่อแสดงเวอร์ชัน:
   ```bash
   cksum --version
   ```

4. ใช้ตัวเลือกช่วยเหลือ:
   ```bash
   cksum --help
   ```

## Tips
- ใช้ `cksum` ร่วมกับคำสั่งอื่น ๆ เช่น `find` เพื่อคำนวณ checksum ของไฟล์ที่ค้นพบ
- ตรวจสอบ checksum ของไฟล์ที่ดาวน์โหลดเพื่อยืนยันความถูกต้อง
- เก็บค่า checksum ไว้ในไฟล์เพื่อใช้ในการตรวจสอบในอนาคต