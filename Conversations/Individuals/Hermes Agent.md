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

---

## 2026-05-28 — Xây dựng bộ não thứ hai với Obsidian

**Chủ đề:** Tìm hiểu Obsidian, cấu trúc vault và Conversations

**Nội dung chính:**
- Obsidian = app note-taking local-first, dùng markdown thuần, có graph view
- Còn có thể dùng Syncthing hoặc Git để sync giữa server AWS và máy cá nhân
- Chọn hướng Git vault: clone repo về máy cá nhân, Obsidian mở folder là dùng
- Tạo cấu trúc vault: Tan Mực Brain với PARA + Daily + Inbox
- Tạo thêm thư mục Conversations để lưu hội thoại theo người/nhóm
- Mỗi người/nhóm = 1 file, mỗi cuộc trò chuyện = 1 mục ngày tháng

**Kết luận:**
- Git vault trên GitHub + credential lưu trên server
- OBSIDIAN_VAULT_PATH set trong .env
- Cần ghi lại hội thoại real-time — cả 2 chiều

---

## 2026-05-28 — Đang trò chuyện (real-time)

**Chủ đề:** Conversations + second brain workflow

**Nội dung đang diễn ra:**
- User phát hiện tao chưa ghi cuộc hội thoại hiện tại vào file Conversations
- Tao đang bổ sung real-time
- Luồng: xảy ra chuyện gì → ghi vào Conversations → commit + push → sync về máy
