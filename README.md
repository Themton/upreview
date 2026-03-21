# 🖼️ FB Auto Comment รูปภาพ

คอมเมนต์รูปภาพอัตโนมัติผ่าน Facebook Graph API  
เลือกรูปจากเครื่อง สูงสุด 30 รูป • บันทึกเพจ • เซฟโหมดป้องกันโดนบล็อค

## ✨ ฟีเจอร์

- ✅ คอมเมนต์ด้วยรูปภาพ (ไม่มีตัวอักษร)
- ✅ เลือกรูปจากเครื่อง / ลากวาง (สูงสุด 30 รูป)
- ✅ ดึงชื่อเพจอัตโนมัติเมื่อวาง Token
- ✅ บันทึกเพจ — เปิดครั้งหน้าเลือกได้เลย
- ✅ แปลง URL โพสต์เป็น Post ID อัตโนมัติ
- ✅ 🛡️ เซฟโหมด — สุ่มเวลา + พักทุก 10 รูป
- ✅ หยุดอัตโนมัติเมื่อเจอ Rate Limit
- ✅ แสดงเวลาโดยประมาณก่อนเริ่ม
- ✅ Progress bar + Log ผลลัพธ์พร้อม Thumbnail

## 🔒 ความปลอดภัย

- Token เก็บเฉพาะใน **localStorage** ของเบราว์เซอร์คุณเท่านั้น
- ไม่มี Backend / Server เก็บข้อมูล
- โค้ดเปิดเผยทั้งหมด ตรวจสอบได้

---

## 🚀 วิธี Deploy ผ่าน GitHub Pages

### วิธีที่ 1: ผ่านเว็บ GitHub (ง่ายสุด)

1. **สร้าง Repository ใหม่**
   - ไปที่ [github.com/new](https://github.com/new)
   - ตั้งชื่อ เช่น `fb-auto-comment`
   - เลือก **Public**
   - กด **Create repository**

2. **อัพโหลดไฟล์**
   - กด **uploading an existing file**
   - ลากไฟล์ `index.html` เข้าไป
   - กด **Commit changes**

3. **เปิด GitHub Pages**
   - ไปที่ **Settings** → **Pages**
   - Source: เลือก **Deploy from a branch**
   - Branch: เลือก **main** → **/root**
   - กด **Save**

4. **รอ 1-2 นาที** → เข้าใช้งานได้ที่:
   ```
   https://YOUR_USERNAME.github.io/fb-auto-comment/
   ```

### วิธีที่ 2: ผ่าน Git CLI

```bash
# Clone repo ที่สร้างไว้
git clone https://github.com/YOUR_USERNAME/fb-auto-comment.git
cd fb-auto-comment

# คัดลอก index.html เข้า repo
cp /path/to/index.html .

# Push
git add .
git commit -m "Initial commit"
git push origin main
```

จากนั้นเปิด GitHub Pages ตามวิธีที่ 1 ข้อ 3-4

---

## 📖 วิธีใช้งาน

### เตรียม Facebook

1. สร้าง App ที่ **[developers.facebook.com](https://developers.facebook.com)**
2. เปิด **Graph API Explorer**
3. เลือก App → กด **User or Page** → เลือก **Page Token**
4. เพิ่มสิทธิ์:
   - `pages_manage_posts`
   - `pages_read_engagement`
5. กด **Generate Access Token** → คัดลอก

### ใช้งาน

1. เปิดเว็บ GitHub Pages
2. วาง **Token** → ระบบดึงชื่อเพจอัตโนมัติ + บันทึก
3. ใส่ **Post ID** ของโพสต์ที่จะคอมเมนต์
4. เลือกรูปจากเครื่อง (สูงสุด 30 รูป)
5. ตั้งหน่วงเวลา + เปิดเซฟโหมด
6. กด **🚀 เริ่ม**

### หา Post ID

เปิดโพสต์ → คลิกขวาที่วันที่โพสต์ → Copy Link

```
https://www.facebook.com/PAGE_NAME/posts/123456789
```

Post ID = `PAGE_ID_123456789`

---

## ⚠️ ป้องกันโดนบล็อค

| ตั้งค่า | แนะนำ |
|---------|-------|
| หน่วงเวลา | ≥ 5 วินาที |
| เซฟโหมด | เปิด ✅ |
| จำนวนรูป | ≤ 30 รูป/โพสต์ |
| ถ้าเจอ Error 368 | หยุดรอ 1-2 ชม. |

---

## 📄 License

MIT — ใช้ได้อิสระ
