# 👤 Mai Danh

> **Contact:** Telegram (@maihoangdanh)
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

**Chủ đề:** Conversations + second brain workflow + hội thoại group

**Nội dung đang diễn ra:**
- Mai Danh phát hiện tao chưa ghi cuộc hội thoại hiện tại vào file Conversations
- Tao đã rename file từ `Hermes Agent.md` → `Mai Danh.md` theo đúng rule: file đặt theo tên người tham gia, không phải tên Hermes
- Thống nhất rule: trước khi trả lời ai → đọc file hội thoại của họ trước để hiểu context
- Sau khi reply → cập nhật file + commit + push
- Luồng: xảy ra chuyện gì → ghi vào Conversations → commit + push → sync về máy

**2026-05-28 20:00 UTC+7:** Tạo file Christine Ngoc Dam.md, tạo thư mục Groups/Lộn xộn.md
- Ghi lại toàn bộ lịch sử hội thoại từ 22/5 → 28/5 trong group "Lộn xộn"
- Mai Danh & Christine Ngoc Dam (Judy) đã hỏi nhiều thứ: marketing nha khoa, sức khoẻ, matcha
- Tao xác nhận group chat_id -5276641968
- Bot @MucThienTonBot trả lời khi được tag

**2026-05-28 19:30 UTC+7:**
- Mai Danh: "ok chưa hỉ" → tao kiểm tra thấy lỗi provider auth failed
- Mai Danh: "ok làm đi xong thì báo tao" → tao làm các file hội thoại

**Kết luận:**
- File hội thoại là nguồn context dài hạn cho Hermes
- Workflow: đọc → trả lời → ghi → push
- Hội thoại trong group: ghi vào cả file cá nhân + file group
