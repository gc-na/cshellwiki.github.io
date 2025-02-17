# [ระบบปฏิบัติการ] Bash lvextend การขยาย Logical Volume: ขยายขนาด Logical Volume ใน LVM

## Overview
คำสั่ง `lvextend` ใช้ในการขยายขนาดของ Logical Volume (LV) ใน Logical Volume Manager (LVM) โดยสามารถเพิ่มพื้นที่ให้กับ LV ที่มีอยู่แล้ว เพื่อรองรับข้อมูลที่เพิ่มขึ้นหรือการใช้งานที่มากขึ้น

## Usage
รูปแบบพื้นฐานของคำสั่ง `lvextend` คือ:

```bash
lvextend [options] [arguments]
```

## Common Options
- `-L +size`: เพิ่มขนาด LV โดยระบุขนาดที่ต้องการเพิ่ม
- `-L size`: ตั้งค่าขนาด LV เป็นขนาดที่ระบุ
- `-r`: ขยาย filesystem โดยอัตโนมัติหลังจากขยาย LV
- `-n`: เปลี่ยนชื่อ LV

## Common Examples
1. ขยาย LV ขนาด 10GB:
   ```bash
   lvextend -L +10G /dev/vg_name/lv_name
   ```

2. ตั้งค่าขนาด LV เป็น 50GB:
   ```bash
   lvextend -L 50G /dev/vg_name/lv_name
   ```

3. ขยาย LV และขยาย filesystem โดยอัตโนมัติ:
   ```bash
   lvextend -r -L +5G /dev/vg_name/lv_name
   ```

4. เปลี่ยนชื่อ LV:
   ```bash
   lvextend -n new_lv_name /dev/vg_name/old_lv_name
   ```

## Tips
- ตรวจสอบพื้นที่ว่างใน Volume Group (VG) ก่อนขยาย LV เพื่อให้แน่ใจว่ามีพื้นที่เพียงพอ
- ใช้ตัวเลือก `-r` เพื่อทำให้การขยาย LV และ filesystem เป็นไปโดยอัตโนมัติ ซึ่งจะช่วยลดความยุ่งยาก
- ควรทำการสำรองข้อมูลก่อนที่จะทำการขยาย LV เพื่อป้องกันการสูญหายของข้อมูลในกรณีที่เกิดข้อผิดพลาด