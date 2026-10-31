# AI Cooking Master Video — Video Nấu Ăn ASMR 1 Chảo (KKHome AI)

> Phiên bản: v1.0 — 31/10/2026 — bản đầu tiên, đã kiểm chứng qua dự án thật "Bánh Nutella Nhân Chảy 1 Chảo" (10 cảnh, phim 95.5 giây, 1080x1920, có poster + gói SEO, giao qua Google Drive).
> SKILL này = Master Prompt **ChefVision AI** (5 phase) + lớp **lời dẫn tiếng Việt** của KKHome AI, đặt trên nền **Workflow Phim Khải Kiều v3.2**. Ưu tiên số 1: **độ liền mạch của thước phim**.

## SKILL này dùng khi nào

Khi người dùng muốn làm video nấu ăn/bánh kiểu ASMR siêu thực, quay top-down hoặc 45°, dọc 9:16 cho TikTok / Reels / Shorts / YouTube, nấu gọn trong **1 chảo hoặc 1 nồi**, và **bắt buộc có lời dẫn bằng tiếng Việt** (không làm ASMR câm).

## Đầu vào — hỏi gọn 3 thứ

1. **Món ăn** — người dùng tự chọn, hoặc để SKILL gợi ý 5 món ở Phase 1 rồi người dùng chốt 1.
2. **Giọng dẫn** — chọn 1 trong 3 (xem `references/02-loi-dan-voice-dna.md`). Mặc định nếu không chọn: *Giọng nữ vui tươi, năng lượng TikTok*.
3. **Số cảnh** — 8–12 cảnh, mặc định 10. (Tên kênh/series nếu có, dùng cho SEO.)

Sau đó chạy theo **5 phase có chốt duyệt** — hết mỗi phase phải hỏi duyệt, không tự nhảy phase (trừ khi người dùng dặn làm một lèo).

## Quy trình 5 phase + 2B

### Phase 1 — Gợi ý & chọn món
- Đề xuất **5 món** có tiềm năng viral: nấu gọn 1 chảo, tiếng ASMR đã tai, có cú *reveal* ở cuối (cắt ra chảy nhân, kéo sợi, mặt vàng giòn...).
- Mỗi món kèm 1 câu lời dẫn mở mẫu để người dùng cảm được giọng.
- Người dùng chốt 1 món mới đi tiếp.

### Phase 2 — Chia cảnh (storyboard)
- Chia món thành **8–12 cảnh theo đúng trình tự nấu thật**, mỗi cảnh 10 giây: chuẩn bị chảo → cho nguyên liệu khô → nguyên liệu ướt → khuấy/trộn → giấu nhân/topping → vào lò hoặc nấu → reveal ra lò → cắt miếng đầu → thìa hero + CTA.
- Mỗi cảnh ghi: số cảnh, mốc thời gian, hành động hình ảnh, chi tiết cảm giác (độ sánh, màu, kết cấu), âm thanh ASMR chính.
- Thời lượng phim ráp = N×10 − (N−1)×0.5 giây (crossfade 0.5s).

### Phase 2B — Kịch bản lời dẫn tiếng Việt (lớp KKHome AI thêm vào)
- Mỗi cảnh 10 giây = **3 beats**: Beat 1 lời dẫn mở (8–12 từ) → Beat 2 **ASMR thuần, KHÔNG giọng** (để tiếng nấu tỏa sáng) → Beat 3 lời dẫn chốt (≤10 từ, gieo tò mò sang cảnh sau).
- Khóa **1 Voice DNA duy nhất** cho người dẫn, lặp nguyên văn ở mọi prompt (xem references/02).
- Lời dẫn viết như rủ bạn ăn cùng: ngắn, hào hứng ở từ khóa vị giác, không đọc công thức khô khan.

### Phase 3 — Prompt ảnh từng cảnh (JSON)
- Mỗi cảnh **1 block JSON riêng**, đúng cấu trúc ở references/01. Khung 9:16.
- Mọi prompt đều nhúng **Visual DNA Lock**: cùng 1 chảo/nồi, cùng đôi tay (tay nữ trẻ, móng tự nhiên không sơn), cùng bàn gỗ sồi tối, cùng ánh sáng sáng ấm, style siêu thực UGC. Xem references/03.

### Phase 4 — Prompt video chuyển động (JSON + lời dẫn)
- Mỗi cảnh **1 block JSON riêng**: cấu trúc gốc của ChefVision **cộng thêm** 4 trường `narration_vi` (beat_1 / beat_2 = "NO VOICE - pure ASMR only" / beat_3), `voice_dna`, `asmr_sound`, `narration_timing` (Beat 1: 0–3.5s, Beat 2: 3.5–7s, Beat 3: 7–9.5s, 0.5s lặng cuối).
- Nhấn vật lý thật: độ sánh, trọng lực, sức căng bề mặt; cấm bay lơ lửng, cấm morphing, cấm méo tay.
- **Cảnh cuối:** trong **3 giây cuối**, cho hiện icon CTA bằng **chất liệu của món/kịch bản** (ví dụ dải Nutella chảy, hơi nóng): một hình **ngón tay cái** và một hình **chuông**, mô tả **chỉ bằng hình dáng** — TUYỆT ĐỐI không viết các từ chỉ tên nút trong prompt, không để hiện chữ hay nút bấm. Và **không bao giờ cho phụ đề/chữ lên video** ở bất kỳ cảnh nào.

### Phase 5 — SEO + thumbnail
- Theo Master Prompt gốc: 3 tiêu đề viral, mô tả + hashtag, 10–15 tags/keywords, prompt thumbnail **16:9** dạng JSON.
- Khi đăng YouTube theo chuẩn KKHome AI, làm lại SEO bằng **File 03** và Poster bằng **File 02** (xem references/04).

## Sản xuất (sau khi duyệt hết 5 phase)

1. **Poster** theo File 02 Poster Engine: 1 code block prompt duy nhất (Single Reference Lock, 3 lớp, Artifact Anchor macro, Title Event bằng chất liệu món, 3–7 từ, 9:16) + tối đa 3–5 dòng "Lời dặn dò". Render thử 1 bản nếu công cụ cho phép.
2. **SEO** theo File 03 Revenue Engine: đúng 5 khối theo thứ tự (3 tiêu đề mobile high-CTR — hook trong 65 ký tự đầu, tối đa 1–2 hashtag · mô tả đa tầng tự nhiên + timeline mồi tò mò + thông báo minh bạch AI + bản tiếng Anh rút gọn · pinned comment kích thuật toán · bộ tag 1 dòng · tên file gốc chuẩn algo).
3. **Render video** trực tiếp bằng công cụ media của Muse: tối đa **6 video mỗi lượt tin nhắn**; nhiều hơn thì chia lượt và nói rõ còn bao nhiêu cảnh. Dán Visual DNA Lock + Voice DNA + lời dẫn vào prompt của TỪNG cảnh.
4. **Upscale** từng cảnh 720x1280 → 1080x1920 bằng ffmpeg (scale lanczos, crf 18, aac 192k).
5. **Ráp phim** bằng xfade/acrossfade 0.5s (offset điểm nối thứ j = j×9.5s), kiểm tra thời lượng đúng công thức ở Phase 2.
6. **QC bắt buộc** trước khi giao (checklist ở references/03): ffprobe từng cảnh đúng 10.0s; frame mở đầu (hook); frame cao trào (cắt/reveal); frame 3 giây cuối (CTA bằng chất liệu, **không có chữ**); không phụ đề ở mọi frame.
7. **Giao phim:** upload **bản gốc** lên Google Drive và gửi link tải (kèm bản preview nhẹ 540x960 nếu cần xem nhanh trong chat). Lưu ý trung thực: trợ lý không nghe được audio mình tạo — nhắc người dùng tự nghe kiểm giọng dẫn tiếng Việt trước khi đăng.

## Lỗi thường gặp & cách xử lý

- **Cảnh bị lệch DNA** (đổi chảo, đổi tay, lọt người dẫn, đổi màu món): render lại **chỉ cảnh đó** với Visual DNA Lock viết mạnh hơn, không render lại cả phim; báo rõ cho người dùng cảnh nào đã thay.
- **CTA hiện thành chữ/nút bấm:** do prompt lỡ chứa tên nút — sửa prompt chỉ mô tả hình dáng + chất liệu rồi render lại cảnh cuối.
- **Lời dẫn đè tiếng ASMR:** giữ đúng nhịp 3 beats, Beat 2 luôn im lặng tuyệt đối.
- **Quá 6 cảnh/lượt:** dừng đúng 6, báo còn lại bao nhiêu, chờ người dùng nhắn tiếp rồi làm nốt — không hứa hẹn lấp lửng.
