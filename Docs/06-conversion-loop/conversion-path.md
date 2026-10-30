# OPC 06 — Đường đi từ tiếp cận đến trải nghiệm (đề xuất)

## Mẫu luồng
Bài đăng Facebook và video TikTok (được phép công bố) → một form đăng ký miễn phí → kiểm tra đủ điều kiện/đồng ý log → chọn đủ 5 người/nhóm → gửi bản Android thử qua Firebase App Distribution → phiên đầu → phản hồi → theo dõi D7.

Vì MVP **không có thanh toán**, 'giao dịch' ở vòng này là **đồng ý tham gia dùng thử và nhận bản test miễn phí**, không phải mua hàng. Đường bán luận giải tử vi trả phí được kiểm chứng ở vòng sau; không gắn màn hình thanh toán giả dễ gây hiểu lầm.

## Từng bước + người làm + đo
| Bước | Người làm | Dữ liệu | Chỗ mất người |
|---|---|---|---|
| Đăng bài sau khi xin phép | Founder | nhóm, ngày đăng, số bài được duyệt; lượt xem chỉ tham khảo | Bài bị từ chối, không phù hợp người đọc |
| Form đăng ký | Founder thiết lập, AI soạn | người nộp form thực tế, nguồn đến | Link khó mở, thông điệp chưa rõ |
| Sàng lọc | Founder | số đủ điều kiện / tổng form; 5 người/nhóm; trùng email chỉ tính một | Thiếu Android, chưa đồng ý log |
| Mời cài bản thử | Founder qua Firebase | số được gửi lời mời / người đủ điều kiện; số chấp nhận | Email vào spam, khó cài |
| Phiên đầu | Game ghi event, founder giám sát | `entered_first_session` / người nhận lời mời có thể cài | Lỗi APK, FPS, không hiểu điều khiển |
| Trải nghiệm cốt lõi | Game | `completed_core_loop` / người vào lần đầu | Khó dùng, mất kết nối |
| Ngày thứ 7 | Game, founder tổng hợp | `returned_day7` / người có phiên đầu hợp lệ D7 đã chín muồi | Không đủ thú vị, lỗi hoặc quên |

- Chỉ số chính thử nghiệm giữ nguyên Bước 05: **≥6/15 quay lại D7** và mỗi nhóm ≥1, ≥10/15 hoàn thành vòng chơi, không lỗi chặn. **≤2/15** là tín hiệu yếu. Phần còn lại hoặc thiếu dữ liệu: chưa kết luận.
- Không lấy lượt xem bài làm số người đủ điều kiện được tiếp cận, không lấy đăng ký làm số người đã chơi. Đếm mỗi người một lần qua `tester_id`.
- Thời gian bắt đầu chỉ sau khi vượt cổng đơn máy và online trên thiết bị thật, theo múi giờ Asia/Ho_Chi_Minh.
- Người thử có thể tự rút lui; không bắt buộc đăng nhập, không phạt Phước vì nghỉ.

## Phương tiện theo dõi
1 sheet CSV chỉ chứa tester_id ẩn danh, nguồn, nhóm và trạng thái. Email liên hệ lưu riêng có giới hạn người truy cập, không đưa vào log gameplay.
Các sự kiện `entered_first_session`, `completed_core_loop`, `returned_day7` ghi theo tester_id, không đòi họ tên/ngày sinh thật.

## Hướng phát hành thử
Firebase App Distribution: https://firebase.google.com/docs/app-distribution/android/distribute-console
Nhà phát triển tạo APK đã ký, đưa lên Firebase Console và mời từng tester qua email sau khi họ đồng ý.
Nếu chưa có ứng dụng, chưa tạo liên kết mời hoặc tuyên bố đã phát hành.

## Quyết định kênh sau cập nhật
- Facebook và TikTok là hai kênh chính cùng lúc. Ghi nguồn theo mỗi người ở form, không gộp toàn bộ lượt xem rồi coi là số người đã tiếp cận đủ điều kiện.
- Một người có thể xem ở cả hai kênh: ghi nguồn lần đầu tự khai, không đếm hai lần ở các chỉ số theo người.
- Tạo cùng bản APK thử nghiệm cho hai kênh; các phép đo trên người chơi là chung một cohort có thông tin nguồn.
