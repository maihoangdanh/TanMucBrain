# 🤖 Hermes Agent

> **Contact:** Telegram DM (@maihoangdanh)
> **Vault:** Tan Mực Brain

---

## 2026-05-28 — Thiết lập bộ não thứ hai

**Chủ đề:** Setup Obsidian vault trên AWS + kết nối Hermes

**Nội dung chính:**
- Cấu hình Hermes: model=md-gpt, provider=custom, base_url=http://34.142.235.166:20128/v1
- Khởi tạo Tan Mực Brain vault theo cấu trúc PARA
- Kết nối GitHub repo maihoangdanh/TanMucBrain (git-based sync)
- Giải thích Daily Notes và Inbox

**Kết luận:**
- Git + GH PAT đã setup xong
- Hermes đọc/ghi vault được
- Mở thêm thư mục Conversations

---

## 2026-05-28 — Provider auth failed

**Chủ đề:** Lỗi gateway "Unknown provider 'md-gpt'"

**Nội dung chính:**
- config.yaml: model.default=md-gpt, provider=custom, base_url=34.142.235.166:20128
- Gateway có bug: đôi lúc resolve 'md-gpt' thành provider name thay vì model
- Runtime resolve ra custom endpoint vẫn chạy được

**Kết luận:**
- Config đúng, lỗi ở phía gateway override
- Tạm thời Hermes vẫn hoạt động
