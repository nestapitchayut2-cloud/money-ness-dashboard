# system/ — สำเนาไฟล์อ้างอิงสำหรับ Claude อ่านทางไกล (The Money Ness)

โฟลเดอร์นี้เก็บ**สำเนาอ่านอย่างเดียว (read-only mirror)** ของไฟล์อ้างอิงที่ Claude
ใช้ก่อนเขียน Content ทุกครั้ง เก็บไว้ในนี้ (public repo) เพื่อให้ Claude
อ่านได้ผ่าน GitHub โดยตรงตอนที่**ไม่ได้เชื่อมต่อคอมพิวเตอร์ของ Ness**

## ⚠️ ต้นฉบับตัวจริงอยู่ที่เครื่อง Ness เท่านั้น — ห้ามแก้ไฟล์ในนี้โดยตรง

ไฟล์ในนี้เป็นแค่ "ภาพถ่าย" ของต้นฉบับ ณ เวลาที่ sync ล่าสุด ต้นฉบับตัวจริง
(ที่ระบบทั้งหมดของ Ness ใช้งานจริง — MASTER-WORKFLOW.md, scheduled tasks
ต่างๆ, และ IB Forex) ยังอยู่ที่ `SHARED/` บนเครื่อง Ness เหมือนเดิมทุกอย่าง:

- `SHARED/ness-profile.md` — ตัวตนและสไตล์ของ Ness
- `SHARED/weekly-topics.md` — Layer + หัวข้อประจำสัปดาห์ (มี section forex ที่ IB Forex ใช้ด้วย)
- `SHARED/style-guide.md` — Reel DNA, tone, โครงสร้าง, CTA rules, Gemini Image Brief format
- `SHARED/content-calendar.md` — ปฏิทิน content ที่ทำไปแล้ว/กำลังทำ
- `SHARED/fact-check-protocol.md` — กฎการ fact-check ตัวเลขก่อนตีพิมพ์
- `MASTER-WORKFLOW.md` (root ของ Claude Workspace) — กฎระบบรวม ใช้กับหลายโปรเจค ไม่ใช่แค่ The Money Ness

## กติกา sync

Claude จะ copy เนื้อหาจาก `SHARED/` มาทับไฟล์ในโฟลเดอร์นี้ทุกครั้งที่เชื่อมต่อ
คอมพิวเตอร์ Ness และมีการแก้ไฟล์อ้างอิงพวกนี้ — เพื่อให้สำเนาทางไกลไม่เก่าเกินไป
**ถ้า Ness แก้ไฟล์ใน `SHARED/` เอง แล้วยังไม่เห็นการเปลี่ยนแปลงในนี้ แปลว่ายัง
ไม่ได้ sync รอบล่าสุด** — บอก Claude ให้ sync ให้ได้เลยตอนที่เชื่อมคอมอยู่

(หมายเหตุ: เดิมทีตั้งใจให้โฟลเดอร์นี้เป็นต้นฉบับตัวจริง แต่พบว่า MASTER-WORKFLOW.md
และ Scheduled tasks หลายตัวอ้างอิง path `SHARED/...` แบบ hardcode ไว้อยู่แล้ว
— ย้ายต้นฉบับจริงออกจาก `SHARED/` เลยจะทำให้ระบบอื่นพังโดยไม่ตั้งใจ จึงเปลี่ยนมา
ใช้โมเดล "sync ทางเดียว" แทน ปลอดภัยกว่าและไม่ต้องแก้ไฟล์ระบบอื่นหลายสิบจุด)
