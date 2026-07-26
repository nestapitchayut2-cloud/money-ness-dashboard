# ☀️ Weekend Lesson — วันอาทิตย์ที่ 26 กรกฎาคม 2569

**🗓️ Phase 1 / Week 4: Excel — Power Query: Merge Queries (รวม 2 ตารางเป็นตารางเดียว)**

> สัปดาห์ที่แล้วรู้จัก Power Query เบื้องต้น (import + ทำความสะอาดข้อมูล) — วันนี้ต่อยอดตามที่บอกไว้: **Merge Queries** เครื่องมือ "รวม" ข้อมูลจาก 2 ตารางเข้าด้วยกัน โดยอิงคอลัมน์ที่ตรงกัน (คล้าย VLOOKUP แต่เก่งกว่า)

---

## 📖 เรียนรู้อะไรวันนี้ (5 นาที)

**Merge Queries = เอาสองตารางมาต่อกันโดยใช้ "คอลัมน์ร่วม" เป็นตัวจับคู่** เช่น ตารางพอร์ต (มีคอลัมน์ Layer) + ตารางอธิบาย Layer (มีคอลัมน์ Layer เหมือนกัน) → รวมเป็นตารางเดียวที่มีข้อมูลครบ

ทำไมต้องรู้:
- เทียบกับ VLOOKUP: VLOOKUP ต้องเขียนสูตรทีละเซลล์ ข้อมูลเปลี่ยนต้องลากสูตรใหม่ ส่วน Merge ทำ "ขั้นตอน" ไว้ครั้งเดียว กด Refresh ทีหลังก็รวมให้ใหม่อัตโนมัติ
- **Join Kind ที่ใช้บ่อยที่สุด: Left Outer Join** = เก็บทุกแถวจากตารางหลัก (เช่น ตารางพอร์ต) แล้วดึงข้อมูลที่ตรงกันจากตารางรอง (เช่น คำอธิบาย Layer) มาแปะให้ — ถ้าไม่มีข้อมูลตรงกันก็ปล่อยว่าง ไม่ทำให้แถวหลักหาย
- นี่คือ concept เดียวกับที่นักวิเคราะห์ใช้รวมข้อมูลจากหลายแหล่ง (เช่น ยอดขาย + ข้อมูลลูกค้า + ข้อมูล region) ก่อนเอาเข้า Pivot Table หรือ Power BI

**concept สำคัญ:** ตารางหลักไม่ต้องพิมพ์ข้อมูลซ้ำเอง — แค่มี "คอลัมน์ร่วม" ที่ตรงกัน Power Query จะไปดึงข้อมูลจากตารางรองมาแปะให้เอง และถ้าตารางรองมีการแก้ไข กด Refresh ตารางหลักก็อัปเดตตาม

---

## 🎬 ดูก่อน (10 นาที)

**Merge Tables in Excel Using Power Query** — Sumit Bansal (ผู้ก่อตั้ง TrumpExcel.com, Microsoft Excel MVP)
→ https://www.youtube.com/watch?v=M_jIsnksv7I

คลิปยาว **9:53 นาที** พอดีกับเวลา ดูเน้นช่วง **"Merging Table 1 and Table 2"** (ครึ่งแรกของคลิป) เป็นหลัก:
- ช่วงต้น → ทำไมต้องแปลงตารางเป็น Connection ก่อน (From Table/Range → Only Create Connection)
- ช่วงกลาง → วิธีเปิด Merge dialog (Get Data → Combine Queries → Merge) และเลือกคอลัมน์ร่วมทั้งสองตาราง
- ช่วงท้าย (merge ตารางที่ 3 เพิ่ม) เป็นโบนัส ข้ามได้ถ้าเวลาไม่พอ — วันนี้แค่รวม 2 ตารางก็พอ

_(ถ้าอยากอ่านแทนดู: บทความเดียวกันแบบข้อความอยู่ใน English Bonus ด้านล่าง)_

---

## ⚡ ลองทำเลย (15 นาที)

ใช้ไฟล์ `Investment_Portfolio_v3.xlsx` (ตาราง Layer + จำนวนเงิน ที่ทำ Pivot Table ไปแล้วในสัปดาห์ก่อนๆ):

1. สร้างชีตใหม่ พิมพ์ตารางเล็ก 2 คอลัมน์:

   | Layer | คำอธิบาย |
   |---|---|
   | Stable | หุ้นปันผล / ETF / กองทุน |
   | Growth | BTC / หุ้น US / Macro |
   | High-risk | EA / Forex |

   กด **Ctrl+T** แปลงเป็น Table → ไปแท็บ **Table Design** → ช่อง Table Name เปลี่ยนเป็น `tblLayerInfo`

2. คลิกที่ตารางนี้ → แท็บ **Data** → **From Table/Range** → หน้าต่าง Power Query Editor เปิดขึ้นมา → กด **Close & Load** → **Close & Load To** → เลือก **Only Create Connection** → OK

3. ไปที่ตารางพอร์ตหลัก (มีคอลัมน์ Layer + จำนวนเงิน) → ทำแบบเดียวกัน (From Table/Range → Only Create Connection) ถ้ายังไม่เคยทำ

4. แท็บ **Data** → **Get Data** → **Combine Queries** → **Merge**

5. หน้าต่าง Merge: เลือกตารางพอร์ตเป็นตัวแรก, `tblLayerInfo` เป็นตัวสอง → คลิกคอลัมน์ **Layer** ในทั้งสองตารางให้ตรงกัน (สังเกตแถบสีฟ้าคาดที่คอลัมน์)

6. **Join Kind** เลือก **Left Outer (all from first, matching from second)** → กด OK

7. จะเห็นคอลัมน์ใหม่ (nested table) โผล่มาท้ายตาราง → กดปุ่มลูกศรคู่ (⇄) ที่หัวคอลัมน์นั้น → ติ๊กเฉพาะ **คำอธิบาย** → เอาติ๊ก "Use original column name as prefix" ออก → OK

8. **Close & Load** → ตอนนี้ตารางพอร์ตจะมีคอลัมน์คำอธิบายเพิ่มมาเองอัตโนมัติ ไม่ต้องพิมพ์ซ้ำ!

9. ทดสอบพลังจริง: เพิ่ม asset ใหม่ในพอร์ต ใส่ Layer ที่มีอยู่แล้ว (เช่น Growth) → แท็บ Data → **Refresh All** → เช็คว่าคำอธิบายขึ้นเองไหมโดยไม่ต้องพิมพ์

**คำถามให้คิด:** ถ้าอนาคตอยากเพิ่มคอลัมน์ "เป้า % ต่อ Layer" (50/35/15) เข้าไปใน `tblLayerInfo` — ต้องแก้ตารางพอร์ตหลักด้วยไหม หรือแค่แก้ `tblLayerInfo` แล้ว Refresh ก็พอ?

> 📌 สัปดาห์หน้า (2 ส.ค.) ขึ้น Phase ใหม่ในแผน: **SQL concept** — ทำความเข้าใจว่า "query" คืออะไร (ยังไม่ต้องเขียนเอง) ปิดจ็อบ Power Query แค่นี้พอสำหรับตอนนี้

---

## 📰 English Bonus

**บทความ:** "Merge Tables in Excel Using Power Query" — Sumit Bansal (TrumpExcel)
→ https://trumpexcel.com/merge-tables/
_บทความต้นฉบับของคลิปที่ดูด้านบน อธิบายขั้นตอน merge เป็นข้อความทีละสเต็ป ใช้คำศัพท์ตรงกับปุ่มที่เห็นในโปรแกรมจริง อ่านทวนได้ถ้าดูคลิปแล้วยังงงบางจุด_

**Vocab วันนี้** (จดลง `ENGLISH/vocab-list.md`):
- *merge* = รวม/ผสานข้อมูล → "Merge tables to combine data from different sources."
- *connecting column / matching column* = คอลัมน์ที่ใช้จับคู่ระหว่างตาราง → "The connecting column must have no duplicates."
- *duplicate* = ข้อมูลซ้ำ → "Make sure there's no duplicate value in the matching column."

---
_เรียน 30 นาที วันนี้ = ก้าวหนึ่งที่นับได้ 💪_
