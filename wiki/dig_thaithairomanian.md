# [Bash] dig ใช้: ค้นหาข้อมูล DNS

## Overview
คำสั่ง `dig` (Domain Information Groper) เป็นเครื่องมือที่ใช้ในการค้นหาข้อมูล DNS (Domain Name System) ซึ่งช่วยให้ผู้ใช้สามารถตรวจสอบและวิเคราะห์การตั้งค่าของ DNS ได้อย่างง่ายดาย

## Usage
การใช้คำสั่ง `dig` มีรูปแบบพื้นฐานดังนี้:

```bash
dig [options] [arguments]
```

## Common Options
- `@server`: ระบุ DNS server ที่ต้องการใช้ในการค้นหา
- `-t type`: ระบุประเภทของข้อมูลที่ต้องการค้นหา เช่น A, MX, TXT
- `+short`: แสดงผลลัพธ์ในรูปแบบที่สั้นและเข้าใจง่าย
- `+trace`: ติดตามการค้นหาจาก root DNS server ไปยัง authoritative server

## Common Examples
1. ค้นหาที่อยู่ IP ของโดเมน:
   ```bash
   dig example.com
   ```

2. ค้นหาข้อมูล MX records ของโดเมน:
   ```bash
   dig -t MX example.com
   ```

3. ค้นหาข้อมูล DNS จาก DNS server ที่กำหนด:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. แสดงผลลัพธ์แบบสั้น:
   ```bash
   dig +short example.com
   ```

5. ติดตามการค้นหาจาก root DNS server:
   ```bash
   dig +trace example.com
   ```

## Tips
- ใช้ `+short` เพื่อให้ผลลัพธ์ที่ได้อ่านง่ายและรวดเร็ว
- หากต้องการตรวจสอบการตั้งค่า DNS ของโดเมนที่คุณเป็นเจ้าของ ควรใช้ DNS server ของผู้ให้บริการโดเมนของคุณ
- การใช้ `+trace` จะช่วยให้คุณเห็นเส้นทางการค้นหาข้อมูล DNS ซึ่งสามารถช่วยในการวิเคราะห์ปัญหาได้ดี