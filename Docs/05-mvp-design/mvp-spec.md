# Bước 05 — MVP: “Chốn An Nhiên” (tên tạm) — ĐÃ CHỐT PHẠM VI, CHƯA TRIỂN KHAI

## Giả thuyết duy nhất cần kiểm tra trước
Người trong cả ba nhóm khách hàng sẽ tự nguyện quay lại không gian chùa 3D vào ngày thứ 7 sau khi trải nghiệm đầu tiên, dù không có phần thưởng gây áp lực đăng nhập. Nếu không quay lại, mở rộng công nghệ/thu phí chưa có căn cứ.

## Ai được thử
15 người thật, cố gắng 5 người/nhóm: (1) giới trẻ và dân văn phòng, (2) Phật tử/người thường đi chùa, (3) người thích tử vi/tâm linh. Các nhóm ngang hàng, không mặc định một nhóm quan trọng hơn. Tốt nhất là chưa tham gia phát triển game.

## Dạng MVP
Nguyên mẫu một vòng trải nghiệm có thể chạy trên điện thoại Android. Có **một phòng online riêng thử 2–5 người thật**, các vị trí vắng được NPC đi lại làm nền. NPC phải được gắn nhận dạng rõ, không giả làm người thật. Tạm không phát hành cửa hàng ứng dụng công khai.

## Một vòng chơi 8–12 phút (mục tiêu thiết kế, không áp đặt thời gian)
1. Vào cổng, nghe chuông và vãn cảnh.
2. Làm công quả nhẹ (quét lá hoặc chăm sen); nhìn thấy phản hồi Phước.
3. Vào chính điện, sử dụng một vật phẩm nhang ảo miễn phí.
4. Xin một quẻ xăm miễn phí, xem lời giải cơ bản mang tính văn hóa.
5. Chọn xem giao diện **lá số mẫu** (không yêu cầu cung cấp ngày sinh thật trong MVP); không mua bán thật.
6. Chọn ngồi thiền, ngắm cảnh, trò chuyện giới hạn với người thật/NPC, rồi tự do rời đi.

## Trong phạm vi
- Một sân chùa, một chính điện nhỏ, một hồ sen và lối đi.
- Một kiểu nhân vật đồng nhất trong thế giới, di chuyển chạm/màn hình cảm ứng, góc nhìn thứ ba.
- 3 NPC có đường đi và lời thoại viết sẵn, nhận diện được là NPC.
- Đồng bộ tối thiểu vị trí/hành động của 2–5 người thật trong một phòng; có cách tự chạy bản offline nếu server không sẵn.
- 2 hành động công quả nhẹ (quét lá, chăm sen) + thắp một nhang ảo miễn phí.
- Chỉ số Phước tích lũy không giảm khi offline; Duyên lành có thể giảm. Không công bố thước đo đạo đức/nhân quả thật.
- Xin xăm miễn phí và diễn giải văn hóa ngắn. Màn hình lá số tử vi mẫu, không cần tên/ngày giờ sinh thật.
- Góc thiền, âm thanh êm, hồ sơ đơn giản chỉ thấy trang phục/điểm khi nhấn xem.
- Ghi log ẩn danh tối thiểu: bắt đầu phiên, hoàn thành công quả, xin xăm, vào lại ngày 7.

## Ngoài phạm vi MVP
- Thanh toán, bán báo cáo tử vi chi tiết, hệ thống tử vi đầy đủ, AI tạo nội dung thời gian thực.
- AI NPC hội thoại tự do, chatbot thầy tu, hàng trăm NPC, hàng chục khu vực, công cụ xây chùa.
- Chat mở cho người lạ, vật phẩm bán bằng tiền thật, quyên góp tiền thật, xếp hạng Phước.
- Android+iOS cùng lúc; chưa triển khai iOS, không chốt engine cuối cho dự án mở rộng.

## Đề xuất kỹ thuật, không phải lựa chọn đã chốt
- **Godot 4 (GDScript)** để làm game Android 3D; dùng Blender cho mô hình, Codex/Claude cho tác vụ code nhỏ. Godot có xuất Android theo tài liệu chính thức.
- Ưu tiên một cảnh nhỏ, ánh sáng nướng sẵn, vật thể tối ưu, kiểm tra hiệu năng trên điện thoại thật.
- Hệ thống multiplayer chỉ mở khi bản đơn máy ổn; phòng thử riêng, không tổ chức cộng đồng rộng.
- Dữ liệu Tử vi thật và giao dịch thu phí để vòng riêng, tránh thu thập dữ liệu sinh trong MVP.

## Lý do chọn
Đủ ba trụ cột (thư giãn, đời sống chùa, văn hóa tâm linh), vừa kiểm tra rủi ro công nghệ online lẫn việc người chơi muốn quay lại. Không đánh đồng khen đẹp với sự quan tâm lâu dài.

## Trạng thái
MVP đã được người dùng duyệt, các bổ sung từ review ngày 30/10/2026 cũng đã được duyệt. Chưa có người thử, chưa có kết quả chứng minh giả thuyết.

## Bổ sung MVP ĐÃ ĐƯỢC CHỐT — 30/10/2026 (từ review gameplay)
Người dùng đã phê duyệt đúng **ba bổ sung tinh gọn**. Không tự thêm các tính năng mở rộng khác trong review.

### A. Một tình huống mèo chùa (thiền vị hài)
- Trong sân chùa, khi người chơi quét lá, một mèo chùa low-poly chạy đến hoặc nằm lên đống lá (tối đa một lần trong phiên thử).
- Hai phản hồi đơn giản, nhẹ nhàng: **chờ/gãi mèo** và **quét sang bên cạnh**; cả hai đều hoàn thành được công quả, không ép chọn 'đúng đạo đức'.
- Có một lời thoại dí dỏm, không chế nhạo Phật, giáo lý hoặc nghi lễ. Chính điện giữ trang nghiêm.
- **Đạt:** trên Android mèo xuất hiện đúng ngữ cảnh, hai nút bấm hoạt động, không khóa vòng chơi, không lặp gây phiền. Không cần AI hội thoại.

### B. Tịnh tâm rảnh tay v0 — đúng một chế độ
- Nút lớn **Tịnh tâm rảnh tay** đưa nhân vật ngồi tại hồ sen; phát một vòng âm thanh dịu nhẹ **được phép sử dụng**, đã có sẵn trong ứng dụng; hẹn giờ 15 phút, có nút kết thúc thủ công.
- Chế độ giảm nhịp xử lý/khung hình khi cảnh tĩnh nếu máy đáp ứng, rồi **khôi phục cài đặt cũ khi thoát**; không khẳng định tỷ lệ tiết kiệm pin khi chưa đo.
- Việc giữ màn hình sáng phải theo lựa chọn và khả năng hệ điều hành; **không cam kết nghe khi khóa màn hình**. Khi hết giờ âm thanh dừng nhẹ và trả về tương tác bình thường.
- Không tự cộng Phước do treo máy. Có thể phản hồi Tâm An như chỉ số trải nghiệm (không là chỉ số phước thật).
- **Đạt:** vào/ra một chạm, âm thanh và hẹn giờ hoạt động, thoát giữa chừng không bị treo, không để lại chế độ giảm FPS/giữ màn hình sau khi thoát.

### C. Sen Duyên Lành — tiến trình 7 ngày
- Một chậu sen riêng có **bốn mesh/trạng thái**: mầm (ngày 0–1) → lá (ngày 2–3) → nụ (ngày 4–6) → hoa (ngày 7 trở đi); dùng ngày bắt đầu theo múi giờ Việt Nam và lưu tiến độ qua các lần mở lại.
- Không chết cây, không giảm Phước khi offline. Nếu Duyên lành biến thiên, đó là chỉ báo mềm và tưới sen giúp cây tươi lại, **không ép đăng nhập**.
- **Đạt:** tắt/mở game không mất chậu, trạng thái thay đổi đúng theo đồng hồ ngày thử; ca kiểm thử chỉnh ngày/đồng hồ được ghi nhận, chưa quảng bá tính chống gian lận production.

### Không bổ sung ở vòng này
Đêm Hoa Đăng D7, 7 lá số mới, đài radio nhiều tập, kinh hành tự động, bốn chế độ treo máy, stream audio từ cloud, bảng thời trang xỏ nhầm dép, AI NPC tự do. Không tăng chi phí thử nghiệm 4 triệu hoặc thay 15 tester.

**Hiện trạng:** Đây là đặc tả đã duyệt, **không có nghĩa các tính năng đã được lập trình hoặc kiểm thử**.
