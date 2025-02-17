# [Linux] Bash setenv utilizare: [set environment variables]

## Overview
คำสั่ง `setenv` ใช้ในการตั้งค่าตัวแปรสภาพแวดล้อมใน Bash ซึ่งช่วยให้ผู้ใช้สามารถกำหนดค่าตัวแปรที่ใช้ในเซสชันของเชลล์ได้อย่างง่ายดาย

## Usage
การใช้งานคำสั่ง `setenv` มีรูปแบบพื้นฐานดังนี้:

```bash
setenv [variable_name] [value]
```

## Common Options
คำสั่ง `setenv` ไม่มีตัวเลือกที่ซับซ้อน แต่สามารถใช้เพื่อกำหนดตัวแปรได้หลายตัวในครั้งเดียว โดยการเรียกใช้คำสั่งหลายครั้ง

## Common Examples
ตัวอย่างการใช้งานคำสั่ง `setenv` มีดังนี้:

1. ตั้งค่าตัวแปร PATH:
   ```bash
   setenv PATH /usr/local/bin:$PATH
   ```

2. ตั้งค่าตัวแปร HOME:
   ```bash
   setenv HOME /home/user
   ```

3. ตั้งค่าตัวแปร JAVA_HOME:
   ```bash
   setenv JAVA_HOME /usr/lib/jvm/java-11-openjdk
   ```

## Tips
- ตรวจสอบว่าตัวแปรที่ตั้งค่าแล้วมีผลในเซสชันปัจจุบันโดยใช้คำสั่ง `echo` เช่น:
  ```bash
  echo $JAVA_HOME
  ```
- ใช้คำสั่ง `unset` เพื่อลบตัวแปรที่ไม่ต้องการ:
  ```bash
  unset variable_name
  ```
- ควรตั้งค่าตัวแปรที่ใช้บ่อยในไฟล์ `.bashrc` หรือ `.bash_profile` เพื่อให้มีผลทุกครั้งที่เริ่มต้นเชลล์ใหม่