# Ask Why — BA Elicitation Skill · BA Zone

> A Claude AI skill that turns vague feature requests into structured business
> requirements — by asking the right questions before anyone writes a single
> line of spec.
>
> Developed by **Phúc NT** · Founder, BA Zone · [bazone.org](https://bazone.org)
> *For the Digital School BA/PO practitioner community — Vietnam & Southeast Asia*

[![Claude Skill](https://img.shields.io/badge/Claude-Skill-orange)](https://claude.ai)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)
[![Author](https://img.shields.io/badge/Author-Ph%C3%BAc%20NT-purple)](#)
[![BA Zone](https://img.shields.io/badge/BA-Zone-orange)](https://bazone.org)
[![BABOK](https://img.shields.io/badge/Framework-BABOK%20v3-green)](#)
[![Method](https://img.shields.io/badge/Method-5--Whys%20%2B%20Cockburn-blue)](#)

---

## 🌐 Language / Ngôn ngữ

- [🇬🇧 English](#english-version)
- [🇻🇳 Tiếng Việt](#phiên-bản-tiếng-việt)

---

<a name="english-version"></a>
## 🇬🇧 English Version

### The problem this skill solves

Most BA mistakes happen **before** any document is written:

- Accepting "we need an AI feature" as a requirement
- Jumping to Functional Requirements without confirming Business Requirements
- Asking generic textbook questions that don't surface real gaps
- Producing a spec for the wrong problem

**Ask Why** enforces the discipline of discovery-first elicitation. It won't let you skip to solutioning.

> *"The most expensive mistake in BA work is building the right solution to the wrong problem."* — Phúc NT, BA Zone

---

### What the skill does

1. **Detects intent** — classifies every request into 10 types, flags Solution Bias immediately
2. **Maps requirement layers** — shows which of the 5 BABOK layers are filled, partial, or empty
3. **Detects gaps** — produces a Known / Unknown table before asking anything
4. **Asks strategic questions** — max 3-5 per turn, always contextualised, never generic
5. **Extracts insights** — paraphrases back, classifies (symptom vs root cause vs constraint), updates findings
6. **Scans edge cases** — failure modes, fraud risk, RBAC, audit, compliance
7. **Produces structured summary** — 13-field output ready for BRD/PRD/UC writer

---

### The 7-step workflow

```
1. Intent Detection          → classify, flag Solution Bias
2. Requirement Layer Check   → show 5-layer status table
3. Gap Detection             → Known / Unknown table
4. Ask Why Questions         → 3-5 contextual, prioritised
5. Business Insight Extract  → paraphrase, classify, update
6. Edge Case Scan            → failure modes, fraud, compliance
7. Structured Summary        → 13-field output when stop condition met
```

---

### Installation

#### Option 1: Claude Project Knowledge (recommended)

1. Download or clone this repo
2. In [claude.ai](https://claude.ai) → **Projects → Create new project**
3. Upload the entire a-zone-ask-why/ folder to project knowledge
4. Start chatting — skill activates automatically on relevant inputs

#### Option 2: Paste SKILL.md as system prompt

Copy SKILL.md content into the system prompt of your Claude API call or custom GPT configuration.

#### Option 3: /mnt/skills/user/ (skill-runner environments)

Copy the folder to /mnt/skills/user/ba-zone-ask-why/.

---

### What this skill does NOT do

- ❌ Write BRD/SRS/PRD (use a doc-writer skill after discovery)
- ❌ Draw diagrams or UML
- ❌ Write test cases or acceptance criteria
- ❌ Accept a named solution as a confirmed requirement

---

### Domain coverage

The question-library.json includes starter question sets for:

| Domain | Examples in Digital School context |
|---|---|
| EdTech platform | Completion rate, learner journey, drop-off |
| Digital School enrollment | Funnel conversion, payment friction |
| Mentor matching | Booking, availability, satisfaction |
| Loyalty / retention | Churn, engagement, rewards |
| Reporting | Dashboard vs export, decision-driven data |
| Payment | Failure, retry, reconciliation, refund |
| AI features | Problem validation, data availability, fallback |
| Integration | Real-time vs batch, fallback, auth |

---

### Attribution

Developed by **Phúc NT** · Founder, [BA Zone](https://bazone.org) · Digital School

This is intellectual property of **BA Zone**. Free to use and fork under MIT License, provided you **keep the author attribution** in all distributed copies.

> Note: The full question-sequencing methodology, advanced follow-up logic, and live elicitation practice are taught in the **Digital School BA Advanced** program at [bazone.org](https://bazone.org).

---

### License

MIT — see [LICENSE](LICENSE). Attribution required on redistribution.

---

---

<a name="phiên-bản-tiếng-việt"></a>
## 🇻🇳 Phiên bản Tiếng Việt

> Bộ skill Claude AI hỗ trợ làm rõ những yêu cầu mơ hồ thành yêu cầu nghiệp vụ có cấu trúc —
> bằng cách đặt đúng câu hỏi trước khi viết bất kỳ dòng spec nào.
>
> Phát triển bởi **Phúc NT** · Founder, BA Zone · [bazone.org](https://bazone.org)
> *Dành cho cộng đồng BA/PO, đây là sản phẩm cá nhân cho cộng đồng BA Zone không liên quan đến cá nhân hoặc tổ chức nào khác, các ví dụ không liên quan đến sản phẩm thực tế nào trên thị trường để đảm bảo tuân thủ bảo mật và bản quyền*

---

### Bộ Skill này giúp gì cho BA, PO, PM

Một sai lầm thường gặp của BA, PO khi phân tích nghiệp vụ đó là:
- Chấp nhận "chúng tôi cần tính năng AI" như một yêu cầu thực sự và đi vào phân tích luôn mà không đặt câu hỏi tại sao.
- Nhảy thẳng vào Yêu cầu Chức năng mà không xác nhận Yêu cầu Nghiệp vụ khi chưa hiểu được tần yêu cầu kinh doanh (Business Requirement) hay Yêu cầu bên liên quan (Stakeholder requirement)
- Đặt các câu hỏi chung chung, không khai thác được khoảng các yêu cầu hoặc rủi ro tiềm ẩn của dự án.
- Tạo ra spec đúng cho một vấn đề sai, tức là giải pháp không đáp ứng được yêu cầu người dùng.

**Ask Why - Product discovery** đề cao kỷ luật elicitation theo hướng khám phá trước theo framework của Babok v3 chuẩn quốc tế IIBA.Skill không cho phép bạn bỏ qua bước này để đi thẳng vào giải pháp khi chưa làm rõ yêu cầu.

> *"Sai lầm tốn kém nhất trong công việc BA, PO là xây dựng đúng giải pháp cho một vấn đề sai."* — Phúc NT, Founder BA Zone

### Skill này giúp BA, PO làm gì

1. **Phát hiện ý định** — phân loại mọi yêu cầu thành 10 loại, gắn cờ Solution Bias ngay lập tức
2. **Ánh xạ các lớp yêu cầu** — hiển thị 5 lớp BABOK nào đã đủ, còn thiếu, hoặc trống
3. **Phát hiện khoảng trống** — tạo bảng Known / Unknown trước khi đặt bất kỳ câu hỏi nào
4. **Đặt câu hỏi chiến lược** — tối đa 3-5 câu mỗi lượt, luôn theo ngữ cảnh, không bao giờ chung chung
5. **Trích xuất insight** — diễn giải lại, phân loại (triệu chứng vs nguyên nhân gốc rễ vs ràng buộc), cập nhật phát hiện
6. **Quét edge cases** — failure modes, rủi ro gian lận, RBAC, audit, compliance
7. **Tạo tóm tắt có cấu trúc** — output 13 trường sẵn sàng cho BRD/PRD/UC writer

---

### Quy trình 7 bước

```
1. Phát hiện ý định          → phân loại, gắn cờ Solution Bias
2. Kiểm tra lớp yêu cầu     → hiển thị bảng trạng thái 5 lớp
3. Phát hiện khoảng trống   → bảng Known / Unknown
4. Câu hỏi Ask Why           → 3-5 câu theo ngữ cảnh, ưu tiên hóa
5. Trích xuất insight        → diễn giải lại, phân loại, cập nhật
6. Quét edge case            → failure modes, gian lận, compliance
7. Tóm tắt có cấu trúc      → output 13 trường khi điều kiện dừng được đáp ứng
```

---

### Cài đặt

#### Tùy chọn 1: Claude Project Knowledge (khuyến nghị)

1. Tải về hoặc clone repo này
2. Vào [claude.ai](https://claude.ai) → **Projects → Tạo project mới**
3. Upload toàn bộ thư mục a-zone-ask-why/ vào project knowledge
4. Bắt đầu chat — skill tự động kích hoạt khi có đầu vào phù hợp

#### Tùy chọn 2: Dán SKILL.md làm system prompt

Copy nội dung SKILL.md vào system prompt trong Claude API call hoặc cấu hình custom GPT của bạn.

#### Tùy chọn 3: /mnt/skills/user/ (môi trường skill-runner)

Copy thư mục vào /mnt/skills/user/ba-zone-ask-why/.

---

### Skill này KHÔNG làm gì

- ❌ Viết BRD/SRS/PRD (dùng skill doc-writer sau bước discovery)
- ❌ Vẽ biểu đồ hay UML
- ❌ Viết test case hay acceptance criteria
- ❌ Chấp nhận tên giải pháp đã đặt sẵn như một yêu cầu đã xác nhận

---

### Phạm vi domain

`question-library.json` bao gồm bộ câu hỏi khởi đầu cho:

| Domain | Ví dụ trong bối cảnh Digital School |
|---|---|
| Nền tảng EdTech | Tỷ lệ hoàn thành, hành trình học viên, drop-off |
| Tuyển sinh Digital School | Chuyển đổi funnel, ma sát thanh toán |
| Kết nối Mentor | Đặt lịch, thời gian rảnh, sự hài lòng |
| Loyalty / giữ chân | Churn, tương tác, phần thưởng |
| Báo cáo | Dashboard vs xuất dữ liệu, dữ liệu hỗ trợ quyết định |
| Thanh toán | Lỗi, thử lại, đối soát, hoàn tiền |
| Tính năng AI | Xác nhận vấn đề, tính sẵn có của dữ liệu, fallback |
| Tích hợp | Real-time vs batch, fallback, xác thực |

---
### Hướng dẫn Prompt
Bạn hãy prompt đơn giản theo cấu trúc:
[Bối cảnh] Hệ thống/sản phẩm: ___ | Lĩnh vực: ___
[Người phát biểu] Vai trò: ___
[Yêu cầu gốc - nguyên văn] "___"
[Hiện trạng as-is] ___
[Họ nghĩ vấn đề là] ___        ← đây là giả định để challenge
[Ràng buộc đã biết] Pháp lý/deadline/hệ thống: ___
Sau đó kích hoạt skill Product discovery. Không viết mô tả yêu cầu ngay. Bắt đầu bằng việc xác định intent, layer còn thiếu, và hỏi tối đa 3 câu why ưu tiên cao nhất để phát triển sản phẩm.
Đừng nên quá chi tiết vì sẽ giới hạn sự sáng tạo nếu có.

### Bản quyền
Phát triển bởi **Phúc NT** · Founder, [BA Zone](https://bazone.org) ·
Đây là tài sản trí tuệ của **BA Zone**. Tự do sử dụng và fork theo giấy phép MIT, với điều kiện bạn **giữ nguyên thông tin tác giả** trong tất cả bản phân phối. 
Cần hỗ trợ các bạn hãy nhắn tin vào fanpage BA Zone để được tư vấn.
> Lưu ý: Skill này nếu được phối lại không đúng tiêu chuẩn sẽ có chất lượng đầu ra kém. Phương pháp luận xếp chuỗi câu hỏi đầy đủ, logic follow-up nâng cao, và luyện tập elicitation trực tiếp được dạy trong chương trình **AI for BA** tại [bazone.org](https://digitalschool.vn/courses/ai-cho-businss-analyst-va-product-owner/).

---
Nếu thấy repo này hữu ích, nhờ anh em đăng nhập và tặng mình 1 ngôi sao và forks về trang github của các bạn nhé.
### Giấy phép

MIT — xem [LICENSE](LICENSE). Yêu cầu ghi rõ tác giả khi phân phối lại.

---
*BA Zone — Cộng đồng BA/PO Việt Nam từ 2017*
*by Phúc NT · bazone.org*
