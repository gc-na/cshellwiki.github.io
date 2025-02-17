# [Linux] Bash psql การใช้งาน: คำสั่งสำหรับจัดการฐานข้อมูล PostgreSQL

## Overview
คำสั่ง `psql` เป็นเครื่องมือที่ใช้ในการเข้าถึงและจัดการฐานข้อมูล PostgreSQL ผ่านทาง command line โดยสามารถใช้ในการรันคำสั่ง SQL, สร้างหรือแก้ไขฐานข้อมูล และจัดการข้อมูลต่าง ๆ ได้อย่างมีประสิทธิภาพ

## Usage
การใช้งานคำสั่ง `psql` มีรูปแบบพื้นฐานดังนี้:
```bash
psql [options] [arguments]
```

## Common Options
- `-h` : ระบุที่อยู่ของเซิร์ฟเวอร์ฐานข้อมูล
- `-U` : ระบุชื่อผู้ใช้ในการเข้าสู่ระบบ
- `-d` : ระบุชื่อฐานข้อมูลที่ต้องการเชื่อมต่อ
- `-p` : ระบุหมายเลขพอร์ตที่ใช้เชื่อมต่อ
- `-c` : รันคำสั่ง SQL ที่ระบุในบรรทัดคำสั่ง

## Common Examples
- เชื่อมต่อไปยังฐานข้อมูล:
```bash
psql -h localhost -U username -d database_name
```

- รันคำสั่ง SQL โดยตรง:
```bash
psql -U username -d database_name -c "SELECT * FROM table_name;"
```

- แสดงรายการฐานข้อมูลทั้งหมด:
```bash
psql -U username -c "\l"
```

- สร้างฐานข้อมูลใหม่:
```bash
psql -U username -c "CREATE DATABASE new_database;"
```

## Tips
- ใช้ `\?` ภายใน `psql` เพื่อดูรายการคำสั่งและตัวเลือกต่าง ๆ ที่สามารถใช้ได้
- ควรใช้การเชื่อมต่อผ่าน SSL หากต้องการความปลอดภัยในการส่งข้อมูล
- ใช้ไฟล์ SQL เพื่อรันคำสั่งหลาย ๆ คำสั่งพร้อมกัน โดยใช้คำสั่ง:
```bash
psql -U username -d database_name -f script.sql
```