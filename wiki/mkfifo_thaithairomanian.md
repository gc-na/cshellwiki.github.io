# [Linux] Bash mkfifo: สร้างไฟล์ FIFO (named pipe)

## Overview
คำสั่ง `mkfifo` ใช้สำหรับสร้างไฟล์ FIFO (First In First Out) หรือที่เรียกว่า named pipe ซึ่งช่วยให้โปรเซสต่าง ๆ สามารถสื่อสารกันได้โดยการส่งข้อมูลผ่านไฟล์นี้

## Usage
รูปแบบพื้นฐานของคำสั่งคือ:

```bash
mkfifo [options] [arguments]
```

## Common Options
- `-m, --mode=MODE` : กำหนดโหมดการเข้าถึงของไฟล์ FIFO ที่สร้างขึ้น
- `-Z, --context=CONTEXT` : ตั้งค่าบริบท SELinux สำหรับไฟล์ FIFO

## Common Examples
### สร้างไฟล์ FIFO พื้นฐาน
```bash
mkfifo mypipe
```

### สร้างไฟล์ FIFO พร้อมกำหนดโหมดการเข้าถึง
```bash
mkfifo -m 644 mypipe
```

### สร้างไฟล์ FIFO พร้อมบริบท SELinux
```bash
mkfifo -Z mypipe
```

## Tips
- ตรวจสอบว่าไฟล์ FIFO ถูกสร้างขึ้นอย่างถูกต้องโดยใช้คำสั่ง `ls -l` เพื่อดูสิทธิ์การเข้าถึง
- ใช้คำสั่ง `cat` หรือ `echo` เพื่อส่งข้อมูลไปยัง FIFO และคำสั่ง `cat` หรือ `read` เพื่ออ่านข้อมูลจาก FIFO
- อย่าลืมว่าการอ่านและเขียนจาก FIFO ต้องทำในโปรเซสที่แตกต่างกัน เพื่อให้การสื่อสารทำงานได้อย่างถูกต้อง