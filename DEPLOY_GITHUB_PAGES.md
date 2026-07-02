# วิธีอัปโหลดขึ้น GitHub Pages

ปัญหาที่พบบ่อย: เปิดในเครื่องได้ แต่ขึ้นเว็บแล้ว CSS หายหรือกดวิชาแล้ว 404

สาเหตุคือ GitHub Pages ต้องมีโครงไฟล์ครบที่ root ของ repository:

- index.html
- assets/css/base.css
- assets/js/app.js
- assets/images/ui/bg_soft.webp
- subjects/math/index.html
- subjects/math/hour-01.html ...
- subjects/thai/index.html ...

## วิธีอัปโหลดที่ถูกต้อง

1. แตกไฟล์ ZIP นี้ก่อน
2. เข้าโฟลเดอร์ที่แตกออกมา
3. อัปโหลด “ไฟล์และโฟลเดอร์ข้างในทั้งหมด” ไปไว้ที่ root ของ repository
4. อย่าอัปโหลดเฉพาะ index.html
5. อย่าอัปโหลดทั้งโฟลเดอร์เป็นชั้นซ้อน เช่น little_steps_v2_ready_to_teach_v6/index.html
6. รอ GitHub Pages build ประมาณ 1–3 นาที แล้วกด Ctrl+F5 รีเฟรช

## โครงที่ต้องเห็นใน GitHub repository

Little-Steps/
├─ index.html
├─ assets/
│  ├─ css/base.css
│  ├─ js/app.js
│  └─ images/ui/bg_soft.webp
└─ subjects/
   ├─ math/index.html
   ├─ thai/index.html
   ├─ english/index.html
   ├─ science/index.html
   ├─ social/index.html
   ├─ computer/index.html
   └─ early-childhood/index.html

ถ้า URL /subjects/math/index.html ขึ้น 404 แปลว่าโฟลเดอร์ subjects ไม่ได้อยู่ที่ root หรือยังไม่ได้ถูกอัปโหลดขึ้น GitHub
