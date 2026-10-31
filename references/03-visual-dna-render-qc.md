# References 03 — Visual DNA Lock, Render, Ráp phim & QC

## Visual DNA Lock (thay cho Character DNA Lock ở dạng phim không nhân vật)
Khóa 4 yếu tố, viết giống hệt nhau trong mọi prompt ảnh/video của dự án:
- **Chảo/nồi:** một chiếc duy nhất (ví dụ: chảo gang đen) — không đổi kiểu, đổi màu giữa chừng.
- **Đôi tay:** cùng một đôi tay (mặc định: tay nữ trẻ, móng ngắn tự nhiên, không sơn).
- **Bàn & nền:** bàn gỗ sồi tối mộc mạc.
- **Ánh sáng:** ánh sáng studio buổi sáng ấm.
Câu khóa mẫu (tiếng Anh, dán vào prompt render): `VISUAL DNA LOCK: same black cast-iron skillet, same young woman's hands with natural short unpolished nails, rustic dark oak wooden table, warm morning studio lighting, continuous smooth motion, never a cut, no morphing, no floating objects, no distorted hands, no text overlay, no subtitles.`

## Render
- Render trực tiếp bằng công cụ media của Muse (ảnh trước nếu cần keyframe, rồi video image-to-video hoặc text-to-video theo prompt Phase 4).
- **Tối đa 6 video mỗi lượt tin nhắn.** Dự án 8–12 cảnh thì chia lượt: làm 6, báo rõ còn mấy cảnh, chờ người dùng nhắn tiếp.
- Prompt render mỗi cảnh phải chứa: hành động của cảnh + Visual DNA Lock + Voice DNA + 2 câu lời dẫn kèm mốc thời gian + "Beat 2 pure ASMR, no voice" + cấm chữ/phụ đề.

## Upscale & ráp (chuẩn Workflow v3.2)
- Upscale từng cảnh: `ffmpeg -i scene.mp4 -vf "scale=1080:1920:flags=lanczos" -c:v libx264 -preset medium -crf 18 -c:a aac -b:a 192k scene_1080.mp4`
- Ráp bằng **xfade (video) + acrossfade (audio), duration 0.5s**; offset của điểm nối thứ j = **j × 9.5s** (9.5, 19, 28.5, ...).
- Thời lượng phim cuối phải bằng **N×10 − (N−1)×0.5** giây (ví dụ 10 cảnh = 95.5s). Lệch là ráp sai, làm lại.

## CTA 3 giây cuối (luật KKHome AI — bắt buộc từ 31/10/2026)
- Ở **phân cảnh cuối**, trong **3 giây kết thúc**: hiện 2 icon CTA được **cách điệu bằng chất liệu của kịch bản/món ăn** (dải socola chảy, hơi nóng, bột bánh... tùy tập).
- Icon 1: hình **ngón tay cái** (ý nghĩa: thích). Icon 2: hình **chuông** (ý nghĩa: đăng ký).
- Trong prompt chỉ mô tả **hình dáng + chất liệu**; **không viết tên nút bằng chữ** (viết ra là model vẽ thành chữ/nút giả ngay).
- QC frame 3 giây cuối: có đủ 2 hình, dễ nhận ra, và **không có bất kỳ chữ nào**.

## Checklist QC trước khi giao
- [ ] ffprobe từng cảnh: đúng **10.0s**, có đủ hình + tiếng.
- [ ] Từng cảnh đã upscale **1080x1920**.
- [ ] Phim ráp: 1080x1920, thời lượng đúng công thức crossfade.
- [ ] Frame 1–2s đầu (hook): món/chảo rõ, bắt mắt ngay.
- [ ] Frame cao trào (cắt/reveal): khoảnh khắc ngon nhất hiện rõ, không lỗi morphing.
- [ ] Frame 3 giây cuối: CTA bằng chất liệu, đủ ngón cái + chuông, **không chữ**.
- [ ] Không frame nào có **phụ đề/chữ** cháy trên hình.
- [ ] Tay, chảo, bàn, ánh sáng nhất quán giữa các cảnh (cảnh nào lệch: render lại riêng cảnh đó và báo người dùng).
- [ ] Đã nhắc người dùng tự nghe kiểm **giọng dẫn tiếng Việt** (trợ lý không nghe được audio tự tạo).

## Giao phim
- Upload **bản gốc 1080P** lên Google Drive, gửi **link Drive** (đây là cách giao mặc định — mở file nặng ngay trong chat rất chậm).
- Kèm bản preview nhẹ 540x960 (crf 28) nếu người dùng muốn xem nhanh trong chat.
- Tên file gốc theo chuẩn algo ở gói SEO File 03.
