# Kế hoạch thử nghiệm MVP — ĐÃ CHỐT THIẾT KẾ, CHƯA CHẠY THỬ

## Giả thuyết
Trong một cảnh chùa 3D có ba trụ cột giá trị, người chơi thuộc cả ba phân khúc quay lại vì trải nghiệm tự thân, không cần phạt đăng nhập.

## Cách đo, mẫu số, thời hạn
- Mục tiêu 15 người chơi thử độc lập, **5 mỗi nhóm**. Mẫu nhỏ chỉ cho tín hiệu định hướng, không suy rộng thị trường.
- Mỗi người được mời trải nghiệm qua APK thử Android. Điều kiện mẫu số: một người thuộc nhóm đã định và đã mở trò chơi/đi vào sân chùa lần đầu, không phải chỉ nhấp xem quảng cáo.
- Ngày 0 = thời điểm bắt đầu phiên đầu của từng người theo giờ Việt Nam. Ghi sự kiện `entered_first_session`.
- **Tỷ lệ quay lại D7** = số người trong 15 người đã vào game lại vào ngày lịch thứ 7 tính từ ngày 0 / 15 người có phiên đầu hợp lệ. Ghi sự kiện `returned_day7` từ hệ thống; nếu thiếu log, không tự nhận định.
- Đánh dấu `completed_core_loop` khi người chơi đã thư giãn/vãn cảnh, làm công quả và xin xăm. Ghi nguyên nhân lỗi/thất bại riêng.
- Bản online được kiểm thử trước với 2–5 người đồng thời; ghi lỗi đồng bộ và trải nghiệm mỗi máy.
- Sau khi phát bản thử cho người cuối, theo dõi đủ 7 ngày theo từng người và tổng kết trong 10 ngày sau khi người cuối vào lần đầu (có thời gian kiểm tra log). Ngày khởi động cụ thể chưa xác định.

## Ngưỡng đề xuất — không phải chuẩn thị trường
- **Có tín hiệu nên tiếp tục:** ≥6/15 quay lại D7 **và** mỗi nhóm có ít nhất 1 người quay lại, ≥10/15 hoàn tất vòng trải nghiệm, không có lỗi chặn toàn bộ.
- **Có tín hiệu cần đổi hướng:** ≤2/15 quay lại D7 khi đủ 15 người và log chính xác, hoặc lỗi chặn không thể khắc phục trong giới hạn chi phí.
- **Chưa đủ bằng chứng:** 3–5/15 quay lại; >5 người quay lại nhưng một nhóm có 0, không đủ 15 người đủ điều kiện, log thiếu hoặc không chạy ổn. Phải giữ nguyên số thực tế và phạm vi kết luận.
- Thu câu trả lời từ 1–2 câu hỏi sau phiên: “Điều gì muốn quay lại?” và “Điều gì khiến không muốn quay lại?”; câu trả lời là dữ liệu định tính, không thay cho tỷ lệ quay lại.

## Hai cửa kiểm soát rủi ro trước khi mời người thật
A. **Prototype đơn máy:** đi lại, công quả, xin xăm, ngồi thiền, FPS đo trên ít nhất hai máy Android thực (tự đặt mục tiêu khoảng 30 FPS ổn định trên máy thử, chưa phải chuẩn thị trường).
B. **Online nhỏ:** 2 máy kết nối đồng thời, thấy nhau di chuyển; server ngắt vẫn cho vào cảnh đơn máy, NPC nhận diện minh bạch; không có mất dữ liệu Phước do đồng bộ.
Nếu không đạt cổng A/B thì chưa mời người thật.

## Trần chi phí đề xuất, không phải báo giá
- Chi tối đa 2.000.000 VND cho bản đơn máy và tài nguyên cần mua.
- Chi tối đa thêm 1.000.000 VND cho server/kiểm thử đồng bộ.
- Chi tối đa 1.000.000 VND cho tuyển người thử, phương tiện test và phát sinh.
- **Giữ lại 6.000.000 VND**, không tự động chi nếu chưa có tín hiệu.
- Ngừng phát sinh khi đã dùng hết 4.000.000 VND thử nghiệm mà vẫn không có vòng chơi ổn trên điện thoại, hoặc không vượt được cổng B trong ngân sách. Có thể giảm phạm vi thay vì đốt tiếp.
- Thời gian founder: 6–8 tiếng/ngày theo nguồn lực; không cam kết ngày xong, chia việc thành mốc đạt đầu ra.

## Trình tự và người phụ trách
1. Founder duyệt MVP, phác sơ đồ sân chùa và phong cách hình ảnh; AI soạn bảng nhiệm vụ kỹ thuật.
2. Founder dựng mô hình, AI viết di chuyển và tương tác nhỏ; founder test trên Android.
3. Founder duyệt nội dung xin xăm/nhang/Phước; AI tích hợp UI và logic.
4. AI hỗ trợ tạo phòng nhỏ và đồng bộ; founder mở thử hai máy, ghi lỗi.
5. Founder mời người chơi thực tế bằng bài giới thiệu trung thực, xin đồng ý dùng log ẩn danh; AI giúp tổng hợp kết quả.
6. So sánh số liệu với ngưỡng đặt trước; không sửa ngưỡng sau khi xem kết quả.

## Tùy kết quả
- Tín hiệu tốt: chuyển xây nguyên mẫu cho vòng tiếp theo, nghiên cứu sản phẩm tử vi trả phí riêng.
- Tín hiệu yếu: phỏng vấn để xác định thiếu thư giãn, sinh hoạt chùa hay tâm linh; đổi một yếu tố rồi thử lại.
- Chưa rõ: tăng mẫu nhỏ có kiểm soát hoặc sửa lỗi log và chạy lại, không tuyên bố thành công.

## Cập nhật phép thử do MVP được bổ sung ba tính năng — ĐÃ DUYỆT 30/10/2026
- **Không đổi:** 15 tester (5/nhóm), hai cổng A/B, trần 4 triệu và 6 triệu dự phòng; giữ nguyên các ngưỡng D7 6/15 và vòng chơi 10/15 đã chốt trước đó.
- **Log phụ**, không thay chỉ số chính: `triggered_cat_event` (một lần theo tester/phiên), `started_idle_zen_mode`, `completed_idle_15m` (đủ 15 phút không bị gián đoạn), `viewed_lotus_stage` (gắn giá trị `stage=bud/leaf/flower`, và `day_since_first_use` theo cách định nghĩa ở spec). Log chỉ tester_id ẩn danh, không thu ngày sinh thật.
- **Phản hồi bổ sung**: người thử thấy tương tác mèo vui hay phiền? Có muốn dùng chế độ rảnh tay không? Cây sen có khiến muốn quay lại không? Câu hỏi định tính, không được thay thế log D7.
- **Đo vận hành:** trên tối thiểu hai Android thực, đo FPS/ổn định và so sánh mức tiêu hao pin cùng điều kiện (cùng máy, thời lượng gần nhau) ở chế độ thường và idle. Chưa đặt hoặc công bố mức tiết kiệm pin trước khi có số đo.
- **Giải thích D7:** phép thử hiện đánh giá mức quay lại của **toàn bộ MVP có sen 7 ngày**, không chứng minh khả năng giữ chân của cảnh chùa tĩnh. Nếu sau này thêm sự kiện/nhắc D7 thì phải ghi người nhận thông báo và cập nhật kế hoạch trước khi thử.
- **Cổng A bổ sung:** mèo hoàn thành không tắc; idle hẹn giờ 15 phút và khôi phục cài đặt khi thoát; sen lưu tiến trình qua app restart và giả lập ngày; đo FPS 2 máy. Chỉ làm online khi đơn máy ổn.
- **Cổng B không thay đổi:** 2 máy đồng bộ online và có phương án offline khi mất mạng.
- **Điều kiện dừng:** nếu phát sinh mới đe dọa trần 4 triệu, cắt giảm hiệu ứng/đồ họa bổ sung trước, không tự tăng quỹ hoặc giảm chuẩn đo lường.
- Đây là **thiết kế phép thử**, không phải kết quả chạy thử; mọi giả thuyết vẫn `unverified`.
