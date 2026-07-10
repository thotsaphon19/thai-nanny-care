# Thai Nanny Care — Prototype (Vercel Deploy)

เว็บแอปตัวอย่าง (prototype) สำหรับพรีเซนต์อาจารย์ เป็น static site ล้วน ๆ
(ไม่ต้อง build, ไม่ต้องติดตั้ง dependency ใด ๆ) — ไฟล์ `index.html` เพียงไฟล์เดียว
รวม React + Babel ไว้ในตัวแล้ว

## วิธี Deploy บน Vercel (เลือกวิธีใดวิธีหนึ่ง)

### วิธีที่ 1: ใช้ Vercel CLI (เร็วที่สุด ไม่ต้องมี GitHub)
1. ติดตั้ง Vercel CLI (ครั้งเดียว):
   ```
   npm install -g vercel
   ```
2. เข้ามาที่โฟลเดอร์นี้ แล้วรันคำสั่ง:
   ```
   cd vercel-project
   vercel --prod
   ```
3. ทำตามขั้นตอนที่ CLI ถาม (ล็อกอิน/สร้างบัญชี Vercel ถ้ายังไม่มี, ตั้งชื่อโปรเจกต์)
4. เสร็จแล้วจะได้ลิงก์ เช่น `https://your-project.vercel.app` ใช้เปิดให้อาจารย์ดูได้ทันที

### วิธีที่ 2: ผ่านเว็บ Vercel (ไม่ต้องใช้ Terminal)
1. อัปโหลดโฟลเดอร์นี้ขึ้น GitHub (สร้าง repo ใหม่ แล้วลากไฟล์ `index.html`, `vercel.json` ขึ้นไป)
2. ไปที่ https://vercel.com → New Project → Import Git Repository → เลือก repo ที่เพิ่งสร้าง
3. Framework Preset เลือก **Other** (Vercel จะ deploy เป็น static site ให้อัตโนมัติ)
4. กด Deploy รอสักครู่ก็จะได้ลิงก์ใช้งานจริง

## หมายเหตุ
- แอปนี้ใช้ `localStorage` ของเบราว์เซอร์ผู้ใช้แต่ละคนเก็บข้อมูล (ราคาที่แอดมินแก้, สถานะพี่เลี้ยง, รีวิว ฯลฯ)
  ดังนั้นข้อมูลจะไม่ sync ข้ามอุปกรณ์/เบราว์เซอร์ — เหมาะสำหรับ demo คนเดียวหรือเปิดเครื่องเดียวพรีเซนต์
- รูปโปรไฟล์พี่เลี้ยง (pravatar.cc) และฟอนต์ (Google Fonts) โหลดจากอินเทอร์เน็ต ต้องมีเน็ตตอนเปิดใช้งาน
- ไม่มี backend/database จริง ทุกอย่างเป็นข้อมูลจำลอง (mock) เพื่อสาธิตแนวคิดเท่านั้น
