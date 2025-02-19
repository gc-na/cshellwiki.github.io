# [Linux] C Shell (csh) dnf การใช้งาน: คำสั่งจัดการแพ็คเกจ

## Overview
คำสั่ง `dnf` (Dandified YUM) เป็นเครื่องมือที่ใช้ในการจัดการแพ็คเกจในระบบปฏิบัติการ Linux ซึ่งช่วยให้ผู้ใช้สามารถติดตั้ง อัปเดต และลบซอฟต์แวร์ได้อย่างง่ายดาย

## Usage
รูปแบบพื้นฐานของคำสั่ง `dnf` คือ:

```bash
dnf [options] [arguments]
```

## Common Options
- `install`: ใช้เพื่อติดตั้งแพ็คเกจ
- `remove`: ใช้เพื่อลบแพ็คเกจ
- `update`: ใช้เพื่ออัปเดตแพ็คเกจที่ติดตั้งอยู่
- `search`: ใช้ค้นหาแพ็คเกจในฐานข้อมูล
- `list`: แสดงรายการแพ็คเกจที่ติดตั้งหรือที่มีอยู่ในระบบ

## Common Examples
- ติดตั้งแพ็คเกจ:
  ```bash
  dnf install package-name
  ```

- ลบแพ็คเกจ:
  ```bash
  dnf remove package-name
  ```

- อัปเดตแพ็คเกจ:
  ```bash
  dnf update package-name
  ```

- ค้นหาแพ็คเกจ:
  ```bash
  dnf search package-name
  ```

- แสดงรายการแพ็คเกจที่ติดตั้ง:
  ```bash
  dnf list installed
  ```

## Tips
- ควรใช้ `dnf update` เป็นประจำเพื่อให้ระบบของคุณมีความปลอดภัยและทันสมัย
- ใช้ `dnf search` เพื่อค้นหาแพ็คเกจที่คุณต้องการติดตั้งก่อนที่จะใช้คำสั่ง `install`
- หากคุณต้องการติดตั้งแพ็คเกจหลายตัวในครั้งเดียว สามารถระบุชื่อแพ็คเกจได้หลายตัวในคำสั่ง `install` เช่น `dnf install package1 package2`