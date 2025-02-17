# [Linux] Bash endif: [conditional statement termination]

## Overview
คำสั่ง `endif` ใน Bash ใช้เพื่อสิ้นสุดบล็อกของคำสั่งเงื่อนไขที่เริ่มต้นด้วย `if` โดยช่วยในการจัดระเบียบโค้ดและทำให้การอ่านง่ายขึ้น มันเป็นส่วนหนึ่งของโครงสร้างการควบคุมที่ช่วยให้ผู้ใช้สามารถกำหนดเงื่อนไขในการดำเนินการต่าง ๆ ได้

## Usage
การใช้งานพื้นฐานของคำสั่ง `endif` จะอยู่ในรูปแบบดังนี้:

```bash
if [ condition ]; then
    # commands
fi
```

## Common Options
คำสั่ง `endif` ไม่มีตัวเลือกที่เฉพาะเจาะจง เนื่องจากมันเป็นเพียงการสิ้นสุดของบล็อกเงื่อนไขที่เริ่มต้นด้วย `if` แต่ต้องใช้ร่วมกับคำสั่ง `if`, `then`, และ `fi` เพื่อให้โครงสร้างสมบูรณ์

## Common Examples
นี่คือตัวอย่างการใช้งาน `endif` ในสคริปต์ Bash:

### Example 1: Basic If Statement
```bash
if [ -f "file.txt" ]; then
    echo "File exists."
fi
```

### Example 2: If-Else Statement
```bash
if [ -d "directory" ]; then
    echo "Directory exists."
else
    echo "Directory does not exist."
fi
```

### Example 3: Nested If Statement
```bash
if [ -f "file.txt" ]; then
    echo "File exists."
    if [ -r "file.txt" ]; then
        echo "File is readable."
    fi
fi
```

## Tips
- ตรวจสอบให้แน่ใจว่าใช้ `fi` เพื่อปิดบล็อก `if` เสมอ เพื่อหลีกเลี่ยงข้อผิดพลาดในการทำงานของสคริปต์
- ใช้การจัดรูปแบบที่เหมาะสมเพื่อให้โค้ดอ่านง่าย โดยการจัดระเบียบบล็อก `if` และ `endif` ให้ชัดเจน
- สามารถใช้ `elif` เพื่อเพิ่มเงื่อนไขเพิ่มเติมในบล็อก `if` ได้ ซึ่งจะช่วยให้โค้ดมีความยืดหยุ่นมากขึ้น