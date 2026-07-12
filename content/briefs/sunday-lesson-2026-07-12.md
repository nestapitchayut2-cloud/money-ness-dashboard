# ☀️ Weekend Lesson — วันอาทิตย์ที่ 12 กรกฎาคม 2569

**🗓️ Phase 1 / Week 2: Excel — Pivot Table (ปิดท้าย) → PivotChart + เตรียมขึ้น Power Query**

> สัปดาห์ที่แล้วทำ % of Grand Total เช็คพอร์ต 50/35/15 ได้แล้ว — วันนี้ปิดจ็อบ Pivot Table ด้วยการ "เปลี่ยนตารางเป็นกราฟ" ที่อัปเดตอัตโนมัติ

---

## 📖 เรียนรู้อะไรวันนี้ (5 นาที)

**PivotChart คือ Pivot Table เวอร์ชันกราฟ** — พอลากข้อมูลเปลี่ยน กราฟก็ขยับตามทันที ไม่ต้องวาดใหม่

ทำไมต้องรู้:
- ตัวเลขในตารางดูยาก แต่กราฟวงกลม/แท่งเห็นปุ๊บรู้เลยว่า "BTC กินพอร์ตเกินไปไหม"
- นี่คือทักษะเดียวกับที่จะใช้ตอนทำ **Dashboard พอร์ตตัวเอง** ใน Power BI (Phase 2) — PivotChart คือเวอร์ชันฝึกมือก่อน
- เอาไปทำ content ของ The Money Ness ได้เลย (ภาพกราฟพอร์ต = single image ดี ๆ หนึ่งภาพ)

**concept สำคัญ:** กราฟไม่ใช่การ "วาด" แต่คือการ "ผูก" กับข้อมูล — ข้อมูลเปลี่ยน กราฟเปลี่ยนเอง

---

## 🎬 ดูก่อน (10 นาที)

**How to create a PivotChart in Excel | Microsoft** (ช่องทางการของ Microsoft — สั้น กระชับ)
→ https://www.youtube.com/watch?v=7IbW_DF89Ws
ดูจนจบคลิป (สั้นมาก) แล้วโฟกัสตอนที่เขากด **Insert → PivotChart** และเลือกชนิดกราฟ

_(ถ้าอยากอ่านแทนดู: Microsoft Support "Create a PivotChart" → https://support.microsoft.com/en-us/office/create-a-pivotchart-c1b1e057-6990-4c38-b52b-8255538e7b1c )_

---

## ⚡ ลองทำเลย (15 นาที)

ใช้ Pivot Table ที่ทำไว้สัปดาห์ที่แล้ว (Layer = Stable/Growth/High-risk + จำนวนเงิน) หรือไฟล์ `Investment_Portfolio_v3.xlsx`:

1. คลิกที่ Pivot Table เดิม → เมนู **Insert** → กด **PivotChart**
2. เลือกกราฟ **Pie (วงกลม)** → กด OK
3. ตอนนี้จะเห็นพอร์ตแยกเป็น 3 ก้อน Stable/Growth/High-risk เป็นวงกลม
4. คลิกขวาที่กราฟ → **Add Data Labels** → เลือกให้โชว์ **%** จะเห็นสัดส่วนบนกราฟเลย
5. เทียบกับเป้า 50/35/15 ด้วยตา — ก้อนไหนใหญ่/เล็กกว่าที่ควรจะเป็น?
6. โบนัส: เปลี่ยนเป็นกราฟ **แท่ง (Column)** โดยคลิกกราฟ → **Change Chart Type** เพื่อดูว่าแบบไหนสื่อง่ายกว่ากัน

**คำถามให้คิด:** ถ้าจะโพสต์ภาพนี้ลง The Money Ness — pie หรือ bar อันไหนที่คนเลื่อนผ่านแล้วเข้าใจใน 1 วินาที?

> 📌 **สัปดาห์หน้า (19 ก.ค.) ขึ้นเรื่องใหม่: Power Query** — เครื่องมือ "ทำความสะอาดข้อมูล" ก่อนเอาเข้า Pivot จบ Pivot Table แค่นี้พอสำหรับตอนนี้

---

## 📰 English Bonus

**บทความ:** "Create a PivotChart" — Microsoft Support
→ https://support.microsoft.com/en-us/office/create-a-pivotchart-c1b1e057-6990-4c38-b52b-8255538e7b1c
_เป็นคู่มือทางการที่บอกทีละขั้นว่าจะสร้างกราฟจาก pivot ยังไง — อ่านคำสั่งภาษาอังกฤษจริงที่ขึ้นในโปรแกรม จะได้ชินกับปุ่ม_

**Vocab วันนี้** (จดลง `ENGLISH/vocab-list.md`):
- *chart* = แผนภูมิ/กราฟ → "Insert a chart to visualize the data."
- *label* = ป้ายกำกับ (ตัวเลขบนกราฟ) → "Add data labels to show the percentage."
- *visualize* = ทำให้เห็นเป็นภาพ → "A pie chart helps you visualize your portfolio."

---
_เรียน 30 นาที วันนี้ = ก้าวหนึ่งที่นับได้ 💪_
