# [Bash] Bash unalias utilizare: ลบ alias ที่กำหนดไว้

## Overview
คำสั่ง `unalias` ใช้เพื่อยกเลิก alias ที่ถูกกำหนดไว้ในเซสชันของ Bash ซึ่งช่วยให้ผู้ใช้สามารถคืนค่าคำสั่งกลับไปเป็นค่าปกติได้

## Usage
รูปแบบพื้นฐานของคำสั่ง `unalias` คือ:

```bash
unalias [options] [arguments]
```

## Common Options
- `-a`: ยกเลิก alias ทั้งหมดที่ถูกกำหนดไว้
- `-m`: ยกเลิก alias ที่ตรงกับรูปแบบที่กำหนด

## Common Examples
- ยกเลิก alias ที่ชื่อว่า `ll`:
    ```bash
    unalias ll
    ```

- ยกเลิก alias ทั้งหมด:
    ```bash
    unalias -a
    ```

- ยกเลิก alias ที่ตรงกับรูปแบบ:
    ```bash
    unalias -m 'l*'
    ```

## Tips
- ควรตรวจสอบ alias ที่มีอยู่ก่อนที่จะยกเลิก โดยใช้คำสั่ง `alias` เพื่อดูรายการทั้งหมด
- หากต้องการให้การเปลี่ยนแปลงมีผลในทุกเซสชัน ควรเพิ่มคำสั่ง `unalias` ในไฟล์ `.bashrc` หรือ `.bash_profile`