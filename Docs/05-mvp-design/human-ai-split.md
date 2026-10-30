# Phân công người và AI — BẢN ĐỀ XUẤT

| Hạng mục | Người sáng lập | AI agents | Điểm kiểm tra bắt buộc |
|---|---|---|---|
| Thiết kế trải nghiệm | Chọn phong cách, bố trí sân chùa, nhịp chơi | Gợi ý luồng/chi tiết | Cảm giác yên bình, đủ ba trụ cột |
| Mô hình 3D | Tạo/chỉnh mô hình bằng Blender và AI 3D | Hỗ trợ checklist tối ưu, import | Bản quyền nguồn, đa giác, ánh sáng, chạy tốt trên Android |
| Điều khiển/UI | Trải nghiệm thử trên điện thoại | Codex/Claude viết từng chức năng | Không lỗi, dễ hiểu, thao tác bằng tay một cách tự nhiên |
| Online/NPC | Mở/đóng thử phòng, quan sát NPC | Xây kết nối + đường đi/lời thoại cố định | Không giả mạo người thật, không lộ thông tin cá nhân |
| Nội dung Phật giáo/xin xăm | Viết, kiểm tra tính tôn trọng và giới hạn | Soạn mẫu, chuẩn hóa dữ liệu | Không trộn tử vi với giáo lý, không khẳng định tác dụng thật |
| Tử vi | Xác nhận lá số mẫu và nội dung giải thích | Dựng giao diện minh họa | Không thu ngày/giờ sinh thật trong MVP |
| Test | Quyết định tiêu chí, mời người tham gia, xử lý phản hồi | Tổng hợp dữ liệu định lượng, log lỗi | Không tuyên bố kết quả khi thiếu mẫu/log |
| Phí & kinh doanh | Duyệt chi phí và quyết định thu phí sau | Bảng phân tích chi phí/biên lợi nhuận | Chưa kích hoạt thanh toán trong MVP |

## Quy tắc dùng agent
- Mỗi nhiệm vụ chỉ giao một thay đổi nhỏ có tiêu chí nghiệm thu cụ thể.
- Dùng Git để lưu phiên bản trước khi để agent sửa code.
- Người sáng lập tự chạy và xem game, không chấp nhận chỉ dựa vào AI nói “đã xong”.
- Không chia sẻ mật khẩu, khóa API, dữ liệu cá nhân với prompt/commit.

## Công việc mới đã duyệt — hỗ trợ bởi agent
| Hạng mục | Người sáng lập | Codex/Claude | Nghiệm thu |
|---|---|---|---|
| Mèo chùa | Dựng/duyệt mèo low-poly và thoại | Trigger trong công quả, UI 2 nút, giới hạn tần suất | Trải nghiệm không gián đoạn, không giễu nhại tôn giáo |
| Tịnh tâm rảnh tay | Chọn audio hợp quyền, kiểm tra nhiệt/pin | Chế độ camera tĩnh, timer, thoát, khôi phục FPS/màn hình | Chạy/thoát ổn trên 2 Android |
| Sen 7 ngày | Tạo 4 trạng thái sen và duyệt hình ảnh | Lưu ngày đầu, tính stage, khôi phục sau restart | Ngày 0,2,4,7 đúng; offline không mất Phước |

Chỉ giao mỗi lần một thay đổi nhỏ, commit Git trước và sau; chưa thuê người, chưa mở server production.
