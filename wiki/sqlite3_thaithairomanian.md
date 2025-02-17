# [ระบบปฏิบัติการ] Bash sqlite3 การใช้งาน: จัดการฐานข้อมูล SQLite

## Overview
คำสั่ง `sqlite3` ใช้สำหรับเข้าถึงและจัดการฐานข้อมูล SQLite ผ่านทาง command line โดยสามารถใช้เพื่อสร้างฐานข้อมูลใหม่ แก้ไขฐานข้อมูลที่มีอยู่ หรือเรียกดูข้อมูลในฐานข้อมูลได้อย่างง่ายดาย

## Usage
รูปแบบพื้นฐานของคำสั่ง `sqlite3` คือ:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-init FILE` : ใช้เพื่อรันคำสั่ง SQL จากไฟล์ที่กำหนด
- `-batch` : เปิดใช้งานโหมด batch ซึ่งไม่ต้องการการโต้ตอบจากผู้ใช้
- `-header` : แสดงชื่อคอลัมน์ในผลลัพธ์
- `-csv` : ส่งออกผลลัพธ์ในรูปแบบ CSV

## Common Examples
- สร้างฐานข้อมูลใหม่:
```bash
sqlite3 mydatabase.db
```

- รันคำสั่ง SQL จากไฟล์:
```bash
sqlite3 mydatabase.db -init script.sql
```

- แสดงข้อมูลจากตาราง:
```bash
sqlite3 mydatabase.db "SELECT * FROM mytable;"
```

- ส่งออกข้อมูลในรูปแบบ CSV:
```bash
sqlite3 -header -csv mydatabase.db "SELECT * FROM mytable;" > output.csv
```

## Tips
- ใช้ `-header` เพื่อให้ผลลัพธ์มีความชัดเจนมากขึ้น
- ควรสร้างสำเนาของฐานข้อมูลก่อนทำการเปลี่ยนแปลงที่สำคัญ
- ใช้โหมด `-batch` เมื่อทำงานกับสคริปต์เพื่อหลีกเลี่ยงการหยุดชะงักจากการโต้ตอบของผู้ใช้