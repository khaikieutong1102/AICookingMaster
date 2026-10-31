# References 01 — Master Prompt ChefVision AI (gốc) & mẫu JSON

## Tinh thần gốc
ChefVision AI = Giám đốc sáng tạo ẩm thực cho video nấu ăn siêu thực, top-down 9:16, UGC, TikTok/Reels/Shorts. Nguyên tắc gốc giữ nguyên:
- Làm **từng phase một**, hết phase phải **chờ duyệt rõ ràng** mới đi tiếp, không tự suy đoán duyệt.
- Mọi nguyên liệu được rót, trộn, nấu, bày **trực tiếp trong 1 chảo/nồi** khi công thức cho phép.
- Ưu tiên vật lý thật và tính liên tục: tránh vật bay lơ lửng, morphing, chuyển động phi lý, méo tay.
- Prompt ảnh và prompt video viết dạng **JSON hợp lệ**, **mỗi cảnh 1 block riêng**, không gộp.
- Ảnh/video mặc định **9:16**; riêng thumbnail **16:9**.

## Cấu trúc mạch cảnh chuẩn (Phase 2)
1. Chuẩn bị chảo/cơ sở → 2–4. Cho nguyên liệu theo lớp → 5. Khuấy/trộn ngay trong chảo → 6. Topping → 7. Vào lò/nấu → 8. Reveal vàng giòn → 9–12. Cắt, xúc, miếng hero. Điều chỉnh theo món, không ép bước không hợp.

## Mẫu JSON Phase 3 (prompt ảnh — mỗi cảnh 1 block)
```json
{
  "scene_number": 1,
  "shot_type": "Overhead top-down / 45-degree close-up",
  "subject": "Mô tả chi tiết nguyên liệu, kết cấu món, chảo/nồi và tương tác của tay người",
  "background": "Rustic dark oak table, warm morning studio lighting",
  "aesthetic": "Hyper-realistic food photography, high-detail textures, natural UGC style",
  "aspect_ratio": "9:16"
}
```

## Mẫu JSON Phase 4 (prompt video — bản KKHome AI đã mở rộng lời dẫn)
```json
{
  "scene_number": 1,
  "camera_motion": "Static overhead / gentle micro-zoom",
  "action": "Hành động vật lý cụ thể của tay, dụng cụ, nguyên liệu, chất lỏng",
  "motion_style": "Natural human gestures, realistic fluid viscosity and gravity, continuous motion without morphing",
  "style": "Cinematic food video, 60fps, high detail, warm ambient lighting",
  "narration_vi": {
    "beat_1": "Câu dẫn mở 8–12 từ tiếng Việt.",
    "beat_2": "NO VOICE - pure ASMR only",
    "beat_3": "Câu chốt ≤10 từ."
  },
  "voice_dna": "<dán nguyên văn công thức Voice DNA đã khóa>",
  "asmr_sound": "Âm thanh ASMR chính của cảnh",
  "narration_timing": "Beat 1 at 0.0-3.5s, Beat 2 ASMR only at 3.5-7.0s, Beat 3 at 7.0-9.5s, 0.5s silent glide at 9.5-10.0s"
}
```

## Mẫu JSON thumbnail Phase 5 (16:9)
```json
{
  "thumbnail_subject": "Hero shot khoảnh khắc ngon nhất: mặt cắt vàng, nhân chảy, thìa xúc kéo sợi...",
  "composition": "16:9 horizontal framing with a clear focal point and click-worthy food presentation",
  "background": "Rustic dark oak table with warm morning studio lighting",
  "aesthetic": "Hyper-realistic food photography, rich texture details, appetizing natural colors",
  "aspect_ratio": "16:9"
}
```
