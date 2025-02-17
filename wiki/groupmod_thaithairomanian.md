# [Linux] Bash groupmod utilizare: [modificare grup]

## Overview
คำสั่ง `groupmod` ใช้สำหรับปรับเปลี่ยนคุณสมบัติของกลุ่มในระบบ Unix/Linux โดยสามารถใช้เพื่อเปลี่ยนชื่อกลุ่มหรือ ID ของกลุ่มได้

## Usage
คำสั่งพื้นฐานของ `groupmod` มีรูปแบบดังนี้:

```bash
groupmod [options] [arguments]
```

## Common Options
- `-n, --new-name NEW_GROUP`: เปลี่ยนชื่อกลุ่มเป็น `NEW_GROUP`
- `-g, --gid GID`: เปลี่ยน GID (Group ID) ของกลุ่ม
- `-h, --help`: แสดงข้อมูลช่วยเหลือเกี่ยวกับคำสั่ง

## Common Examples
1. เปลี่ยนชื่อกลุ่มจาก `oldgroup` เป็น `newgroup`:
   ```bash
   groupmod -n newgroup oldgroup
   ```

2. เปลี่ยน GID ของกลุ่ม `mygroup` เป็น `1001`:
   ```bash
   groupmod -g 1001 mygroup
   ```

3. แสดงข้อมูลช่วยเหลือเกี่ยวกับคำสั่ง `groupmod`:
   ```bash
   groupmod --help
   ```

## Tips
- ตรวจสอบให้แน่ใจว่าไม่มีผู้ใช้ใดอยู่ในกลุ่มที่คุณกำลังจะเปลี่ยนชื่อหรือ GID
- ใช้คำสั่ง `getent group` เพื่อตรวจสอบกลุ่มและ GID ปัจจุบันก่อนทำการเปลี่ยนแปลง
- ควรทำการสำรองข้อมูลก่อนที่จะทำการเปลี่ยนแปลงที่สำคัญในระบบกลุ่ม