# ระบบบริหารงานโรงเรียน School Management System (SMS)
เป็นระบบช่วยเหลือในการบริหารงานโรงเรียน หรือ สถานศึกษา ประกอบด้วย 3 ส่วนหลักๆ
* ระบบฐานข้อมูลบุคคลากร ผู้บริหาร ครู-อาจาร์ย (Personnel)
* ระบบสารบรรณ (E-Document) รับ-ส่ง เอกสารภายในหน่วยงาน
* ระบบเกรดของนักเรียน (School)

จุดประสงค์หลักของโปรเจ็คนี้ เพื่อพัฒนาระบบแสดงเกรดของนักเรียน โดยมีความสามารถเบื้องต้นในการจัดเก็บและรายงานผลการเรียนของนักเรียนเป็นรายบุคคล ระบบพื้นฐานแบ่งผู้ใช้งานออกเป็น 4 กลุ่ม (สามารถเพิ่มเติมได้)
* Admin สามารถทำได้ทุกอย่างบนไซต์
* เจ้าหน้าที่บริหาร ทำได้ทุกอย่างเช่นกัน ยกเว้นการตั้งค่าระบบ
* ครู-อาจาร์ย สามารถจัดการรายวิชาและผลการเรียนของนักเรียนในวิชาที่ตัวเองสอน สามารถจัดการข้อมูลนักเรียนได้ทุกคน
* นักเรียน สามารถเข้าดูผลการเรียนของตัวเอง สามารถดูย้อนหลังได้เป็นรายเทอม

รายละเอียดเพิ่มเติม https://www.kotchasan.com/index.php?module=knowledge&id=89

## ความต้องการของระบบ
* PHP 5.3 ขึ้นไป
* ext-mbstring
* PDO Mysql

## การติดตั้งและการอัปเกรด
1. ให้อัปโหลดโค้ดทั้งหมดจากที่ดาวน์โหลด ขึ้นไปบน Server
2. ในกรณีที่มีการติดตั้งใหม่ ให้เรียกตัวติดตั้ง http://domain.tld/install/ และดำเนินการตามขั้นตอนการติดตั้งจนกว่าจะเสร็จสิ้น
3. ลบไดเร็คทอรี่ install/ ออก
4. ในกรณีเป็นการอัปเกรด ให้ตรวจสอบว่ามีฟิลด์ salt ในตาราง xxx_user (เปลี่ยน xxx เป็น prefix ของเว็บที่ใช้งานอยู่)  หรือไม่ ถ้าไม่มีให้เพิ่มฟิลด์ salt ชนิด VARCHAR(32) ลงในตาราง xxx_user และรันคำสั่ง SQL ```UPDATE xxx_user SET salt=username``` ที่ phpMyAdmin

## การใช้งาน
* เข้าระบบเป็นผู้ดูแลระบบ : ```admin@localhost``` และ Password : ```admin```

## ข้อตกลงการนำไปใช้งาน
* สามารถนำไปใช้งานส่วนตัวได้
* สามารถพัฒนาต่อยอดได้
* มีข้อสงสัยสามารถสอบถามได้ที่บอร์ดของคชสาร https://www.kotchasan.com
* ต้องการให้ผู้เขียนพัฒนาเพิ่มเติม ติดต่อผู้เขียนได้โดยตรง (อาจมีค่าใช้จ่าย)
* ผู้เขียนไม่รับผิดชอบข้อผิดพลาดใดๆในการใช้งาน
* ห้ามขาย ถ้าต้องการนำไปพัฒนาต่อเพื่อขายให้ติดต่อผู้เขียนก่อน (เพื่อบริจาค)

## หากต้องการสนับสนุนผู้เขียน สามารถบริจาคช่วยเหลือค่า Server ได้ที่
```
ธนาคาร กสิกรไทย สาขากาญจนบุรี
เลขที่บัญชี 221-2-78341-5
ชื่อบัญชี กรกฎ วิริยะ
```
