# Golf Shot Decision Assistant (Thai UI)

เว็บแอป MVP แบบไฟล์เดียว (index.html) สำหรับช่วยตัดสินใจเลือกวิธีตีในแต่ละช็อตและเรียนรู้จาก Feedback ของผู้ใช้ (เก็บใน localStorage)

## โครงสร้าง
```
.
├─ index.html      # แอปหลัก พร้อมใช้งานบน GitHub Pages
├─ .nojekyll       # ปิดการประมวลผล Jekyll (กันไฟล์/โฟลเดอร์ที่ขึ้นต้นด้วย _)
└─ README.md
```

## วิธี Deploy ด้วย GitHub Web (ง่ายสุด)
1. สร้าง Repository ใหม่บน GitHub (Public) — ตั้งชื่ออะไรก็ได้ เช่น `golf-shot-assistant`  
2. อัปโหลดไฟล์ทั้งหมดจาก zip นี้ (`index.html`, `.nojekyll`, `README.md`) เข้าไปใน repo
3. ไปที่ **Settings → Pages**
4. ในหัวข้อ **Build and deployment**:
   - Source: เลือก **Deploy from a branch**
   - Branch: เลือก **main** และโฟลเดอร์ **/** (root) แล้วกด **Save**
5. รอสักครู่ หน้าเว็บจะอยู่ที่ URL: `https://<ชื่อผู้ใช้>.github.io/<ชื่อ-repo>/`  
   - ถ้าอยากให้เป็น root domain ของ Pages ให้ตั้งชื่อ repo เป็น `<ชื่อผู้ใช้>.github.io`

## วิธี Deploy ด้วย Git (ทางเลือก)
```bash
git init
git add .
git commit -m "Initial commit: Golf Shot Decision Assistant"
git branch -M main
git remote add origin https://github.com/<USER>/<REPO>.git
git push -u origin main
```
จากนั้นเปิด **Settings → Pages** และตั้งค่าเหมือนขั้นตอนด้านบน

## การแก้ไข/อัปเดต
- แก้ไข `index.html` แล้ว commit/push ใหม่ GitHub Pages จะอัปเดตให้อัตโนมัติ
- ถ้าต้องการเพิ่มโดเมนส่วนตัว ให้ตั้งค่า CNAME ใน Settings → Pages

## หมายเหตุ
- แอปนี้ไม่ใช้ backend และไม่เรียก API ภายนอก จึงรันได้ 100% บน GitHub Pages
- ข้อมูลการเรียนรู้ (weights/logs) ถูกเก็บใน `localStorage` ของเบราว์เซอร์เครื่องผู้ใช้
- สามารถ Export/Import โปรไฟล์ได้ที่เมนูในหน้าเว็บ
```

