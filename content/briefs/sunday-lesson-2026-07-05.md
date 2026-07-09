# ☀️ Weekend Lesson — วันอาทิตย์ที่ 5 กรกฎาคม 2569

**🗓️ Phase 1 / Week 1: Excel — Pivot Table (ภาค 2: ใช้กับพอร์ตจริง)**

> 📌 บทเรียนนี้สร้างย้อนหลัง — task วันที่ 5 ก.ค. รันแล้วแต่ไฟล์ไม่ถูกบันทึก (แก้ระบบแล้ว 9 ก.ค.)

---

## 📖 เรียนรู้อะไรวันนี้ (5 นาที)

สัปดาห์ที่แล้วรู้จัก Pivot Table พื้นฐาน (ลาก Rows + Values) — วันนี้ต่อยอด 3 ท่าที่นักวิเคราะห์ใช้จริงทุกวัน:

1. **Group by เดือน** — สรุปยอดซื้อขายรายเดือนอัตโนมัติจากคอลัมน์วันที่
2. **% of Grand Total** — เปลี่ยนตัวเลขดิบเป็นสัดส่วน เช่น "BTC กินพอร์ตกี่ %" (ตรงกับการเช็ค 50/35/15 ของเราพอดี)
3. **Filter/Slicer** — กดปุ่มเดียวเห็นเฉพาะ asset ที่สนใจ

ทำไมต้องรู้: นี่คือท่าที่ใช้เช็คว่าพอร์ตยังเป็น 50/35/15 จริงไหม โดยไม่ต้องเขียนสูตรเลย

---

## 🎬 ดูก่อน (10 นาที)

ค้นใน YouTube: **"Excel Pivot Table Group by Month % of Total"** เลือกคลิปของ Leila Gharani หรือ ExcelIsFun ที่สั้นกว่า 15 นาที (ดูถึงตอนจบส่วน % of Total พอ)
_(ถ้าไม่อยากดู video: chandoo.org → search "pivot table percentage")_

---

## ⚡ ลองทำเลย (15 นาที)

ใช้ไฟล์ `Investment_Portfolio_v3.xlsx` ใน Claude Workspace หรือพิมพ์ตารางเทรดจากบทเรียน 28 มิ.ย. เพิ่มคอลัมน์ "Layer" (Stable/Growth/High-risk):

1. สร้าง Pivot Table ใหม่จากตาราง
2. ลาก **Layer** → Rows, **จำนวนเงิน** → Values
3. คลิกขวาที่ตัวเลขใน Values → **Show Values As → % of Grand Total**
4. เทียบผลกับเป้า 50/35/15 — เลเยอร์ไหนเกิน/ขาด?
5. โบนัส: ลาก **วันที่** → Rows แล้วคลิกขวา → **Group → Months** ดูว่าเดือนไหนซื้อเยอะสุด

**คำถามให้คิด:** ถ้าพอร์ตจริงตอนนี้ High-risk เกิน 15% — เงินใหม่เดือนหน้าควรเข้าเลเยอร์ไหน?

---

## 📰 English Bonus

ค้น: **"How to analyze your investment portfolio in Excel"** (Investopedia/Microsoft Learn)
Vocab วันนี้: *allocation* (การจัดสรร), *rebalance* (ปรับสมดุลพอร์ต), *grand total* (ยอดรวมทั้งหมด) → จดลง `ENGLISH/vocab-list.md`

---
_เรียน 30 นาที วันนี้ = ก้าวหนึ่งที่นับได้ 💪_
_สัปดาห์หน้า (12 ก.ค.): Pivot Table week 2 ปิดท้าย → เตรียมขึ้น Power Query_
