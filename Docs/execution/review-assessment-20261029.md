# Đánh giá review gameplay Chốn An Nhiên — 29/10/2026

**Tài liệu nguồn:** `inputs/reviews/20261029-review-gameplay-zen-idle.md` (review do người dùng đính kèm). Ở giai đoạn `execution`, các đề xuất dưới đây **chưa được người dùng xác nhận thay đổi phạm vi**. Không tự nâng trạng thái giả thuyết từ `unverified`.

## Hữu ích và nên ưu tiên để thảo luận
1. Thiền vị hài, chia hai vùng cảm xúc: Chính Điện trang nghiêm; sân chùa/hồ sen/góc xin xăm có tình huống nhỏ dễ thương. Chọn 1 tương tác mèo nằm đống lá và một mẫu thoại Cụ Từ cho MVP.
2. Chế độ Tịnh Tâm Rảnh Tay 1 chạm: thử bản **một chế độ** ngồi trước hồ sen, âm thanh offline, hẹn giờ 15 phút, tùy chọn tắt màn hình tùy hệ điều hành, tùy chọn giảm FPS/độ phân giải. Tính năng tiết kiệm pin phải đo trên máy thật; không hứa pin giảm 60%.
3. Dùng 1 chậu sen 4 trạng thái có tiến trình theo ngày để tăng lý do quay lại, nhưng không biến phước thành cơ chế ép online.
4. Tăng tính cách NPC bằng bảng thoại tĩnh JSON, tránh AI gọi trực tuyến và chi phí không kiểm soát.

## Trì hoãn để tránh phình MVP
- 4 chế độ treo máy đầy đủ, radio nhiều tập từ đám mây, kinh hành auto, đồng tu online ở chế độ treo máy, hàng chục xăm/lá số, minigame xỏ nhầm dép, 7 kỳ án lá số.
- Sự kiện Đêm Hoa Đăng ngày thứ 7 chỉ thêm sau khi cổng A đạt. Nếu thêm, ghi rõ số liệu D7 đo **khả năng thu hút trở lại có sự kiện**, không được mô tả là sức giữ chân tự nhiên của một cảnh tĩnh. Kế hoạch gốc chưa tách hai hiệu ứng này.
- 3–4 người lớn tuổi có thể tuyển như tiểu nhóm khám phá, nhưng không tự đổi ba phân khúc ngang hàng đã xác nhận; 15 người không đủ để đánh giá kết quả theo tuổi một cách đáng tin.

## Các khẳng định kỹ thuật cần sửa
- Google Play Internal Testing là hướng phân phối thử khả thi, không bắt buộc. Phí Play Console là 25 USD một lần, nhưng còn công tác tài khoản, xác minh, tuân thủ; chi phí VND phụ thuộc tỷ giá. Personal developer accounts mới cần closed test >=12 người liên tục 14 ngày trước **sản xuất công khai**, không phải trước internal test. Nguồn: https://support.google.com/googleplay/android-developer/answer/14151465 ; https://support.google.com/googleplay/android-developer/answer/9845334 ; https://support.google.com/googleplay/android-developer/answer/6112435
- Supabase Realtime **Broadcast** có thể chuyển vị trí/trạng thái mức thấp; **Presence** chỉ dành cho online/offline, không dùng cập nhật tọa độ liên tục. Không có cơ sở khẳng định việc xây mạng chỉ 80 dòng, hoặc dùng REST một mình thay thế hoàn toàn kết nối nhận cập nhật WebSocket. Cần authentication, giới hạn kênh, smoothing/lag, reconnect, chi phí fanout, và bảo vệ dữ liệu. Free plan có quota, không bảo đảm miễn phí mãi. Nguồn: https://supabase.com/docs/guides/realtime/presence ; https://supabase.com/docs/guides/realtime/broadcast ; https://supabase.com/docs/guides/platform/manage-your-usage/realtime-messages
- Godot có DisplayServer.screen_set_keep_on, Engine.max_fps, viewport.scaling_3d_scale và AudioStreamOggVorbis.load_from_buffer. Phải đo pin/nhiệt/FPS trên 2 điện thoại thực, không xác nhận 'giảm 60% điện GPU' khi chưa có đo đạc; màn hình bật sáng 30–45 phút có thể hao pin. Nguồn: https://docs.godotengine.org/en/stable/classes/class_viewport.html ; https://docs.godotengine.org/en/latest/classes/class_displayserver.html ; https://docs.godotengine.org/en/latest/classes/class_audiostreamoggvorbis.html
- Không lấy ngày sinh trong MVP **giảm** rủi ro dữ liệu nhạy cảm, nhưng không 'loại bỏ hoàn toàn' vấn đề bảo mật vì vẫn có email tester và event logs.
- '100% khả thi với 4 triệu', 'tạo assets trong 2 ngày', 'nhóm lớn tuổi có khả năng trả phí cao nhất' đều là **nhận định chưa được chứng minh**. Không thay thế số liệu người dùng và thử nghiệm thực.
- Idle tự động +Phước dựa trên số phút treo dễ mâu thuẫn thông điệp Phước tượng trưng cho việc thiện; nên thử +Tâm An và chỉ cho Phước khi có hành động có chủ đích, không mua điểm.

## Quyết định đang chờ
Người dùng cần chốt có muốn đưa 3 cải tiến tinh gọn (thiền vị hài một tương tác + idle một chế độ + sen 7 ngày) vào **MVP hiện tại** hay giữ làm thử nghiệm ở sprint kế tiếp. Trước khi chốt, không thay `mvp-spec.md`, `experiment-plan.md` đã được xác nhận và không thay D7 metric.
