# [ระบบปฏิบัติการ] C Shell (csh) sqlite3 การใช้งาน: คำสั่งจัดการฐานข้อมูล SQLite

## Overview
คำสั่ง `sqlite3` ใช้สำหรับจัดการฐานข้อมูล SQLite ซึ่งเป็นฐานข้อมูลที่เบาและไม่ต้องการเซิร์ฟเวอร์ ทำให้เหมาะสำหรับการใช้งานในแอปพลิเคชันที่ต้องการการเข้าถึงข้อมูลอย่างรวดเร็วและมีประสิทธิภาพ

## Usage
การใช้งานคำสั่ง `sqlite3` มีรูปแบบพื้นฐานดังนี้:

```csh
sqlite3 [options] [arguments]
```

## Common Options
- `-help` : แสดงคำแนะนำการใช้งาน
- `-version` : แสดงเวอร์ชันของ SQLite
- `-init` : ระบุไฟล์ที่ต้องการให้รันเมื่อเริ่มต้น
- `-batch` : รันในโหมด batch โดยไม่แสดง prompt

## Common Examples
1. เปิดฐานข้อมูล SQLite:
   ```csh
   sqlite3 mydatabase.db
   ```

2. รันคำสั่ง SQL จากไฟล์:
   ```csh
   sqlite3 mydatabase.db < script.sql
   ```

3. แสดงเวอร์ชันของ SQLite:
   ```csh
   sqlite3 -version
   ```

4. สร้างตารางใหม่ในฐานข้อมูล:
   ```csh
   sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
   ```

5. แทรกข้อมูลลงในตาราง:
   ```csh
   sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('John Doe');"
   ```

## Tips
- ใช้โหมด batch หากต้องการรันคำสั่งหลายคำสั่งในครั้งเดียวเพื่อประหยัดเวลา
- ตรวจสอบคำสั่ง SQL ที่ใช้ให้ถูกต้องก่อนรัน เพื่อหลีกเลี่ยงข้อผิดพลาด
- สำรองข้อมูลฐานข้อมูลเป็นประจำเพื่อป้องกันการสูญหายของข้อมูล