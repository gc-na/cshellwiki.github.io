# [ไทย] Bash docker-compose การใช้งาน: จัดการคอนเทนเนอร์ Docker

## Overview
คำสั่ง `docker-compose` ใช้สำหรับจัดการแอปพลิเคชันที่ประกอบด้วยหลายคอนเทนเนอร์ Docker โดยสามารถกำหนดการตั้งค่าต่างๆ ในไฟล์ `docker-compose.yml` และทำให้การจัดการคอนเทนเนอร์เป็นเรื่องง่ายและสะดวกยิ่งขึ้น

## Usage
รูปแบบพื้นฐานของคำสั่งคือ:
```bash
docker-compose [options] [arguments]
```

## Common Options
- `up`: สร้างและเริ่มคอนเทนเนอร์
- `down`: หยุดและลบคอนเทนเนอร์ที่ทำงานอยู่
- `build`: สร้างภาพ Docker ใหม่จากไฟล์ Dockerfile
- `logs`: แสดงบันทึกการทำงานของคอนเทนเนอร์
- `ps`: แสดงสถานะของคอนเทนเนอร์ที่กำลังทำงาน

## Common Examples
- เริ่มคอนเทนเนอร์ทั้งหมดที่กำหนดในไฟล์ `docker-compose.yml`:
  ```bash
  docker-compose up
  ```

- หยุดและลบคอนเทนเนอร์ทั้งหมด:
  ```bash
  docker-compose down
  ```

- สร้างภาพ Docker ใหม่:
  ```bash
  docker-compose build
  ```

- แสดงบันทึกการทำงานของคอนเทนเนอร์:
  ```bash
  docker-compose logs
  ```

- แสดงสถานะของคอนเทนเนอร์:
  ```bash
  docker-compose ps
  ```

## Tips
- ใช้ `-d` เพื่อรันคอนเทนเนอร์ในโหมดเบื้องหลัง:
  ```bash
  docker-compose up -d
  ```

- ตรวจสอบไฟล์ `docker-compose.yml` ให้ถูกต้องก่อนรันคำสั่ง เพื่อหลีกเลี่ยงข้อผิดพลาดในการสร้างคอนเทนเนอร์

- ใช้คำสั่ง `docker-compose exec` เพื่อเข้าถึงเชลล์ของคอนเทนเนอร์ที่กำลังทำงานอยู่:
  ```bash
  docker-compose exec <service_name> bash
  ```