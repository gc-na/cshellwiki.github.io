# [Linux] Bash getopts: [จัดการตัวเลือกในสคริปต์]

## Overview
คำสั่ง `getopts` ใช้ในการจัดการตัวเลือก (options) ในสคริปต์ Bash โดยช่วยให้สามารถอ่านและประมวลผลตัวเลือกที่ถูกส่งเข้ามาในขณะเรียกใช้งานสคริปต์ได้อย่างมีประสิทธิภาพ

## Usage
การใช้งานพื้นฐานของคำสั่ง `getopts` มีดังนี้:

```bash
getopts [options] [arguments]
```

## Common Options
- `-a`: ใช้เพื่อกำหนดตัวเลือกที่ต้องการ
- `-b`: ใช้เพื่อกำหนดค่าพารามิเตอร์ที่เกี่ยวข้องกับตัวเลือก
- `-c`: ใช้เพื่อระบุว่าต้องการให้แสดงข้อความช่วยเหลือ

## Common Examples

### Example 1: การใช้ getopts เพื่ออ่านตัวเลือก
```bash
#!/bin/bash

while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B selected with value: $OPTARG"
      ;;
    c)
      echo "Option C selected with value: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### Example 2: การใช้ getopts ในการแสดงข้อความช่วยเหลือ
```bash
#!/bin/bash

while getopts "ab:c:h" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B selected with value: $OPTARG"
      ;;
    c)
      echo "Option C selected with value: $OPTARG"
      ;;
    h)
      echo "Usage: script.sh [-a] [-b value] [-c value]"
      exit 0
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

## Tips
- ควรใช้ `getopts` ในการจัดการตัวเลือกที่มีรูปแบบชัดเจนเพื่อหลีกเลี่ยงความสับสน
- ใช้ `OPTARG` เพื่อเข้าถึงค่าที่ถูกส่งมาพร้อมกับตัวเลือก
- อย่าลืมจัดการกรณีที่ไม่ถูกต้องเพื่อให้ผู้ใช้ได้รับข้อมูลที่ชัดเจนเมื่อมีการใช้ตัวเลือกที่ไม่ถูกต้อง