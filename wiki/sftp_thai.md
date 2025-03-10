# [ไทย] Debian Almquist Shell (dash) sftp การใช้งาน: การถ่ายโอนไฟล์ผ่าน SSH

## Overview
คำสั่ง `sftp` ใช้สำหรับการถ่ายโอนไฟล์ระหว่างเครื่องคอมพิวเตอร์ผ่านโปรโตคอล SSH ซึ่งช่วยให้การส่งข้อมูลมีความปลอดภัยและเข้ารหัส

## Usage
รูปแบบพื้นฐานของคำสั่งคือ:

```bash
sftp [options] [user@]host
```

## Common Options
- `-o` : ใช้เพื่อระบุตัวเลือกการเชื่อมต่อเพิ่มเติม
- `-P` : ระบุพอร์ตที่ต้องการเชื่อมต่อ
- `-b` : ใช้เพื่อระบุไฟล์แบตช์สำหรับการดำเนินการหลายคำสั่ง

## Common Examples
- เชื่อมต่อกับเซิร์ฟเวอร์ SFTP:
```bash
sftp user@hostname
```

- ดาวน์โหลดไฟล์จากเซิร์ฟเวอร์:
```bash
get remote_file.txt
```

- อัปโหลดไฟล์ไปยังเซิร์ฟเวอร์:
```bash
put local_file.txt
```

- ดาวน์โหลดไดเรกทอรีทั้งหมด:
```bash
get -r remote_directory
```

## Tips
- ใช้ `-b` เพื่อทำงานกับไฟล์แบตช์เมื่อคุณมีหลายคำสั่งที่ต้องการดำเนินการ
- ตรวจสอบการเชื่อมต่อ SSH ของคุณก่อนที่จะใช้ `sftp` เพื่อให้แน่ใจว่าการเชื่อมต่อทำงานได้อย่างถูกต้อง
- ใช้คำสั่ง `ls` ภายใน sftp เพื่อดูรายการไฟล์ในไดเรกทอรีปัจจุบันบนเซิร์ฟเวอร์