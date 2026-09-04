> ⚠️ **ไฟล์นี้เป็นสำเนา (mirror)** ของ `MASTER-WORKFLOW.md` ที่ root ของ Claude Workspace ซึ่งยังเป็นต้นฉบับตัวจริงอยู่ (ใช้กับหลายโปรเจกต์ ไม่ใช่แค่ The Money Ness) ก๊อปปี้มาไว้ที่นี่เพื่อให้ Claude อ่านได้ตอนไม่ได้เชื่อมต่อคอม แต่ **อาจไม่ทันสมัยที่สุด** ถ้าแก้ MASTER-WORKFLOW.md ตัวจริงเมื่อไหร่ ให้ก๊อปปี้มาทับไฟล์นี้อีกครั้งด้วย

# MASTER WORKFLOW INSTRUCTIONS
# ไฟล์นี้ Cowork ต้องอ่านทุกครั้งก่อนเริ่มงาน
# Owner: Ness | The Money Ness System
# Path: C:\Users\NP\Desktop\Claude Workspace\MASTER-WORKFLOW.md

---

## 🔴 CRITICAL RULES — อ่านก่อนทำทุกอย่าง

1. อ่าน about-me.md ก่อนเริ่มงานทุกครั้งเสมอ
1b. อ่าน SHARED/ness-profile.md ก่อนงานวางแผน การตัดสินใจ หรืองานที่เกี่ยวกับเป้าหมายระยะยาว
1c. อ่าน SHARED/style-guide.md ก่อนสร้าง content ทุกชิ้น — เป็น source of truth สำหรับ tone, format, และ decisions ล่าสุด
2. Content ทุกชิ้นต้องเป็นภาษาไทย 100% ห้าม exception
3. ⚠️ FACT-CHECK ก่อน publish เสมอ — อ่าน SHARED/fact-check-protocol.md ทุกครั้งที่เนื้อหามีตัวเลขภาษี กฎหมาย ชื่อผลิตภัณฑ์การเงิน หรือราคาตลาด → ค้น web verify ก่อน ห้าม assume ว่าข้อมูลเดิมยังถูก (กรณีตัวอย่าง: SSF ยกเลิกแล้ว Thai ESG มาแทน)
4. บันทึกทุกไฟล์ตาม folder structure ที่กำหนดเท่านั้น
5. อัพเดท SHARED/content-calendar.md ทุกครั้งหลังสร้าง content
6. เมื่อสร้างไฟล์ morning brief / daily orientation → บันทึก 2 ที่เสมอ: market-research/ และ SHARED/morning-brief-latest.md
7. บันทึก Quiz Result ลง FINANCE-LEARNING/quiz-results/quiz-log.md ทุกครั้งหลัง Quiz
8. บันทึก Content Performance ลง SHARED/content-performance-tracker.md ทุกครั้งหลังโพสต์ 48 ชม.
9. IB Forex และ YouTube — **พักไว้ก่อน** (as of มิ.ย. 2026) ไม่ต้องทำงานใน 2 project นี้จนกว่า Ness จะบอก
10. ⚠️ **แยกให้ชัดว่า "รอคอนเฟิร์ม" ใช้กับอะไร** (แก้ 3 ส.ค. 2569 — กฎเดิมเขียนรวมกันจน morning brief ไม่ถูก push ติดต่อกัน 4 วัน)
    - **Content ที่จะเอาไปโพสต์จริง (Reels / Post / Caption)** → ส่งให้ Ness อ่านก่อน **รอคอนเฟิร์มแล้วค่อย push** เพราะเป็นของที่จะออกสู่สาธารณะ
      → `content/posts/` + อัปเดต `content/index.json`
    - **Morning Brief / Learning Brief / Sunday Lesson / ผล Quiz** → **push ทันทีในรอบเดียวกัน ห้ามรอคอนเฟิร์ม** เพราะเป็นของที่ Ness ต้องเปิดอ่านบน dashboard เอง ถ้ารอคอนเฟิร์มก่อน = Ness ไม่มีทางเห็นตั้งแต่แรก (เป็นงูกินหาง)
      → Morning Brief: `content/morning/` | Learning Brief / Lesson: `content/briefs/` + อัปเดต `content/index.json`
    - Repo: `nestapitchayut2-cloud/money-ness-dashboard` | **Token: อ่านจากไฟล์ `SYSTEM/github-token.txt` เท่านั้น ห้ามเขียน token ลงในไฟล์ใดๆ** (เคยมี PAT เก่าฝังอยู่ในบรรทัดนี้ หมดอายุแล้วทำให้ push ล้มเหลวโดยไม่รู้ตัว)

---

## 📂 FOLDER STRUCTURE — Claude ต้องจำ

```
Claude Workspace/
├── about-me.md                         ← อ่านทุกครั้ง
├── MASTER-WORKFLOW.md                  ← ไฟล์นี้
│
├── SHARED/                             ← Cross-project bridge
│   ├── ness-profile.md                 ← ⭐ อ่านก่อนงานวางแผน — ตัวตน เป้าหมาย 3 phases
│   ├── goal-framework.md              ← Goal Framework v2.0 — 50/35/15, 3 Projects, KPI
│   ├── action-plan.md                 ← แผนรายวัน/สัปดาห์/เดือน/ปี + Early Warning
│   ├── learning-curriculum.md         ← Curriculum 3 layers × 12 episodes
│   ├── fact-check-protocol.md         ← ⭐ Fact-Check Protocol — อ่านก่อน publish ทุกครั้ง
│   ├── style-guide.md                 ← อ่านก่อนสร้าง content ทุกครั้ง
│   ├── morning-brief-latest.md        ← Daily Orientation ล่าสุด
│   ├── weekly-topics.md               ← Topics + Learning Topics สัปดาห์นี้ (5 columns)
│   ├── dashboard.html                 ← เปิดใน browser: KPI + Learning Hub + Vocab + Brief Archive
│   ├── content-angles.md              ← รวม ideas ทุก project
│   └── content-calendar.md            ← Master schedule
│
├── FINANCE-LEARNING/
│   ├── market-research/               ← morning brief archive
│   ├── study-notes/                   ← study notes แต่ละ topic
│   └── quiz-results/                  ← quiz log
│
├── THE-MONEY-NESS/
│   ├── drafts/week-[date]/            ← content drafts รายสัปดาห์
│   ├── published/                     ← โพสต์ที่ publish แล้ว
│   ├── reels-scripts/                 ← Reels scripts
│   └── youtube-scripts/              ← YouTube scripts
│
├── IB-FOREX/
│   ├── drafts/                        ← forex content drafts
│   └── published/                     ← โพสต์ที่ publish แล้ว
│
└── ENGLISH/
    └── vocab-list.md                  ← vocab ที่เรียนใหม่
```

---

## 🟢 PROJECT 1 — THE MONEY NESS

### ตัวตน
- เพจสำหรับมนุษย์เงินเดือนไทยที่อยากลงทุน
- เล่าจากประสบการณ์จริงของ Ness เสมอ
- ไม่ใช่อาจารย์สอน — เป็นเพื่อนที่ทำมาก่อนและแชร์ประสบการณ์

### Content Pillars
- 70% Finance & Investment: stocks, crypto, DCA, options, index funds, forex, BTC, tax
- 30% Lifestyle: work-life balance, money mindset, personal stories

### Tone Rules
- ภาษาไทย 100% ทุกครั้ง
- Casual, friendly เหมือนเพื่อนคุยกัน
- อธิบายซับซ้อนให้เป็นเรื่องง่าย
- แชร์ทั้งความสำเร็จและความผิดพลาด

### Post Structure — Single Image + Long-form Facebook Post (FORMAT หลัก)
```
⚠️ ยกเลิก Carousel แล้ว — ใช้ Single Image เท่านั้น (decision 20 มิ.ย. 2026)

1. Text บนรูป
   - หัวข้อหลัก (font ใหญ่ bold อ่านได้ตั้งแต่ scroll ผ่าน)
   - Sub text (ขยายความ 1 บรรทัด)
   - Branding: The Money Ness

2. Caption (Long-form)
   - Hook — เปิดด้วย personal story หรือ context สั้นๆ
   - เนื้อหาหลักแบบละเอียด หลาย paragraph
   - ตัวเลขจริงประกอบ
   - โยงกับชีวิต Sales Rep / มนุษย์เงินเดือน
   - Quiz 4 ข้อ (scenario จริง) ท้าย caption
   - CTA (save / comment)

3. Gemini Image Brief
   - ใช้ format มาตรฐาน (ดู style-guide.md หรือ Content Creation Workflow ด้านล่าง)
   - สัดส่วน 4:5 แนวตั้งเสมอ

⚠️ เพิ่ม 4 ก.ย. 2026: Caption ต้องมี 2 เวอร์ชันเสมอ — Facebook (ยาวเต็ม) + Instagram (ย่อ ≤2,200 ตัวอักษร) ดูรายละเอียดใน style-guide.md → Decisions Log
```

### Post Structure — Reels (60-90 วินาที)
```
0-3 วิ:   Hook ที่หยุดคนดูได้ (คำถามหรือ pain point)
3-15 วิ:  เล่าเรื่อง pain ของตัวเอง — relate กับคนดู
15-60 วิ: Solution จากประสบการณ์จริง + ตัวเลขจริง
60-90 วิ: บทเรียน + จบแบบ Loop ย้อนกลับ hook แรก
```

### Ness's Short Clip Style (จดจำทุกครั้ง)
```
✅ เล่าเป็นเรื่อง — ไม่ตัด jump cut เร็วๆ
✅ พูดทีเดียวรวดเดียว — เหมือนเล่าให้เพื่อนฟัง
✅ มีตัวเลขจริง + ผลลัพธ์จริง — ไม่ใช่แค่แนวคิด
✅ อารมณ์คือ hook แต่ value คือสิ่งที่คนเอาไปใช้ได้
✅ จบแบบ Loop — ให้คลิปวนซ้ำได้เนียน
❌ ห้ามเล่นแต่อารมณ์โดยไม่ให้ประโยชน์
```

### Post Structure — YouTube (10-15 นาที)
```
นาที 0-1:   Hook + preview สิ่งที่จะได้เรียน
นาที 1-3:   Story ของ Ness กับ topic นี้
นาที 3-12:  Main content 3-5 key points
นาที 12-14: Summary + takeaways
นาที 14-15: Subscribe + next video
```

### File Save Rules
```
Single Image posts → FINANCE-LEARNING/market-research/post-[topic].md
Reels scripts      → THE-MONEY-NESS/reels-scripts/reels-[topic].md
YouTube scripts    → THE-MONEY-NESS/youtube-scripts/yt-[topic].md
Published posts    → THE-MONEY-NESS/published/[date]-[topic].md

หมายเหตุ: post drafts บันทึกใน market-research/ เพราะ content มาจาก morning brief research
```

### Weekly Content Target
```
จันทร์: Finance Single Image + Long-form (FB + IG)
พุธ:    Finance/Lifestyle Single Image + Long-form (FB + IG)
ศุกร์:  Finance Single Image + Long-form (FB + IG)
เสาร์:  Reels (IG + FB + YouTube Shorts)
อาทิตย์: YouTube Long-form (ถ้ามี)

⚠️ ยกเลิก Carousel แล้ว — เหตุผล: ทำรูปเยอะ งานเยอะ แต่ value น้อยกว่า Single Image + Long-form caption
```

---

## 🟡 PROJECT 2 — IB FOREX PRIVATE

### ตัวตน
- เพจ educational forex สำหรับ IB referral program
- เน้น education ก่อน promotion เสมอ
- เป็น grey zone ในไทย — ต้องระมัดระวังทุกครั้ง

### ⚠️ HARD RULES — ห้ามละเมิดเด็ดขาด
```
❌ ห้ามรับประกันกำไรหรือรายได้ทุกกรณี
❌ ห้ามบอกว่า Forex ง่ายหรือไม่มีความเสี่ยง
❌ ห้าม mix content กับ The Money Ness
❌ ห้ามใช้ hype language หรือ income claims
✅ ต้องใส่ risk disclaimer ทุกโพสต์เสมอ
✅ เน้น education เสมอ ไม่ใช่ promotion
```

### Risk Disclaimer — ใส่ทุกโพสต์
```
⚠️ การเทรด Forex มีความเสี่ยงสูง
ผู้ลงทุนควรศึกษาข้อมูลให้ครบถ้วน
ก่อนตัดสินใจลงทุนทุกครั้ง
```

### Post Structure — Single Image + Long-form (IB Forex)
```
⚠️ ยกเลิก Carousel แล้ว — ใช้ Single Image เท่านั้น

1. Text บนรูป: หัวข้อ Forex + Sub text + Branding
2. Caption (Long-form):
   - Hook — คำถามหรือ fact เกี่ยวกับ Forex
   - อธิบาย concept ง่ายๆ จากประสบการณ์จริง Ness
   - ตัวอย่างจริงจากตลาด + ตัวเลขจริง
   - Risk management ที่ต้องรู้
   - ⚠️ Risk Disclaimer (ห้ามลืม) + CTA
3. Gemini Image Brief (format มาตรฐาน)
```

### File Save Rules
```
Forex drafts   → IB-FOREX/drafts/forex-[topic].md
Reels scripts  → IB-FOREX/drafts/reels-forex-[topic].md
Published      → IB-FOREX/published/[date]-forex-[topic].md
```

### Weekly Content Target
```
⚠️ ยกเลิก Carousel แล้ว (decision 20 มิ.ย. 2026)
อังคาร: Forex Educational Single Image + Long-form
พฤหัส: Forex Tutorial Reels
```

---

## 📚 PROJECT 3 — FINANCE LEARNING

### ตัวตน
- พื้นที่ส่วนตัวสำหรับ Ness เรียนรู้การเงินอย่างลึก
- output จาก project นี้ feed เข้า 2 projects อื่นผ่าน SHARED folder
- ไม่ใช่ content สำหรับโพสต์ — เป็นความรู้ส่วนตัว

### Topics ที่กำลังเรียน
```
- Options Trading (Greeks, strategies, risk management)
- Forex (technical analysis, risk/reward)
- BTC & Crypto (market cycles, on-chain analysis)
- Index Funds (S&P500, passive investing)
- Mutual Funds (evaluation, selection)
- Tax Planning (legal tax reduction in Thailand)
```

### Daily Orientation Format (อัปเดต มิ.ย. 2026 — แทน Morning Brief เดิม)

**ไม่ใช่ Finance Summary — เป็น "จัดทิศทางวัน" ให้ Ness**  
**เวลาอ่าน:** 2 นาที | **บันทึก 2 ที่:** market-research/ + SHARED/morning-brief-latest.md

```
STEP 0 — ก่อนเขียน: อ่าน ness-profile.md + weekly-topics.md + goal-framework.md

ELEMENT 1 — XAU/USD Context (สำหรับ EA)
  - Trending / Sideways / Volatile (เลือก 1)
  - ราคาปัจจุบัน + direction ล่าสุด
  - EA condition: Active / Caution / Pause

ELEMENT 2 — Topic วันนี้
  - หัวข้อ Content จาก weekly-topics.md (ถ้าวันนั้นเป็น Post day)
  - หัวข้อเรียน (Learning Topic) จาก weekly-topics.md (ถ้าวันนั้นเป็น Learn day)
  - 1 angle หรือ hook ที่น่าสนใจ

ELEMENT 3 — Reflective Question
  - 1 คำถาม ไม่ใช่ quiz — ให้คิดต่อ
  - เชื่อมกับ topic วันนั้น
```

**กฎสำคัญ:**
```
❌ ห้ามสร้าง topic เอง — ดูจาก weekly-topics.md เท่านั้น
❌ ห้าม Google Drive ก่อน — ดู SHARED/ ก่อนเสมอ
✅ orient ไม่ใช่ inform — 2 นาที อ่านจบ ไม่ใช่เรียนครบ
```

**Learning Brief (Full) — แยกจาก Daily Orientation**
- สร้างเมื่อ Ness ขอ "เรียนเรื่อง [topic]" หรือ "ทำ brief วันเรียน"
- บันทึก: FINANCE-LEARNING/market-research/brief-[date]-[topic].md
- เพิ่มใน Dashboard Brief Archive → แท็บ "📚 บทเรียน"
- ความยาว: 15-20 นาที อ่าน

### File Save Rules
```
Market research  → FINANCE-LEARNING/market-research/morning-brief-[date].md
                   SHARED/morning-brief-latest.md (overwrite ทุกวัน)
Study notes      → FINANCE-LEARNING/study-notes/[topic]-notes.md
Quiz results     → FINANCE-LEARNING/quiz-results/quiz-log.md
Content angles   → SHARED/content-angles.md (append ไม่ต้อง overwrite)
Weekly topics    → SHARED/weekly-topics.md (overwrite ทุกอาทิตย์)
```

---

## 🔄 DAILY WORKFLOW — Claude ทำตามนี้ทุกวัน

### เช้า (Auto — Scheduled Task)
```
[Finance Learning Project]
1. ค้นหาข่าวตลาดล่าสุด USA stocks, crypto, forex
2. สรุปเป็น morning brief
3. บันทึก FINANCE-LEARNING/market-research/morning-brief-[date].md
4. บันทึก SHARED/morning-brief-latest.md (overwrite)
5. เพิ่ม content angles ใน SHARED/content-angles.md
```

### เช้า (Manual — Ness เปิด Cowork)
```
[The Money Ness Project]
1. อ่าน SHARED/morning-brief-latest.md
2. เลือก content angle ที่ดีที่สุด
3. สร้าง Single Image + Long-form Caption + Gemini Brief
4. บันทึก FINANCE-LEARNING/market-research/post-[topic].md
5. อัพเดท SHARED/content-calendar.md
```

### กลางวัน (Manual — 10 นาที)
```
[The Money Ness Project]
1. อ่าน draft ที่สร้างตอนเช้า
2. สร้าง Canva design
3. บันทึก design link ใน SHARED/content-calendar.md
4. อัพเดท status เป็น ✅ Ready
```

---

## 📅 WEEKLY WORKFLOW — Claude ทำตามนี้ทุกสัปดาห์

### วันอาทิตย์ — Sunday Batch (60 นาที)
```
STEP 1 — Finance Learning (15 นาที)
- ค้นหา trending topics สัปดาห์หน้า
- บันทึก SHARED/weekly-topics.md
- อัพเดท SHARED/content-angles.md

STEP 2 — The Money Ness (20 นาที)
- อ่าน SHARED/weekly-topics.md
- Draft 3 Single Image posts (จันทร์/พุธ/ศุกร์)
- บันทึก FINANCE-LEARNING/market-research/post-[topic].md

STEP 3 — IB Forex (10 นาที)
- อ่าน SHARED/weekly-topics.md (ดู forex section)
- Draft 2 educational posts
- บันทึก IB-FOREX/drafts/forex-[topic].md

STEP 4 — Design All in Canva (10 นาที)
- Design ทุก draft ใน THE-MONEY-NESS/drafts/week-[date]/
- บันทึก design links ใน SHARED/content-calendar.md

STEP 5 — Finalize (5 นาที)
- อัพเดท SHARED/content-calendar.md ให้สมบูรณ์
- แจ้ง Ness ว่า content พร้อม post กี่ชิ้น
```

### วันจันทร์ถึงเสาร์ — Daily Routine
```
เช้า:     Morning Brief (Auto) → เลือก angle → Draft post (30 นาที)
กลางวัน: Design ใน Canva (10 นาที)
เย็น:     Review + approve (5 นาที)
```

### วันพุธ — IB Outreach Day (เพิ่มเติม)
```
+15 นาที เย็น:
1. เปิด SHARED/ib-milestone-tracker.md
2. เลือกคน 3 คนจาก Pipeline
3. ส่งข้อความส่วนตัว — แชร์ content ที่ทำสัปดาห์นี้เป็น opener
4. บันทึกผลใน Outreach Log
5. ถ้าคนสนใจ → นัดคุยต่อ ไม่ต้องรีบ pitch
```

---

## 🔗 CROSS-PROJECT RULES

### เมื่อ Finance Learning สร้างไฟล์
```
ถ้าสร้าง morning brief → บันทึก 2 ที่เสมอ:
  1. FINANCE-LEARNING/market-research/morning-brief-[date].md
  2. SHARED/morning-brief-latest.md (overwrite)

ถ้าสร้าง content angles → append ไม่ต้อง overwrite:
  SHARED/content-angles.md

ถ้าสร้าง weekly topics → overwrite:
  SHARED/weekly-topics.md
```

### เมื่อ The Money Ness อ่านจาก Shared
```
อ่าน SHARED/morning-brief-latest.md เพื่อ → สร้าง daily post
อ่าน SHARED/content-angles.md เพื่อ → เลือก topic
อ่าน SHARED/weekly-topics.md เพื่อ → วาง weekly plan
เขียน SHARED/content-calendar.md เพื่อ → track status
```

### เมื่อ IB Forex อ่านจาก Shared
```
อ่าน SHARED/morning-brief-latest.md (forex section เท่านั้น)
อ่าน SHARED/weekly-topics.md (forex topics เท่านั้น)
ห้ามอ่านหรือ copy content จาก The Money Ness ทุกกรณี
```

---

## 📋 CONTENT CALENDAR — Status System

```
⏳ Draft    = Claude กำลัง draft
✏️ Review   = รอ Ness review
🎨 Design   = รอ design ใน Canva
✅ Ready    = พร้อม post
📤 Posted   = โพสต์แล้ว
```

### อัพเดท Calendar ทุกครั้งที่
```
- สร้าง draft ใหม่ → เพิ่ม row ใหม่ status ⏳ Draft
- Design เสร็จ → อัพเดท status เป็น ✅ Ready + ใส่ Canva link
- โพสต์แล้ว → อัพเดท status เป็น 📤 Posted
```

### Archive Rule — ป้องกัน Calendar เน่า
```
- ต้นสัปดาห์ทุกอาทิตย์ → ลบ row ที่เกิน 14 วันและยังเป็น ⏳ Draft ออก
  (Draft ที่ค้างนานกว่า 2 สัปดาห์ = ไม่ได้ใช้แล้ว)
- เก็บไว้เฉพาะ row ของสัปดาห์นี้และสัปดาห์หน้าเท่านั้น
- ถ้า Draft เก่ายังดีอยู่ → ย้ายไป SHARED/idea-bank.md แทนลบทิ้ง
```

---

## 🚦 HOW TO IDENTIFY WHICH PROJECT

เมื่อ Ness ให้ task มา Claude ต้องระบุก่อนเสมอว่า task นี้อยู่ใน project ไหน:

```
ถ้า task เกี่ยวกับ: ข่าวตลาด, เรียนรู้, research
→ Finance Learning Project

ถ้า task เกี่ยวกับ: content มนุษย์เงินเดือน, carousel, reels, youtube
→ The Money Ness Project

ถ้า task เกี่ยวกับ: forex trading, broker, IB
→ IB Forex Private Project

ถ้า Ness ไม่ได้ระบุ project
→ Claude ถามก่อนเสมอ: "งานนี้อยู่ใน project ไหนครับ?"
```

---

## ✅ CHECKLIST ก่อนส่ง Output ทุกครั้ง

```
□ อ่าน about-me.md แล้ว
□ อ่าน SHARED/ness-profile.md แล้ว (ถ้างานเกี่ยวกับแผน/เป้าหมาย)
□ อ่าน MASTER-WORKFLOW.md แล้ว
□ Content เป็นภาษาไทย 100%
□ Tone casual และ friendly
□ บันทึกไฟล์ถูก folder
□ อัพเดท content-calendar.md แล้ว (ถ้าสร้าง content)
□ Fact-Check ผ่านแล้ว (ถ้า content มีตัวเลขภาษี/กฎหมาย/ราคาตลาด)
□ ไม่มีงาน IB Forex หรือ YouTube เว้นแต่ Ness จะบอกให้ทำ
□ Correct English ของ Ness ท้าย response (ถ้ามี)
```

---

---

## ✍️ Content Creation Workflow (กำหนด 16 มิ.ย. 2026)

หลังจาก Quiz ผ่าน (≥ 3/4) ให้ทำตามขั้นตอนนี้:

```
STEP 1 — เลือก Format (decision 20 มิ.ย. 2026 — ยกเลิก Carousel แล้ว)
  A) Single Image + Long-form Caption  → FORMAT หลักสำหรับทุกโพสต์
  B) Reels Script (60-90 วิ)           → สำหรับ Facebook/IG Reels
  C) YouTube Script                    → Long-form video
  ❌ Carousel — ยกเลิกแล้ว ห้ามใช้

STEP 2 — เลือก Hook (ให้ Ness เลือก)
  - เสนอ 3-4 แบบ แล้วให้ Ness เลือก
  - Hook ต้องจูงใจ สื่อถึงประโยชน์ที่ได้รับ
  - ไม่ใช่แค่บอก topic เช่น "วันนี้เรามาเรียน Covered Call"

STEP 3 — เขียน Content ตาม Format ที่เลือก
  Single Image + Caption:
    ── Caption (ต้องลึกและยาวพอ — อ่านแล้วได้ความรู้จริง) ──

    โครงสร้าง:
    1. Hook — ประโยคแรกหยุด scroll ทันที เปิดด้วยสิ่งที่คนไม่รู้หรือขัดกับความเชื่อเดิม
    2. Setup — เล่าจากประสบการณ์ Ness ("ผมนั่งคำนวณดู..." / "ผมเพิ่งรู้จัก...")
    3. อธิบาย Mechanism จริง — ต้องอธิบายว่า "มันทำงานยังไง" ไม่ใช่แค่บอกว่ามีอยู่
       - ใช้ analogy / เปรียบเทียบกับสิ่งใกล้ตัว (ร้านกาแฟ, บ้านเช่า ฯลฯ)
       - อธิบายทีละขั้น ให้คนที่ไม่รู้เรื่องเลยตามได้
    4. ตัวเลขจริงที่คำนวณได้ — แสดงผลกระทบเป็นตัวเลขชัดเจน
       - ทั้งผลระยะสั้น (ปีนั้น) และระยะยาว (20-30 ปี)
       - ตัวเลขต้องเป็น scenario ที่ใกล้เคียงชีวิตจริง (เงิน 500K-1M)
    5. Context — บอกว่าสำคัญยังไงในภาพรวม เชื่อมกับ concept อื่นถ้ามี
    6. ข้อควรระวัง / มุมที่คนมักเข้าใจผิด
    7. CTA — save / comment / share พร้อมบอกว่า save ไปทำอะไร

    ── Image Brief (ส่งให้ Gemini) ──
    ก๊อปปี้ฟอร์มด้านล่างนี้ เติมข้อมูลตาม Topic แล้วส่งให้ Ness ได้เลย

    Style หลัก: 3D Miniature, Cinematic Sci-fi, แสงมืดดุดันตัดแสงสว่างจ้า
    ฉากและวัตถุหลัก: เปลี่ยนตาม Topic ทุกครั้ง

    ══════════════════════════════════════════
    [ก๊อปปี้ข้อความด้านล่างนี้ ส่งให้ผมได้เลยครับ]

    📌 คำสั่งบังคับทางเทคนิค (Strict System Rules - ห้าม AI เปลี่ยนแปลงเด็ดขาด):
    สัดส่วนภาพ (Aspect Ratio): บังคับแนวตั้ง 4:5 เท่านั้น ห้ามปรับเป็นแนวนอน
    ข้อห้ามเด็ดขาด: ห้ามมีลายน้ำประกายดาว (No watermarks) และ ห้ามใส่เครื่องหมายคำพูด (") ในข้อความ
    โครงสร้างภาพ: พื้นที่ด้านบนเป็นภาพฉาก รอยต่อภาพด้านล่างต้องไล่เฉดสีเนียนกริบ (Smooth Gradient) กลืนลงมาเป็น "พื้นที่สีดำทึบ"
    เลย์เอาต์ข้อความ: จัดวางข้อความบนพื้นที่สีดำ ขยับตำแหน่งข้อความทั้งหมดให้สูงขึ้น (ไม่ให้อัดแน่นติดขอบล่าง) และเว้นพื้นที่ว่างใต้บรรทัดที่ 3 ประมาณหนึ่งสำหรับใส่โลโก้/เครดิตเพจ
    ขนาดฟอนต์: บรรทัดที่ 1 ต้อง "ใหญ่ที่สุด" / บรรทัดที่ 3 ต้องใหญ่และเด่นชัดรองลงมา / บรรทัดที่ 2 เป็นขนาดกลาง

    📝 ข้อมูลบรีฟคอนเทนต์ (Content Brief):

    ภาพที่ต้องการ (Image Prompt):

    [ใส่คำบรรยายฉากที่ต้องการ: เช่น ภาพ 3D โมเดลจิ๋ว (Miniature) แนว Cinematic โฟกัสที่... แสงและเงาโทน...]
    ข้อความภาษาไทย:

    บรรทัด 1: [ใส่ข้อความหลัก]

    บรรทัด 2: [ใส่ข้อความขยายความ]

    บรรทัด 3: [ใส่ข้อความสรุป หรือ Call to Action]
    การเน้นสีข้อความ (โทน Neon Growth):

    ตัวอักษรสีเขียวสะท้อนแสง (Neon Green): [ระบุคำที่ต้องการเน้นในบรรทัด 1]
    กรอบพื้นหลังสีส้มสว่าง (Vibrant Orange): [ระบุคำที่ต้องการเน้นในบรรทัด 3]
    ══════════════════════════════════════════

    ⚠️ Accuracy Rule:
    ตรวจข้อความทุกบรรทัดก่อน output — ห้าม claim ที่ misleading
    เช่น "ไม่ต้องรอ" ในกลยุทธ์ที่มี contract period

  ❌ Carousel — ยกเลิกแล้ว ห้ามใช้ (decision 20 มิ.ย. 2026)

STEP 4 — ส่ง Gemini Image Brief ให้ Ness
  ใช้ format มาตรฐานใน STEP 3 ด้านบน (📌 Strict System Rules)
  สัดส่วน 4:5 แนวตั้ง / Smooth Gradient / Neon Green บรรทัด 1 / Vibrant Orange บรรทัด 3

STEP 5 — Post + Warm Share
  - โพสต์บนเพจ
  - Share ส่วนตัวให้ warm leads 5-8 คน ทันทีหลังโพสต์
```

### Caption Quality Rules
```
✅ เขียนจากประสบการณ์ Ness เสมอ ("ผมนั่งคำนวณดู..." / "ผมเพิ่งรู้จัก...")
✅ อธิบาย Mechanism จริงว่า "ทำงานยังไง" — ไม่ใช่แค่บอกว่ามีอยู่
✅ ใช้ Analogy เปรียบเทียบกับสิ่งใกล้ตัว ให้คนไม่รู้เรื่องเลยตามได้
✅ ตัวเลขจริงทั้งระยะสั้นและระยะยาว (20-30 ปี) บน scenario ใกล้ชีวิตจริง
✅ ระบุข้อควรระวัง / มุมที่คนมักเข้าใจผิด
✅ ความยาวต้องพอให้อ่านแล้วได้ความรู้จริง — ไม่ใช่แค่ awareness
❌ ห้ามสรุปสั้นเกินไปจนไม่มี Mechanism หรือตัวเลข
❌ ห้ามใช้ภาษาเป็นทางการหรือศัพท์วิชาการโดดๆ โดยไม่อธิบาย
❌ ห้าม claim ที่ misleading — ตรวจ fact ทุกบรรทัดก่อน output
```

---

## 📣 Content Distribution Rule (กำหนด 16 มิ.ย. 2026)

ถาม 1 คำถาม: "post นี้พูดถึง Forex หรือ trading platform โดยตรงไหม?"
- ใช่ → No Graph Just Moo (TikTok)
- ไม่ใช่ → The Money Ness (Facebook/Instagram)

ข้อยกเว้น: Forex topic สามารถทำ 2 เพจพร้อมกัน — version ยาว Facebook, clip สั้น TikTok

---

## 🎯 Project Priority (อัปเดต มิ.ย. 2026 — Goal Framework v2.0)

**True Mission:** เงิน 10 ล้านบาท + อิสระ ภายใน 4-5 ปี ผ่าน 3 Projects

**3 Projects ที่กำลังทำ (ไม่เพิ่ม):**
1. 🔴 **Forex EA** — Critical Path: EA → Prop Firm → Income Bridge สำหรับ Canada
   - ตอนนี้: 50% เสร็จ (Optimization phase) | Blocker: MQL5 พื้นฐาน
   - เวลา: 1.5 ชม./วัน
2. 📱 **Content (The Money Ness)** — โตช้าแต่สม่ำเสมอ วินัยก่อน scale
   - เป้า: จ/พ/ศ post, อ/พฤ เรียน
   - เวลา: 1.5 ชม./วัน
3. 💰 **Portfolio 50/35/15** — ลงทุนทุกเดือน, ไม่ทิ้ง

**⚠️ ON HOLD (ไม่ทำจนกว่า Ness จะบอก):**
- IB Forex / เพจแยก
- YouTube

**Decision Filter สำหรับทุก task ใหม่:**
→ "สิ่งนี้ช่วยให้ EA เร็วขึ้น, Content แข็งแกร่งขึ้น, หรือพอร์ตโตขึ้นไหม?"
→ "Canada test: ถ้าไป Canada 2 ปี สิ่งนี้ยังทำงานได้ไหม?"

---

## ♻️ 1 Brief = 4 Content System (อัปเดต 18 มิ.ย. 2026)

Morning Brief แต่ละอัน → แปลงเป็น content ได้ 4 ชิ้นทันที:

```
Brief วันนี้
    ↓
① Single Image + Long-form Caption → The Money Ness (FB/IG) ← FORMAT หลัก
② Reel Script (60-90 วิ)           → The Money Ness (FB/IG) หรือ No Graph Just Moo (TikTok) ถ้าเกี่ยว Forex
③ YouTube Script                   → The Money Ness (YouTube) ถ้าหัวข้อลึกพอ
④ Quiz Post แยก                    → The Money Ness (engagement สูง)

❌ Carousel — ยกเลิกแล้ว (decision 20 มิ.ย. 2026)
```

เมื่อ Ness เลือก Format ให้ Claude ถามเสมอ: "อยากให้แปลงเป็น content อีก 3 แบบที่เหลือไหมครับ?"

---

## 📊 Content Performance Tracking

ทุกครั้งที่โพสต์ บันทึกใน SHARED/content-calendar.md:
- Reach (จำนวนคนเห็น)
- Engagement (Like/Comment/Share/Save)
- หมายเหตุ: "คนถาม IB", "มีคนแชร์ต่อ", "ยอดแย่" ฯลฯ

หลัง 2 สัปดาห์ → Claude สรุปว่า content แบบไหน work แล้วเน้นแบบนั้น

---


## 📁 SYSTEM FILES (อัปเดต มิ.ย. 2026)

```
SHARED/
├── dashboard.html              ← เปิดใน browser: EA progress, Portfolio, Learning Hub, Vocab, Brief Archive
│                                  Brief Archive มี 2 sub-tab: 🌅 Morning Brief | 📚 บทเรียน
│                                  คลิก card → เปิดไฟล์ใน browser tab ใหม่
├── fact-check-protocol.md     ← ⭐ ใช้ทุกครั้งก่อน publish — แบ่ง 🔴🟡🟢 ตามความเสี่ยง outdated
├── ness-profile.md             ← ตัวตน Ness + 8 rules ที่ Claude ต้องรู้ก่อนวางแผน
├── goal-framework.md          ← Goal Framework v2.0 — True Mission, 3 Phases, 50/35/15
├── action-plan.md             ← Daily 3hr, Weekly rotation, Monthly milestones, KPI
├── learning-curriculum.md     ← 3 Layers × 12 Episodes + Optional Topics Bank
└── morning-brief-latest.md    ← Daily Orientation ล่าสุด (overwrite ทุกวัน)

FINANCE-LEARNING/market-research/
├── morning-brief-[date].md    ← Daily Orientation archive
└── brief-[date]-[topic].md   ← Learning Brief เต็ม (15-20 นาที) archive
```

**Brief Archive — เพิ่มไฟล์ใหม่ต้องทำ (ครบทั้ง 3 ข้อ ไม่งั้นไม่ขึ้น dashboard เว็บ!):**
1. บันทึกไฟล์ใน FINANCE-LEARNING/market-research/
2. เพิ่ม entry ใน SHARED/dashboard.html (morningBriefs หรือ learningBriefs array)
3. **Sync ขึ้น GitHub** — dashboard เว็บจริงคือ https://nestapitchayut2-cloud.github.io/money-ness-dashboard/ (repo `nestapitchayut2-cloud/money-ness-dashboard`, token: `SYSTEM/github-token.txt`)
   - git clone repo → copy ไฟล์ .md ไป `content/morning/` (morning brief) หรือ `content/briefs/` (learning brief/lesson) หรือ `content/posts/` (post-/reel-)
   - เพิ่มชื่อไฟล์ใน `content/index.json`
   - เพิ่ม entry ใน array เดียวกันของ `index.html` (ไฟล์ dashboard เว็บใน repo)
   - git commit + push origin main

**📁 วิธีตัดสินว่าไฟล์ไหนต้อง Link เข้า Dashboard (เพิ่ม 26 ก.ค. 2569 — เจอไฟล์กำพร้าจาก "Deep Dive Session" ที่สร้างกลางแชท ไม่ผ่าน scheduled task แล้วไม่มีใคร link ให้):**
- กฎใช้ **ตามปลายทางไฟล์ ไม่ใช่ตามที่มาของคำขอ** — ไม่ว่าไฟล์จะเกิดจาก scheduled task, คำขอเจาะลึกกลางแชท, หรือ session ไหนก็ตาม ถ้าจบลงเป็นไฟล์ .md ใน `FINANCE-LEARNING/market-research/` หรือ `FINANCE-LEARNING/study-notes/` ต้องทำครบ 3 ข้อ Brief Archive เสมอ ไม่มีข้อยกเว้น "แค่ครั้งนี้"
- **ก่อนเขียนไฟล์ลง 2 โฟลเดอร์นี้ ให้ถามตัวเองก่อน:** "Ness จะต้องย้อนกลับมาเปิดอ่านไฟล์นี้อีกไหม (เช่น ใช้ทบทวน อ้างอิง หรือมีโอกาสถูกเอาไปออกข้อสอบ)" — ถ้าใช่ = ต้องเซฟไฟล์ + link ทันทีในรอบเดียวกัน ห้ามเซฟไฟล์แล้วปล่อยไว้ก่อน "เดี๋ยวค่อย link ทีหลัง"
- ถ้าคำตอบคือ "ไม่" (แค่ตอบคำถามในแชท อธิบายสั้นๆ ไม่ได้ตั้งใจให้เป็นบทเรียนถาวร) → ไม่ต้องสร้างไฟล์เลย ตอบในแชทพอ วิธีนี้ลดโอกาสไฟล์กำพร้าไปในตัว เพราะไม่มีไฟล์ก็ไม่มีอะไรให้ลืม link
- ถ้าตัดสินใจเองไม่ได้ว่าเนื้อหานี้ควรเก็บถาวรหรือแค่คุยผ่านไป → ถาม Ness ตรงๆ ก่อนเซฟไฟล์ ("อยากให้บันทึกเป็นบทเรียนเก็บไว้ใน Dashboard ด้วยไหม")
- ก่อนปิด task ใดๆ ที่มีการเขียนไฟล์ลง 2 โฟลเดอร์ข้างบน ให้เช็คว่าทำครบ 3 ข้อ Brief Archive แล้วหรือยัง — ถ้ายัง ถือว่า task ยังไม่เสร็จ

**🧹 กฎกันไฟล์ซ้ำ / ไฟล์ผิดที่ (เขียน 26 ก.ค. 2569 หลังล้างไฟล์ซ้ำ 50 ไฟล์ออกจากระบบ):**

1. **ห้ามก็อปไฟล์กฎหรือไฟล์ระบบไปไว้ 2 ที่ ไม่ว่าด้วยเหตุผลอะไร** — นี่คือ bug ที่ทำให้เกิดไฟล์บทเรียนกำพร้าเมื่อ มิ.ย. 2569: มีสคริปต์ mirror `MASTER-WORKFLOW.md` ไปที่ `SHARED/master-workflow.md` แล้วรันครั้งเดียว สำเนาค้างที่เวอร์ชันเก่าซึ่งกฎไม่ครบ session ที่อ่านสำเนาผิดตัวก็ทำตามกฎไม่ครบ → **มี MASTER-WORKFLOW.md ไฟล์เดียวที่ root เท่านั้น**
2. **ไฟล์ .md ทุกไฟล์มี "บ้าน" ได้ที่เดียว** ตาม File Save Rules — ถ้าเจอไฟล์เนื้อหาเดียวกันอยู่ 2 ที่ ให้เก็บตัวที่อยู่ในโฟลเดอร์ที่ถูกตามกฎ แล้วลบตัวที่เหลือ ไม่ใช่เก็บทั้งคู่
3. **ห้ามเซฟไฟล์เนื้อหาลง root ของ Claude Workspace** — root มีได้แค่ `MASTER-WORKFLOW.md`, `about-me.md`, `UPDATED-GLOBAL-INSTRUCTIONS.md` เท่านั้น (เคยมีไฟล์บทเรียน 4 ไฟล์หลุดมาอยู่ root แล้วไม่มีใคร link เข้า dashboard)
4. **การ์ดบน dashboard ต้องชี้ไปที่ "บ้าน" จริงของไฟล์** — ถ้า reels script อยู่ `THE-MONEY-NESS/reels-scripts/` ก็ให้ path ชี้ไปที่นั่น ห้ามก็อปไฟล์มาไว้ `market-research/` เพื่อให้ path สวย
5. **ก่อนสร้าง dashboard / server / script ระบบใหม่ ให้เช็คก่อนว่ามีของเดิมอยู่แล้วหรือยัง** — เคยมี dashboard 3 ตัวพร้อมกัน (`SHARED/dashboard.html`, repo `index.html`, `SYSTEM/dashboard.html`) จนแก้ผิดไฟล์ซ้ำๆ ตอนนี้เหลือ 2 ตัวที่หน้าที่ชัดเจน **ห้ามสร้างตัวที่ 3 ขึ้นมาอีก**
6. **ถ้าเจอไฟล์ 2 เวอร์ชันของวันเดียวกันที่เนื้อหาต่างกัน (ไม่ใช่ซ้ำ)** — อย่าเก็บทั้งคู่ในชื่อคล้ายกัน ให้ตรวจข้อเท็จจริงก่อนว่าตัวไหนถูก แล้ว (ก) เก็บตัวที่ถูกเป็น morning brief ของวันนั้น (ข) ถ้าตัวอีกตัวมีเนื้อหาเรียนที่ลึกกว่า ให้แยกออกเป็น Learning Brief ชื่อ `brief-[date]-[topic].md` พร้อมระบุจุดที่แก้ไว้ในไฟล์ — เกิดขึ้นจริงกับ brief 26 มิ.ย. ซึ่งเวอร์ชันยาวระบุวันผิดและคำนวณเดือนหลัง Halving ผิด
7. **ตรวจสุขภาพระบบทุกครั้งที่ทำ Weekly Report:** เทียบไฟล์ทั้งหมดใน `market-research/` กับ array บน dashboard ว่ามีไฟล์กำพร้าหรือการ์ดที่ชี้ไปไฟล์ที่ไม่มีอยู่หรือไม่

**🔑 ถ้า git push ล้มเหลว — เช็คก่อนว่าเป็น token หมดอายุ ไม่ใช่ path ผิด (เกิดขึ้นจริง 22 ก.ค. 2569):**
- Error message ที่บอกว่า token หมดอายุ/ใช้ไม่ได้: `remote: Invalid username or token. Password authentication is not supported for Git operations.`
- วิธีเช็ค: `git ls-remote https://x-access-token:$(cat SYSTEM/github-token.txt)@github.com/nestapitchayut2-cloud/money-ness-dashboard.git HEAD` — ถ้า**อ่านได้แต่ push ไม่ได้** = token ยังไม่หมดอายุสำหรับ read แต่หมด/ไม่มีสิทธิ์เขียนแล้ว (มักเป็นเพราะ token ตั้ง expiration ไว้)
- **ห้ามเดาว่าไฟล์ token หายหรืออยู่ผิดที่แล้วขอให้ Ness ย้ายไฟล์** — ไฟล์อยู่ที่ `SYSTEM/github-token.txt` เสมอ ถ้า path นี้อ่านไม่ได้ให้บอก error จริงตามที่เจอ อย่าแต่งคำแนะนำเอง
- ถ้า push ล้มเหลวจาก token จริง → แจ้ง Ness ตรงๆ ว่าต้องสร้าง GitHub token ใหม่จาก https://github.com/settings/tokens (classic, scope `repo`, แนะนำ No expiration) แล้ว paste ให้ใน chat เพื่อบันทึกทับไฟล์เดิม — Claude สร้าง token เองไม่ได้

**🚨 กฎเหล็ก Dashboard (เกิดเหตุ index.html พังมาแล้ว 2 ครั้ง — 9 และ 10 ก.ค. 2569):**
1. **ห้าม copy/เขียนทับ `index.html` ใน repo ด้วย `SHARED/dashboard.html` เด็ดขาด** — เป็นคนละไฟล์กัน: index.html = dashboard เว็บ (โหลด content จาก `content/` same-origin) / dashboard.html = ตัว local ถ้าเอามาทับกัน เว็บพังทันที
2. **ห้ามเขียนไฟล์ dashboard ทั้งไฟล์ (full rewrite)** — ไฟล์ใหญ่หลายแสนตัวอักษร การเขียนทั้งไฟล์เสี่ยงถูกตัดท้ายขาด (truncate) ให้ใช้ Edit แบบแทนที่ string เฉพาะจุดเท่านั้น
3. **ห้ามแก้ `CONTENT_BASE` ใน index.html กลับไปเป็น raw.githubusercontent** — ต้องเป็น `'content/'` (same-origin) เพราะ raw โดนบล็อกจากเน็ตบางเจ้าในไทย
4. หลังแก้ index.html ทุกครั้ง ตรวจก่อน push ว่า (ก) ไฟล์จบด้วย `</html>` (ข) JS ไม่มี syntax error
5. **ก่อนเพิ่มข้อมูลเข้า array ใดๆ ต้องอ่าน entry เดิมก่อนว่าใช้ชื่อ field อะไร ห้ามคิดชื่อ field เอง** (เกิดขึ้นจริง 26 ก.ค. 2569 — การ์ด Quiz #3 ขึ้น `NaN%` / `5/5/undefined ข้อ` / `X ไม่ผ่าน` เพราะเขียน `score:'5/5'`, `pass:true`, `qa:[{a,note}]` ทั้งที่ของจริงคือ `score:5, total:5, passed:true`, `qa:[{q,answered,explanation,correct}]`)
   - schema ที่ถูกของแต่ละ array (อัปเดต 26 ก.ค. 2569):
     - `quizData`: `{ topic, date, score:<number>, total:<number>, passed:<bool>, weak, qa:[{ q, answered, explanation, correct:<bool> }] }`
     - `morningBriefs` / `learningBriefs`: `{ label, day, topic, path }`
     - `pendingQuizzes`: `{ id, title, ready:<bool>, note, questions:[<string>] }`
   - **วิธีตรวจก่อน push:** รัน render function จริงด้วย node แล้วดูผลลัพธ์ ไม่ใช่แค่เช็ค syntax ผ่าน — syntax ถูกแต่ชื่อ field ผิดจะ push ผ่านและพังบนหน้าเว็บ
     ```
     node -e "const h=require('fs').readFileSync('index.html','utf8');
     eval(h.match(/const quizData = \[[\s\S]*?\n\];/)[0].replace('const','var'));
     quizData.forEach(q=>console.log(q.score+'/'+q.total, q.passed, q.qa.length, q.topic));"
     ```

**📅 Weekly Topics / Weekly Report บน dashboard:**
- Ness เปิดอ่านผ่านปุ่มในแท็บ "📅 สัปดาห์นี้" ของ dashboard เว็บ — ไฟล์จริงอยู่ `SHARED/weekly-topics.md` + `SHARED/weekly-report-latest.md`
- **ทุกครั้งที่อัปเดต 2 ไฟล์นี้ ต้อง copy ขึ้น repo `content/briefs/` + push ด้วย** ไม่งั้นปุ่มบนเว็บจะเปิดได้แต่ฉบับเก่า

**💡 Ideas Hub (แท็บบน dashboard) — กติกาดูแล:**
- Source of truth: `SHARED/idea-bank.md` + array `const ideaBank = [` ใน SHARED/dashboard.html และ repo index.html (ต้องแก้คู่กันเสมอ + push)
- Ness เก็บไอเดียผ่านกล่อง Idea Inbox บนเว็บ → กด Copy มาส่งใน chat → Claude ใส่หมวด (หุ้น/BTC/Forex/กองทุน/Tax/Tech/Mindset) + เพิ่มเข้า idea-bank.md และ ideaBank array (num รันต่อ เช่น 004, 005) + push
- อัปเดตสถานะเมื่อถึงจังหวะ: เรียนจบ → `status:'learned'` / content เสร็จ → `status:'done'` (ทั้ง 2 ไฟล์ + mark ใน idea-bank.md)

*MASTER-WORKFLOW.md — Version 2.0*
*อัปเดต: มิ.ย. 2026 | การเปลี่ยนแปลง v2.0: Goal Framework v2.0, Daily Orientation, Fact-Check Protocol, Dashboard Learning Hub, IB/YouTube ON HOLD*
