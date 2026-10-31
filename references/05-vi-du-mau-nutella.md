# References 05 — Ví dụ mẫu đã kiểm chứng: "Bánh Nutella Nhân Chảy 1 Chảo"

Dự án thật chạy trọn SKILL này ngày 31/10/2026 — dùng làm mẫu đối chiếu khi chạy dự án mới.

## Thông số đã chốt
- Món: Molten Nutella Pan Cake — trộn bột **trực tiếp trong chảo gang đen**, giấu 5 muỗng Nutella ở giữa + xoáy vân, topping hạt phỉ + socola chip, nướng lò, cắt ra nhân trào, thìa hero kéo sợi.
- Giọng dẫn: nữ vui tươi năng lượng TikTok (Voice DNA ở references/02).
- 10 cảnh × 10s → phim ráp **95.5s**, 1080x1920. Visual DNA: chảo gang đen + tay nữ móng tự nhiên + bàn gỗ sồi tối + sáng ấm.

## Mạch 10 cảnh + lời dẫn (rút gọn)
1. Quét bơ tan xèo xèo — "Hôm nay làm bánh Nutella nhân chảy trong một chảo thôi nha!" → "Bơ tan xèo xèo, nghe đã tai chưa?"
2. Rây bột như tuyết — "Rây bột mì, đường và bột nở cho thật mịn nè." → "Bột rơi như tuyết, nhìn mê quá đi!"
3. Trứng, sữa, bơ rót vào — "Thêm trứng, sữa tươi và bơ tan chảy vào luôn nhé." → "Dòng sữa này sánh mịn, thơm béo lắm luôn!"
4. Khuấy bột bóng mượt — "Khuấy đều tay đến khi bột bóng mượt, không còn lợn cợn." → "Bột mượt thế này, bánh mới mềm xốp được!"
5. Giấu nhân Nutella — "Giờ giấu Nutella thành từng muỗng tròn vào giữa bột nè." → "Đây là bí mật của phần nhân chảy đó!"
6. Rắc topping — "Rắc thêm hạt phỉ và socola chip lên mặt bánh nha." → "Topping đầy ụ, lát nướng lên giòn rụm!"
7. Cho vào lò — "Cho chảo vào lò, nướng đến khi mặt bánh vàng thơm." → "Chờ chút thôi, điều kỳ diệu sắp tới rồi!"
8. Reveal ra lò — "Ra lò rồi nè, mặt bánh vàng ươm, thơm nức mũi luôn!" → "Bánh còn phồng xốp, hơi nóng bốc lên kìa!"
9. Cắt miếng đầu, nhân trào — "Cắt miếng đầu tiên, mọi người nhìn nhân chảy ra nè!" → "Nutella trào ra rồi, trời ơi đỉnh chưa!"
10. Thìa hero + CTA — "Xúc một thìa to, nhân kéo sợi, bánh mềm tan ngay." → "Lưu video này lại, làm thử cuối tuần nha!"

## Poster & SEO của tập mẫu
- Poster (File 02): title event **"NHÂN CHẢY TRÀO RA"** kết từ dải Nutella chảy + hơi nóng ở 1/3 trên; foreground macro = thìa xúc nhân chảy; render trực tiếp đạt chuẩn (chữ đúng dấu, đọc rõ trên điện thoại).
- SEO (File 03): tiêu đề 1 = "Cắt Miếng Bánh Này Ra, Nutella TRÀO Cả Chảo Luôn Nè! #ASMR"; tên file gốc = `Banh_Nutella_Nhan_Chay_1_Chao_ASMR_1080P.mp4`.

## Kết quả & bài học QC
- Cả 10 cảnh ffprobe đúng 10.0s, có tiếng; ráp xfade/acrossfade 0.5s ra đúng 95.5s; bản gốc ~97MB giao qua Google Drive + bản preview 540x960 xem nhanh.
- Bài học: cảnh 10 bị model tự chuyển sang kiểu có người dẫn xuất hiện và ruột bánh sẫm màu hơn các cảnh trước → khi gặp lệch DNA như vậy phải **báo thật cho người dùng** và đề xuất render lại riêng cảnh đó, không giấu lỗi.
- Bài học 2: luật CTA bằng chất liệu + cấm phụ đề được Anh Khải chốt **sau** tập mẫu này — từ tập sau phải đưa CTA (ngón cái + chuông bằng chất liệu món) vào prompt cảnh cuối ngay từ đầu.
