# Rework — ระบบติดตามม้วน (Roll Tracking)

เว็บแอปบนมือถือสำหรับติดตามงานพนักงานกับม้วน โดยการแสกน QR

## การใช้งาน
1. พนักงานเลือกชื่อตัวเอง → เข้าสู่ระบบ
2. แสกน QR ที่ติดอยู่บนม้วน (กล้องมือถือ)
3. กด **รับเข้า** หรือ **เบิกออก** พร้อมหมายเหตุ
4. ดูประวัติของม้วนได้ทันที ว่าใครทำอะไร เมื่อไหร่

## เทคโนโลยี
- ไฟล์เดียว `index.html` (HTML/JS ล้วน)
- แสกน QR ด้วย [html5-qrcode](https://github.com/mebjas/html5-qrcode)
- ฐานข้อมูล [Supabase](https://supabase.com) (ตาราง `employees`, `rolls`, `roll_events`)

## Deploy
กล้องต้องการ HTTPS — ใช้ GitHub Pages / Netlify / Vercel / Cloudflare Pages
> หมายเหตุ: คีย์ที่ฝังในไฟล์เป็น Supabase *publishable key* ซึ่งออกแบบมาให้เปิดเผยต่อ client ได้
