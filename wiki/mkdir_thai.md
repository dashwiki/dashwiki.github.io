# [ไทย] Debian Almquist Shell (dash) mkdir การใช้งาน: สร้างไดเรกทอรีใหม่

## Overview
คำสั่ง `mkdir` ใช้สำหรับสร้างไดเรกทอรีใหม่ในระบบไฟล์ โดยสามารถสร้างไดเรกทอรีได้หลายระดับตามที่ต้องการ

## Usage
รูปแบบพื้นฐานของคำสั่งคือ:

```bash
mkdir [options] [arguments]
```

## Common Options
- `-p`: สร้างไดเรกทอรีทั้งหมดในเส้นทางที่ระบุ หากไดเรกทอรีบางตัวไม่อยู่ จะถูกสร้างขึ้นโดยอัตโนมัติ
- `-m`: ตั้งค่าการอนุญาต (permissions) สำหรับไดเรกทอรีที่สร้างขึ้น
- `-v`: แสดงข้อความที่บอกว่าไดเรกทอรีถูกสร้างขึ้นแล้ว

## Common Examples
ตัวอย่างการใช้งานคำสั่ง `mkdir` มีดังนี้:

1. สร้างไดเรกทอรีใหม่ชื่อ "myfolder":
   ```bash
   mkdir myfolder
   ```

2. สร้างไดเรกทอรีใหม่พร้อมกับไดเรกทอรีย่อย:
   ```bash
   mkdir -p myfolder/subfolder
   ```

3. สร้างไดเรกทอรีใหม่และตั้งค่าการอนุญาตเป็น 755:
   ```bash
   mkdir -m 755 myfolder
   ```

4. แสดงข้อความเมื่อสร้างไดเรกทอรี:
   ```bash
   mkdir -v myfolder
   ```

## Tips
- ใช้ตัวเลือก `-p` เมื่อคุณไม่แน่ใจว่าไดเรกทอรีหลักมีอยู่แล้วหรือไม่ เพื่อหลีกเลี่ยงข้อผิดพลาด
- ตรวจสอบสิทธิ์การเข้าถึงของไดเรกทอรีที่สร้างขึ้นเพื่อให้แน่ใจว่าผู้ใช้ที่ต้องการสามารถเข้าถึงได้
- ใช้ `mkdir` ร่วมกับคำสั่งอื่น ๆ เช่น `cd` เพื่อเปลี่ยนไปยังไดเรกทอรีที่สร้างขึ้นได้ทันที