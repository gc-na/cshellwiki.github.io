# [ระบบปฏิบัติการ] Bash lvm การใช้งาน: จัดการการจัดเก็บข้อมูลแบบลอจิคัล

## Overview
คำสั่ง `lvm` (Logical Volume Manager) ใช้สำหรับการจัดการการจัดเก็บข้อมูลในระบบ Linux โดยช่วยให้ผู้ใช้สามารถสร้าง, ขยาย, ลดขนาด, และจัดการกับ Logical Volumes ได้อย่างมีประสิทธิภาพ

## Usage
รูปแบบพื้นฐานของคำสั่ง `lvm` คือ:

```
lvm [options] [arguments]
```

## Common Options
- `create`: สร้าง Logical Volume ใหม่
- `extend`: ขยาย Logical Volume ที่มีอยู่
- `reduce`: ลดขนาดของ Logical Volume
- `remove`: ลบ Logical Volume
- `list`: แสดงรายการ Logical Volumes ที่มีอยู่

## Common Examples
1. **สร้าง Logical Volume ใหม่**
   ```bash
   lvm create -n my_volume -L 10G my_volume_group
   ```

2. **ขยาย Logical Volume**
   ```bash
   lvm extend -L +5G /dev/my_volume_group/my_volume
   ```

3. **ลดขนาด Logical Volume**
   ```bash
   lvm reduce -L -2G /dev/my_volume_group/my_volume
   ```

4. **ลบ Logical Volume**
   ```bash
   lvm remove /dev/my_volume_group/my_volume
   ```

5. **แสดงรายการ Logical Volumes**
   ```bash
   lvm list
   ```

## Tips
- ควรทำการสำรองข้อมูลก่อนที่จะลดขนาด Logical Volume เพื่อป้องกันการสูญหายของข้อมูล
- ใช้คำสั่ง `lvm list` เพื่อดูสถานะของ Logical Volumes ก่อนทำการเปลี่ยนแปลง
- การขยาย Logical Volume สามารถทำได้ในขณะที่มันถูกใช้งานอยู่ แต่การลดขนาดควรทำเมื่อ Logical Volume ไม่ได้ถูกใช้งาน