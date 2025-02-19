# [Linux] C Shell (csh) lvcreate การสร้าง Logical Volume: สร้าง Logical Volume ใหม่ในระบบ

## Overview
คำสั่ง `lvcreate` ใช้สำหรับสร้าง Logical Volume ใหม่ในระบบที่ใช้ LVM (Logical Volume Manager) ซึ่งช่วยให้ผู้ใช้สามารถจัดการกับดิสก์และพาร์ติชันได้อย่างมีประสิทธิภาพมากขึ้น

## Usage
รูปแบบพื้นฐานของคำสั่ง `lvcreate` คือ:
```
lvcreate [options] [arguments]
```

## Common Options
- `-n` : ตั้งชื่อให้กับ Logical Volume ที่จะสร้าง
- `-L` : กำหนดขนาดของ Logical Volume
- `-l` : กำหนดขนาดในหน่วย Logical Extents
- `-m` : กำหนดจำนวน mirror ของ Logical Volume
- `-Z` : กำหนดให้ Logical Volume ถูกสร้างขึ้นในโหมด zeroed

## Common Examples
ตัวอย่างการใช้งาน `lvcreate` มีดังนี้:

1. สร้าง Logical Volume ขนาด 10GB ชื่อ "myvolume":
   ```bash
   lvcreate -n myvolume -L 10G myvg
   ```

2. สร้าง Logical Volume ขนาด 5GB โดยใช้ Logical Extents:
   ```bash
   lvcreate -n myvolume -l 100 myvg
   ```

3. สร้าง Logical Volume ที่มี mirror:
   ```bash
   lvcreate -m 1 -n mymirror -L 20G myvg
   ```

4. สร้าง Logical Volume และกำหนดให้ถูก zeroed:
   ```bash
   lvcreate -Z y -n myzeroedvolume -L 15G myvg
   ```

## Tips
- ควรตรวจสอบพื้นที่ว่างใน Volume Group ก่อนสร้าง Logical Volume ใหม่
- ใช้ชื่อที่มีความหมายเพื่อให้การจัดการ Logical Volume ง่ายขึ้น
- หากต้องการสร้าง Logical Volume ที่มี mirror ควรตรวจสอบว่ามีพื้นที่เพียงพอใน Volume Group
- ใช้คำสั่ง `lvdisplay` เพื่อตรวจสอบ Logical Volume ที่สร้างขึ้นแล้ว