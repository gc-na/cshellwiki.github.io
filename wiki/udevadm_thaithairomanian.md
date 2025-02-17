# [Linux] Bash udevadm การใช้งาน: คำสั่งสำหรับจัดการอุปกรณ์

## Overview
คำสั่ง `udevadm` ใช้สำหรับจัดการและตรวจสอบอุปกรณ์ในระบบ Linux โดยเฉพาะการทำงานร่วมกับ udev ซึ่งเป็นระบบจัดการอุปกรณ์ที่ช่วยในการจัดการการเชื่อมต่อและการตั้งค่าของอุปกรณ์ต่าง ๆ ในระบบปฏิบัติการ

## Usage
การใช้งานคำสั่ง `udevadm` มีรูปแบบพื้นฐานดังนี้:

```
udevadm [options] [arguments]
```

## Common Options
- `info`: แสดงข้อมูลเกี่ยวกับอุปกรณ์
- `trigger`: กระตุ้นให้ udev สร้างอุปกรณ์ใหม่
- `settle`: รอให้ udev จัดการอุปกรณ์ที่ยังไม่เสร็จสิ้น
- `control`: ควบคุมการทำงานของ udev daemon

## Common Examples
1. **แสดงข้อมูลเกี่ยวกับอุปกรณ์**
   ```bash
   udevadm info --query=all --name=/dev/sda
   ```

2. **กระตุ้นให้ udev สร้างอุปกรณ์ใหม่**
   ```bash
   udevadm trigger
   ```

3. **รอให้ udev จัดการอุปกรณ์**
   ```bash
   udevadm settle
   ```

4. **ควบคุมการทำงานของ udev daemon**
   ```bash
   udevadm control --reload-rules
   ```

## Tips
- ใช้ `udevadm info` เพื่อดูรายละเอียดของอุปกรณ์ที่คุณสนใจ
- ควรใช้ `udevadm trigger` หลังจากติดตั้งอุปกรณ์ใหม่เพื่อให้ระบบรู้จักอุปกรณ์นั้น
- ใช้ `udevadm settle` เมื่อคุณต้องการรอให้ udev ทำงานเสร็จสิ้นก่อนที่จะดำเนินการต่อ