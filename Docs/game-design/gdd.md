# TÀI LIỆU THIẾT KẾ TRÒ CHƠI (GDD)

## "Chốn An Nhiên" — Không gian chùa Việt 3D trực tuyến

| Mục | Giá trị |
|---|---|
| Phiên bản | 1.0 |
| Ngày | 2026-10-30 |
| Trạng thái tài liệu | Định hướng đã chốt; game **chưa được lập trình** |
| Phạm vi | Toàn bộ thiết kế trò chơi + phạm vi MVP đã duyệt |
| Nguồn tổng hợp | `05-mvp-design/mvp-spec.md`, `experiment-plan.md`, `human-ai-split.md`, `02-niche-positioning/*`, `03-value-proposition/*`, `04-business-model/*`, `execution/review-assessment-20261029.md`, bổ sung duyệt 30/10/2026 |
| Quy ước đánh dấu | **[CHỐT]** = đã được chủ dự án phê duyệt · **[ĐỀ XUẤT]** = hướng đưa ra, chưa duyệt · **[GT]** = giả thuyết, chưa kiểm chứng |

---

## 1. TỔNG QUAN

### 1.1. Mô tả một câu **[CHỐT]**

Một không gian chùa Việt 3D trực tuyến, nơi người chơi chủ động đi lại, tham gia sinh hoạt chùa và khám phá văn hóa tâm linh — thay vì xem livestream một cách thụ động.

### 1.2. Thông tin cơ bản

| Hạng mục | Nội dung | Trạng thái |
|---|---|---|
| Tên tạm | Chốn An Nhiên | Tên tạm, chưa chốt tên chính thức |
| Dự án | Le-Phat-online (Lễ Phật Online) | — |
| Thể loại | Thế giới 3D thư giãn (zen/relax), xã hội nhẹ, văn hóa tâm linh | [CHỐT] |
| Nền tảng MVP | Android (mobile, cảm ứng) | [CHỐT] — iOS chưa triển khai |
| Engine đề xuất | Godot 4 (GDScript) + Blender dựng mô hình | [ĐỀ XUẤT] — chưa chốt engine cho dự án mở rộng |
| Mô hình chơi | Miễn phí; luận giải tử vi chi tiết có phí (sau MVP) | [CHỐT] nguyên tắc, [GT] nhu cầu |
| Ngôn ngữ | Tiếng Việt | [CHỐT] |
| Phát hành thử | APK thử qua form tuyển 15 người; không phát cửa hàng công khai ở MVP | [CHỐT] |
| Đội ngũ | 1 người sáng lập + AI agents (Codex/Claude/Gemini) hỗ trợ code | [CHỐT] |

### 1.3. Điểm khác biệt dự kiến **[GT]**

- So với livestream chùa: người chơi **chủ động** đi lại, làm việc, gặp người — không chỉ xem.
- So với game xã hội thông thường: **không cày cuốc, không áp lực đăng nhập, không cạnh tranh**.
- Lưu ý: lợi ích thực tế và mức độ sử dụng **chưa được kiểm chứng**.

---

## 2. TẦM NHÌN VÀ NGUYÊN TẮC THIẾT KẾ

### 2.1. Ba trụ cột giá trị **[CHỐT]**

Kết hợp **hài hòa**, không phân trụ cột chính/phụ:

1. **Thư giãn** — khung cảnh thiên nhiên, âm thanh nhẹ, nhịp chơi không áp lực.
2. **Sinh hoạt chùa** — trải nghiệm đời sống chùa Phật giáo một cách tôn trọng.
3. **Văn hóa tâm linh** — tử vi, xin xăm, phong tục dưới góc độ văn hóa, chiêm nghiệm; **không khẳng định dự đoán chắc chắn**.

Người chơi tự chọn hoạt động theo nhu cầu nhóm mình; không buộc trải nghiệm cả ba.

### 2.2. Nguyên tắc thiết kế bất di bất dịch **[CHỐT]**

1. **Không ép đăng nhập.** Không phạt vắng mặt bằng cách trừ Phước; không cơ chế "streak" gây áp lực.
2. **Tôn trọng tôn giáo.** Không giễu nhại Phật, giáo lý hay nghi lễ; không đồng nhất tử vi với giáo lý Phật giáo — hai hệ thống nội dung nằm trong khu vực/hoạt động riêng, được diễn giải riêng.
3. **NPC minh bạch.** NPC luôn có nhận dạng rõ, không giả làm người chơi thật.
4. **Không thước đo đạo đức thật.** Phước là cơ chế game, không công bố như thước đo nhân quả/nghiệp thật.
5. **Không cam kết gì chưa đo.** Không quảng bá mức tiết kiệm pin, hiệu năng hay khả năng giữ chân khi chưa có số liệu.
6. **Không thu dữ liệu nhạy cảm trong MVP.** Không lấy tên/ngày giờ sinh thật; log ẩn danh tối thiểu.
7. **Không tiền thật trong MVP.** Không thanh toán, không bán vật phẩm, không quyên góp thật; "cúng dường" chỉ là vật phẩm ảo.
8. **Phù phép thử.** Mọi thay đổi phép thử phải được phê duyệt **trước** khi thu dữ liệu; không sửa ngưỡng sau khi xem kết quả.

---

## 3. NGƯỜI CHƠI MỤC TIÊU

### 3.1. Ba nhóm ngang hàng **[CHỐT]**

Không phân nhóm chính/phụ; mỗi nhóm có lộ trình trải nghiệm riêng trong cùng không gian.

| Nhóm | Mong muốn (jobs) | Trở ngại (pains) | Kết quả mong đợi (gains) | Phần game phục vụ |
|---|---|---|---|---|
| Giới trẻ & dân văn phòng | Nghỉ ngắn, giảm căng thẳng, giao lưu ít áp lực | Thiếu nơi số yên tĩnh; game khác thúc ép cày cuốc | Thanh thản, muốn quay lại | Cảnh chùa 3D, âm nhạc, tản bộ, thiền, NPC thân thiện |
| Phật tử, người đi chùa | Tiếp cận không gian/sinh hoạt chùa khi không tới trực tiếp được | Khoảng cách, thời gian; lo thiếu trang nghiêm | Gắn kết, trải nghiệm có ý nghĩa | Lễ Phật, công quả, sự kiện, nội dung Phật giáo được rà soát |
| Người quan tâm tử vi, tâm linh | Khám phá phong tục, xin xăm, chiêm nghiệm | Thông tin rời rạc, thiếu bối cảnh | Trải nghiệm tương tác đẹp, có giải thích | Góc xin xăm, lá số mẫu, diễn giải văn hóa có giới hạn rõ |

Phân tích từng nhóm ở mức **giả thuyết** — chưa phỏng vấn thực tế.

---

## 4. VÒNG CHƠI CỐT LÕI

### 4.1. Vòng trải nghiệm chính: 8–12 phút **[CHỐT]**

Mục tiêu thiết kế, **không áp đặt** thời gian lên người chơi.

```
VÀO CỔNG ──► VÃN CẢNH ──► CÔNG QUẢ ──► LỄ PHẬT ──► XIN XĂM ──► LÁ SỐ MẪU ──► TỰ DO ──► RỜI ĐI
(chuông)    (đi bộ)      (quét lá /   (nhang     (diễn giải    (xem thử,     (thiền, ngắm
                          chăm sen +   ảo miễn     văn hóa       không cần     cảnh, trò chuyện
                          mèo chùa)    phí)        ngắn)         ngày sinh)    giới hạn)
```

Chi tiết từng bước:

| # | Bước | Nội dung | Ghi nhận |
|---|---|---|---|
| 1 | Vào cổng, nghe chuông và vãn cảnh | Mở đầu không lời, để âm thanh và khung cảnh dẫn dắt | `entered_first_session` (phiên đầu) |
| 2 | Công quả nhẹ | Quét lá hoặc chăm sen; **mèo chùa** có thể xuất hiện (§5.3); thấy phản hồi Phước | `completed_core_loop` (khi đủ công quả + xăm) |
| 3 | Vào chính điện, thắp nhang | Dùng một vật phẩm nhang ảo miễn phí; vùng trang nghiêm | log công quả |
| 4 | Xin một quẻ xăm | Miễn phí; lời giải cơ bản mang tính văn hóa | log xin xăm |
| 5 | Xem lá số mẫu | Giao diện minh họa; **không** yêu cầu ngày sinh thật; không mua bán thật | — |
| 6 | Chọn ngồi thiền / ngắm cảnh / trò chuyện giới hạn | Với người thật hoặc NPC; tự do rời đi bất cứ lúc nào | — |

**Định nghĩa `completed_core_loop`:** người chơi đã thư giãn/vãn cảnh, làm công quả **và** xin xăm.

### 4.2. Vòng dài hạn: Sen 7 ngày **[CHỐT]**

Chậu sen "Duyên Lành" của từng người chơi tiến triển theo ngày (§5.9), tạo lý do quay lại **mềm** — không chết cây, không phạt vắng mặt.

### 4.3. Vòng xã hội (tối thiểu) **[CHỐT]**

Thấy người thật khác (2–5 người/phòng) di chuyển, chào, trò chuyện giới hạn trong không gian chung.

---

## 5. CƠ CHẾ CHƠI CHI TIẾT

### 5.1. Hệ thống chỉ số **[CHỐT]**

| Chỉ số | Luật | Ghi chú |
|---|---|---|
| **Phước** (tích lũy) | Tăng khi làm công quả/hành động có chủ đích. **Không giảm chỉ vì offline.** | Không tăng do treo máy (idle không tự cộng Phước). Không mua điểm. Không xếp hạng Phước trong MVP. |
| **Duyên lành** | Có thể giảm khi vắng mặt. Tưới sen giúp cây tươi lại. | Chỉ báo **mềm**, nhắc nhẹ — không ép đăng nhập, không chết cây. |
| **Tâm An** | Phản hồi trải nghiệm khi dùng chế độ Tịnh tâm rảnh tay. | **Không phải** Phước thật; không khẳng định tác dụng tinh thần thật. |

Nguyên tắc gốc (từ review): Phước tượng trưng việc thiện → chỉ cộng khi có hành động có chủ đích; **không** trả điểm theo số phút treo máy.

### 5.2. Công quả — quét lá & chăm sen **[CHỐT]**

- Hai hành động nhẹ ở sân chùa / hồ sen: quét lá, chăm sen.
- Hoàn thành → phản hồi Phước hiển thị.
- Nội dung thuần khiết, mang ý nghĩa "làm việc chùa", không minigame khó.
- **Đạt:** vòng quét lá chạy ổn, không mắc kẹt nhân vật.

### 5.3. Mèo chùa — tình huống thiền vị hài **[CHỐT] — bổ sung 30/10/2026**

- Trong sân chùa, khi người chơi quét lá: một mèo chùa low-poly chạy đến hoặc nằm lên đống lá — **tối đa 1 lần mỗi phiên**.
- Hai phản hồi, cả hai đều hoàn thành công quả, không có đáp án "đúng đạo đức":
  1. **Chờ / gãi mèo** — dừng quét, vuốt ve.
  2. **Quét sang bên cạnh** — làm việc quanh chú mèo.
- Một lời thoại dí dỏm (Cụ Từ — nhân vật già chùa) đúng thời điểm; **không chế nhạo Phật, giáo lý, nghi lễ**.
- **Đạt (cổng A):** mèo xuất hiện đúng ngữ cảnh trên Android; 2 nút hoạt động; không khóa vòng chơi; không lặp gây phiền.
- Log phụ: `triggered_cat_event` (1 lần theo tester/phiên).
- Không cần AI hội thoại cho mèo.

### 5.4. Thắp nhang ảo **[CHỐT]**

- Một vật phẩm nhang ảo **miễn phí** trong MVP, dùng tại chính điện.
- Không vật phẩm tiêu hao phải mua trong MVP. Cúng dường ảo (hình thức) chỉ mô tả như vật phẩm trong game, **không** là quyên góp tiền thật.

### 5.5. Xin xăm **[CHỐT]**

- Xin một quẻ xăm miễn phí; lời giải **cơ bản**, ngắn, mang tính văn hóa.
- Diễn giải rõ giới hạn: chiêm nghiệm, không khẳng định dự đoán chắc chắn.
- Không đánh đồng với giáo lý Phật giáo.

### 5.6. Lá số tử vi mẫu **[CHỐT]**

- Màn hình **lá số mẫu** để xem thử — không yêu cầu tên/ngày giờ sinh thật trong MVP.
- Không mua bán thật, không hệ thống tử vi đầy đủ.
- Mục đích: cho nhóm quan tâm tử vi thấy hình dạng sản phẩm tương lai (luận giải sâu có phí, vòng sau).

### 5.7. Thiền & ngắm cảnh **[CHỐT]**

- Góc thiền yên tĩnh, âm thanh êm; ngồi thiền/ngắm cảnh là hoạt động tự do cuối vòng.
- Hồ sơ đơn giản: chỉ thấy trang phục/điểm khi nhấn xem.

### 5.8. Tịnh tâm rảnh tay v0 — đúng MỘT chế độ **[CHỐT] — bổ sung 30/10/2026**

- Nút lớn **"Tịnh tâm rảnh tay"** → nhân vật ngồi tại hồ sen.
- Phát **một vòng âm thanh dịu nhẹ đã có sẵn trong ứng dụng** (bản quyền hợp lệ — phải kiểm tra kỹ); hẹn giờ **15 phút**; có nút kết thúc thủ công (vào/ra một chạm).
- Giảm nhịp xử lý/khung hình khi cảnh tĩnh **nếu máy đáp ứng**; **khôi phục cài đặt cũ khi thoát** (FPS, độ phân giải, giữ màn hình).
- Giữ màn hình sáng theo lựa chọn người dùng và khả năng hệ điều hành; **không cam kết phát tiếng khi khóa màn hình**.
- Hết giờ: âm thanh dừng nhẹ, trả về tương tác bình thường; thoát giữa chừng không bị treo.
- Không tự cộng Phước do treo máy; phản hồi **Tâm An** như chỉ số trải nghiệm.
- **Đạt (cổng A):** âm thanh + hẹn giờ hoạt động; không để lại chế độ giảm FPS/giữ màn hình sau khi thoát.
- Log phụ: `started_idle_zen_mode`, `completed_idle_15m` (đủ 15 phút không gián đoạn).
- Đo vận hành trên ≥2 máy Android thật: FPS, pin, nhiệt — so với chơi thường, cùng điều kiện. **Không công bố % tiết kiệm pin trước khi có số đo.**

### 5.9. Sen Duyên Lành — tiến trình 7 ngày **[CHỐT] — bổ sung 30/10/2026**

Một chậu sen riêng cho mỗi người chơi:

| Ngày (múi giờ Việt Nam) | Trạng thái mesh |
|---|---|
| 0–1 | Mầm |
| 2–3 | Lá |
| 4–6 | Nụ |
| 7 trở đi | Hoa |

- Ngày 0 = ngày bắt đầu dùng chậu sen theo giờ Việt Nam; tiến độ **lưu qua các lần mở lại** (persist nội bộ).
- **Không chết cây, không giảm Phước khi offline.** Duyên lành biến thiên chỉ là chỉ báo mềm; tưới sen giúp cây tươi lại.
- **Đạt (cổng A):** tắt/mở game không mất chậu; trạng thái đổi đúng theo đồng hồ ngày; có ca kiểm thử chỉnh ngày/đồng hồ (ghi nhận; chưa quảng bá khả năng chống gian lận production).
- Log phụ: `viewed_lotus_stage` kèm `stage=bud/leaf/flower` và `day_since_first_use`.
- Phép thử D7 hiện đánh giá **toàn bộ MVP có sen 7 ngày** — không chứng minh riêng sức giữ chân của cảnh chùa tĩnh. Nếu sau này thêm sự kiện/nhắc D7 (ví dụ Đêm Hoa Đăng), phải ghi rõ người nhận nhắc và cập nhật kế hoạch phép thử trước khi chạy.

---

## 6. THẾ GIỚI VÀ BỐ CỤC KHÔNG GIAN

### 6.1. Bản đồ MVP **[CHỐT]**

```
        ┌─────────────────────────────────┐
        │  LỐI ĐI → CỔNG CHÙA             │  chuông chào
        ├─────────────────────────────────┤
        │  SÂN CHÙA                       │  quét lá · mèo chùa
        │  (vùng ấm áp, dễ thương)        │  NPC đi lại
        ├───────────────┬─────────────────┤
        │  CHÍNH ĐIỆN   │  HỒ SEN         │
        │  (trang nghiêm)│  (thiền · idle  │
        │  thắp nhang    │   sen 7 ngày ·  │
        │  xin xăm       │   chăm sen)     │
        └───────────────┴─────────────────┘
```

Một sân chùa, một chính điện nhỏ, một hồ sen và lối đi. Không khu vực khác trong MVP.

### 6.2. Hai vùng cảm xúc **[CHỐT]**

| Vùng | Tông | Hoạt động | Quy tắc nội dung |
|---|---|---|---|
| Chính điện | Trang nghiêm, tĩnh lặng | Thắp nhang, lễ Phật | Không tình huống hài; không thoại dí dỏm |
| Sân chùa, hồ sen, góc xăm | Ấm áp, thiền vị, dễ thương | Công quả, mèo chùa, thiền, idle | Tình huống nhỏ vui nhưng luôn tôn trọng |

### 6.3. Hướng nghệ thuật **[ĐỀ XUẤT]**

- Phong cách low-poly, ánh sáng nướng sẵn (baked lighting), vật thể tối ưu cho điện thoại.
- Cảnh nhỏ được chăm chút thay vì cảnh lớn dàn trải.
- Founder duyệt phong cách hình ảnh trước khi AI sản xuất.

---

## 7. NHÂN VẬT VÀ NPC

### 7.1. Nhân vật người chơi **[CHỐT]**

- Một kiểu nhân vật **đồng nhất** trong thế giới (không tùy biến ngoại hình trong MVP).
- Ngoại hình thế giới đồng nhất; thời trang/phông cách chỉ hiện trong **hồ sơ** (khi nhấn xem), không phân hóa trong sân.
- Góc nhìn **thứ ba**; di chuyển bằng chạm/màn hình cảm ứng.

### 7.2. NPC **[CHỐT]**

- **3 NPC** có đường đi và lời thoại **viết sẵn** (bảng thoại tĩnh — JSON, không AI hội thoại trực tuyến).
- NPC có gắn nhận dạng rõ (tên/viết chồng lên đầu) — không giả làm người thật; vị trí vắng được NPC đi lại làm nền.
- **Cụ Từ** (nhân vật già chùa): một câu thoại dí dỏm đúng thời điểm trong tình huống mèo.
- Không chatbot thầy tu, không AI NPC hội thoại tự do trong MVP.

---

## 8. ĐIỀU KHIỂN, CAMERA, GIAO DIỆN

| Hạng mục | Thiết kế | Trạng thái |
|---|---|---|
| Điều khiển | Cảm ứng: joystick ảo/chạm để di chuyển; nút tương tác ngữ cảnh (quét, tưới, ngồi, gãi mèo) | [CHỐT] dạng; chi tiết UI khi dựng |
| Camera | Góc nhìn thứ ba, tự theo sau nhân vật; khóa trong chế độ Tịnh tâm rảnh tay | [CHỐT] |
| UI | Tối giản: nút **Tịnh tâm rảnh tay** lớn; hồ sơ; phản hồi Phước nhẹ nhàng; không bảng xếp hạng | [CHỐT] |
| Ngôn ngữ UI | Tiếng Việt | [CHỐT] |
| Trợ giúp | Mỗi tương tác tự mô tả; không hướng dẫn dài | [ĐỀ XUẤT] |

---

## 9. ÂM THANH

- **Chuông chùa** khi vào cổng; âm nền êm dịu; âm tiếng bước, tiếng lá, tiếng nước nhẹ.
- Chế độ Tịnh tâm: đúng **một vòng âm thanh được phép sử dụng**, đóng gói sẵn trong app (AudioStreamOggVorbis, `load_from_buffer`); không stream từ cloud ở MVP.
- Không radio nhiều tập, không phát trực tuyến.
- Mọi asset audio phải kiểm tra bản quyền trước khi đưa vào.

---

## 10. CHẾ ĐỘ ONLINE

### 10.1. Phòng thử **[CHỐT]**

- **Một phòng online riêng**, 2–5 người thật đồng thời; NPC lấp nền các vị trí vắng.
- Đồng bộ **tối thiểu**: vị trí + hành động đơn giản của người thật.
- Chat giới hạn, không chat mở cho người lạ.

### 10.2. Chạy offline khi mất server **[CHỐT]**

- Server ngắt vẫn vào được cảnh đơn máy; **không mất dữ liệu Phước** do đồng bộ.

### 10.3. Ghi chú kỹ thuật **[ĐỀ XUẤT — từ review, có nguồn]**

- Supabase Realtime **Broadcast** phù hợp truyền vị trí/trạng thái mức nhẹ; **Presence** chỉ dùng online/offline, không cập nhật tọa độ liên tục.
- Cần: authentication, giới hạn kênh, smoothing/lag, reconnect, bảo vệ dữ liệu; free plan có quota, không bảo đảm miễn phí mãi.
- Chỉ mở multiplayer **sau khi bản đơn máy ổn**.

---

## 11. THU THẬP DỮ LIỆU (ANALYTICS)

Log ẩn danh tối thiểu, `tester_id` ẩn danh, không ngày sinh thật, không dữ liệu cá nhân. Xin đồng ý dùng log khi mời thử.

| Event | Ý nghĩa | Loại |
|---|---|---|
| `entered_first_session` | Bắt đầu phiên đầu (ngày 0, giờ VN) | Chính |
| `returned_day7` | Vào lại game đúng ngày lịch thứ 7 | Chính |
| `completed_core_loop` | Đã vãn cảnh + công quả + xin xăm | Chính |
| `triggered_cat_event` | Gặp mèo chùa (1 lần/tester/phiên) | Phụ |
| `started_idle_zen_mode` | Bắt đầu Tịnh tâm rảnh tay | Phụ |
| `completed_idle_15m` | Đủ 15 phút không gián đoạn | Phụ |
| `viewed_lotus_stage` | Xem/ chăm sen; kèm `stage=bud/leaf/flower`, `day_since_first_use` | Phụ |
| log công quả / xin xăm | Hoàn thành từng hoạt động | Chính (cấu thành core loop) |

Phụ tức: không thay thế chỉ số chính (D7). Nếu thiếu log → **không tự nhận định**, ghi nguyên nhân lỗi riêng.

---

## 12. MÔ HÌNH KINH DOANH (SAU MVP)

**[CHỐT] nguyên tắc — [GT] giá cả, chi phí, nhu cầu mua**

| Tầng | Nội dung |
|---|---|
| Miễn phí | Vào chơi; vật phẩm & hoạt động cơ bản; xin xăm; lập lá số; luận giải **sơ bộ** |
| Có phí (vòng sau) | Luận giải tử vi **chi tiết** theo lần mua; giá chưa chốt, chưa kích hoạt trong MVP |
| Đường cấm | Không bán vật phẩm bằng tiền thật, không quyên góp tiền thật, không thanh toán trong MVP; cúng dường chỉ là hình thức ảo |

Câu hỏi kinh doanh chỉ mở **sau** khi có tín hiệu giữ chân (D7) — không thử doanh thu và giữ chân cùng lúc.

---

## 13. YÊU CẦU KỸ THUỤU

### 13.1. Stack đề xuất **[ĐỀ XUẤT]**

- **Godot 4 (GDScript)** xuất Android theo tài liệu chính thức; **Blender** dựng mô hình.
- Codex/Claude viết từng chức năng nhỏ; founder tự chạy và nghiệm thu trên máy thật.
- Cảnh nhỏ, ánh sáng nướng sẵn, vật thể tối ưu.

### 13.2. Hiệu năng mục tiêu

- **~30 FPS ổn định trên máy Android thử** (mục tiêu tự đặt, chưa phải chuẩn thị trường).
- Đo FPS/pin/nhiệt trên ≥2 máy Android thật: chế độ thường vs idle, cùng điều kiện, thời lượng gần nhau.
- API Godot liên quan (đã đối chiếu tài liệu chính thức): `DisplayServer.screen_set_keep_on`, `Engine.max_fps`, `Viewport.scaling_3d_scale`, `AudioStreamOggVorbis`.

### 13.3. Phân phối thử

- APK debug qua tải trực tiếp / Firebase App Distribution cho 15 tester.
- Google Play Internal Testing là hướng khả thi khác (không bắt buộc): phí Play Console 25 USD/lần + công tác tài khoản, xác minh, tuân thủ; tài khoản developer cá nhân mới cần closed test ≥12 người liên tục 14 ngày trước khi phát hành công khai.
- **Không phát hành công khai ở giai đoạn này.**

---

## 14. PHẠM VI MVP

### 14.1. Trong phạm vi **[CHỐT]**

- Một sân chùa, một chính điện nhỏ, một hồ sen, lối đi.
- Một kiểu nhân vật đồng nhất; camera thứ ba; điều khiển cảm ứng.
- 3 NPC có đường đi + thoại viết sẵn, nhận diện rõ là NPC.
- Đồng bộ tối thiểu 2–5 người thật/phòng; tự chạy offline khi mất server.
- 2 công quả (quét lá, chăm sen) + 1 nhang ảo miễn phí.
- Phước không giảm khi offline; Duyên lành có thể giảm; không thước đo đạo đức thật.
- Xin xăm miễn phí + diễn giải văn hóa ngắn; lá số mẫu không cần ngày sinh thật.
- Góc thiền, âm thanh êm, hồ sơ đơn giản.
- **3 bổ sung đã duyệt 30/10/2026:** mèo chùa (§5.3), Tịnh tâm rảnh tay v0 (§5.8), Sen Duyên Lành 7 ngày (§5.9).
- Log ẩn danh tối thiểu (bảng §11).

### 14.2. Ngoài phạm vi MVP **[CHỐT]**

- Thanh toán, bán báo cáo tử vi chi tiết, hệ thống tử vi đầy đủ, AI tạo nội dung thời gian thực.
- AI NPC hội thoại tự do, chatbot thầy tu, hàng trăm NPC, hàng chục khu vực, công cụ xây chùa.
- Chat mở cho người lạ, vật phẩm bán bằng tiền thật, quyên góp tiền thật, xếp hạng Phước.
- Android + iOS cùng lúc; không chốt engine cho dự án mở rộng.

### 14.3. Trì hoãn có chủ đích (chưa làm ở vòng này) **[CHỐT]**

Đêm Hoa Đăng D7 · 7 lá số mới · đài radio nhiều tập · kinh hành tự động · bốn chế độ treo máy · stream audio cloud · bảng thời trang "xỏ nhầm dép" · AI NPC tự do.

> Nếu sau này thêm Đêm Hoa Đăng D7: số liệu D7 khi đó đo "khả năng thu hút trở lại **có sự kiện**" — không được mô tả là sức giữ chân tự nhiên của cảnh tĩnh.

---

## 15. TIÊU CHÍ THÀNH CÔNG VÀ NGƯỠNG QUYẾT ĐỊNH

### 15.1. Hai cổng kiểm soát rủi ro (trước khi mời người thật) **[CHỐT]**

**Cổng A — Prototype đơn máy:**
- Đi lại, công quả, xin xăm, ngồi thiền chạy được.
- Mèo: hoàn thành công quả không tắc; 2 nút hoạt động.
- Idle: hẹn giờ 15 phút + khôi phục cài đặt khi thoát.
- Sen: lưu tiến trình qua restart + giả lập ngày (kiểm ngày 0/2/4/7).
- FPS đo trên ≥2 máy Android thật (~30 FPS mục tiêu).

**Cổng B — Online nhỏ:**
- 2 máy kết nối đồng thời, thấy nhau di chuyển.
- Server ngắt → vào được cảnh đơn máy; NPC minh bạch; không mất Phước do đồng bộ.

> Không đạt cổng A/B → chưa mời người thật.

### 15.2. Phép thử chính **[CHỐT]**

| Hạng mục | Giá trị |
|---|---|
| Tester | 15 người thật, 5/nhóm, chưa tham gia phát triển |
| Chỉ số chính | **Tỷ lệ quay lại D7** = số người vào lại ngày lịch thứ 7 / 15 người có phiên đầu hợp lệ |
| Ngày 0 | Thời điểm bắt đầu phiên đầu của từng người, giờ VN |
| Thu thập | Đủ 7 ngày theo từng người; tổng kết trong 10 ngày sau người cuối vào lần đầu |
| Mẫu số hợp lệ | Đã vào game/đi vào sân chùa lần đầu (không phải chỉ bấm xem quảng cáo) |

**Ngưỡng quyết định (đặt trước, không sửa sau khi xem kết quả):**

| Tín hiệu | Điều kiện |
|---|---|
| **Nên tiếp tục** | ≥6/15 quay lại D7 **và** mỗi nhóm có ≥1 người quay lại; ≥10/15 hoàn tất vòng; không có lỗi chặn toàn bộ |
| **Cần đổi hướng** | ≤2/15 quay lại D7 (đủ 15 người + log chính xác), hoặc lỗi chặn không khắc phục nổi trong ngân sách |
| **Chưa đủ bằng chứng**** | 3–5/15 quay lại; hoặc >5 nhưng một nhóm có 0; hoặc chưa đủ 15 người hợp lệ / log thiếu / không ổn |

Kèm 2 câu hỏi định tính sau phiên: "Điều gì muốn quay lại?" / "Điều gì khiến không muốn quay lại?" — không thay log D7. Ghi dấu người được nhắc/sự kiện D7 (nếu có) để không diễn giải nhầm.

### 15.3. Ngân sách thử **[CHỐT]**

| Khoản | Trần |
|---|---|
| Bản đơn máy + tài nguyên cần mua | ≤ 2.000.000 VND |
| Server / kiểm thử đồng bộ | ≤ 1.000.000 VND |
| Tuyển người thử, test, phát sinh | ≤ 1.000.000 VND |
| **Tổng được chi** | **≤ 4.000.000 VND** |
| Dự phòng giữ lại (không tự động chi) | 6.000.000 VND |

Điều kiện dừng: hết 4 triệu mà chưa có vòng chơi ổn trên điện thoại, hoặc không vượt cổng B → **giảm phạm vi**, không tự tăng quỹ, không giảm chuẩn đo lường. Nguồn lực founder: 6–8 giờ/ngày, chia mốc theo đầu ra, không hẹn ngày.

---

## 16. RỦI RO VÀ GIẢ THUYẾT

### 16.1. Ba giả thuyết rủi ro cao **[GT]**

1. **Giữ chân:** cả ba phân khúc sẽ tự nguyện quay lại thế giới chùa 3D → sai thì phần online + đầu tư 3D khó thu hồi.
2. **Thu phí:** một phần người dùng trả tiền đọc luận giải tử vi chi tiết, đủ lãi sau phí nền tảng/AI/vận hành → sai thì chưa đủ duy trì server.
3. **Vận hành:** 1 người + AI agents + ngân sách hạn đủ xây bản mobile 3D online nhỏ có NPC ổn định → sai thì vượt ngân sách/sức làm.

### 16.2. Rủi ro nội dung & giảm thiểu

| Rủi ro | Giảm thiểu |
|---|---|
| Nội dung đụng chạm tôn giáo | Hai vùng cảm xúc; không hài ở chính điện; founder duyệt toàn bộ thoại; không giễu nhại hình tượng |
| Trộn lẫn tử vi với giáo lý | Khu vực/diễn giải riêng; ghi giới hạn "chiêm nghiệm văn hóa" |
| NPC bị tưởng là người thật | Nhận dạng gắn trên đầu NPC; không AI hội thoại tự do |
| Thu thập dữ liệu nhạy cảm | Không lấy ngày sinh thật; log ẩn danh; xin đồng ý trước |
| Khẳng định kỹ thuật sai | Không công bố pin/FPS/hiệu năng khi chưa đo trên máy thật |
| Gian lận chỉnh đồng hồ (sen) | Ca kiểm thử chỉnh ngày được ghi nhận; chưa quảng bao chống gian lận production |
| Phình MVP | Mỗi thay đổi nhỏ, duyệt trước; danh sách "trì hoãn" ở §14.3 |

---

## 17. LỘ TRÌNH PHÁT TRIỂN (tác vụ kế tiếp — chưa thực hiện)

1. **Khởi tạo repo Godot 4** (`.gitignore`), sân chùa placeholder, di chuyển nhân vật + camera; đóng gói Android debug lên 2 máy.
2. **Vòng quét lá** chạy ổn → gắn mèo chùa + 2 lựa chọn; kiểm không mắc kẹt.
3. **Hồ sen + tương tác ngồi** → chế độ Tịnh tâm rảnh tay v0 (15 phút); đo trên 2 máy.
4. **Chậu sen 4 trạng thái** theo ngày + lưu nội bộ; kiểm ngày 0/2/4/7.
5. **Qua cổng A** → phòng online nhỏ 2–5 người → kiểm cổng B → mới mời tester.

Lệnh giao AI code đầu tiên (dự kiến): tạo dự án Godot 4 tối giản cho Android — scene sân chùa placeholder, `CharacterBody3D` điều khiển phím + cảm ứng, camera thứ ba, mục tiêu 30 FPS; mô tả cấu trúc file và bước kiểm thử trước; không multiplayer/thanh toán/UI phức tạp; sau mỗi thay đổi kèm hướng dẫn chạy trên điện thoại.

### Phân công người / AI (khung đề xuất)

| Hạng | Founder | AI agents | Nghiệm thu bắt buộc |
|---|---|---|---|
| Thiết kế trải nghiệm | Chọn phong cách, bố trí, nhịp chơi | Gợi ý luồng | Cảm giác yên bình; đủ 3 trụ cột |
| Mô hình 3D | Dựng/chỉnh bằng Blender | Checklist tối ưu, import | Bản quyền nguồn, đa giác, ánh sáng, chạy tốt Android |
| Điều khiển/UI | Trải nghiệm thử trên điện thoại | Codex/Claude viết từng chức năng | Không lỗi; thao tác tay tự nhiên |
| Online/NPC | Mở/đóng phòng, quan sát NPC | Kết nối + đường đi/thoại cố định | Không giả người; không lộ dữ liệu cá nhân |
| Nội dung Phật giáo/xăm | Viết, kiểm tôn trọng & giới hạn | Soạn mẫu, chuẩn hóa | Không trộn tử vi với giáo lý |
| Tử vi | Duyệt lá số mẫu | Dựng UI minh họa | Không thu ngày sinh thật |
| Test | Tiêu chí, mời người, xử lý phản hồi | Tổng hợp dữ liệu, log lỗi | Không tuyên bố kết quả khi thiếu mẫu/log |
| Kinh doanh | Duyệt chi, quyết định thu phí sau | Phân tích chi phí/biên | Chưa kích hoạt thanh toán |

Quy tắc giao AI: mỗi lần một thay đổi nhỏ có tiêu chí nghiệm thu cụ thể; **commit Git trước và sau**; founder tự chạy game, không tin "AI nói đã xong"; không đưa mật khẩu/khóa API vào prompt/commit.

---

## 18. PHỤ LỤC — TRẠNG THÁI PHÊ DUYỆT

| Mục | Trạng thái | Bằng chứng |
|---|---|---|
| Ba nhóm khách hàng ngang hàng | CHỐT | decision-20261029-02 |
| Ba trụ cột hài hòa | CHỐT | decision-20261029-03 |
| Miễn phí + luận giải chi tiết có phí; Phước/Duyên tách cơ chế | CHỐT | decision-20261029-04, -05 |
| MVP Android 15 người, ngân sách 4+6 triệu | CHỐT | decision-20261029-06 |
| Kênh tuyển: Facebook + TikTok đồng thời | CHỐT | decision-20261029-07 |
| 3 bổ sung (mèo, idle v0, sen 7 ngày) | CHỐT | decision-20261030-08 — "ừ chốt" |
| Ngưỡng D7 6/15, core loop 10/15 | CHỐT | experiment-plan.md |
| Engine Godot 4 + Blender | ĐỀ XUẤT | chưa chốt cho dài hạn |
| Tên game "Chốn An Nhiên" | TẠM | cần chốt tên chính thức sau |
| Nhu cầu giữ chân / thu phí / vận hành | GT | 6 assumptions — `unverified` |

**Hiện trạng chung:** đặc tả đã duyệt, **chưa có dòng code game nào, chưa có APK, chưa có tester.** Bước tiếp theo là dựng scene nguyên mẫu Godot và kiểm cổng A trên thiết bị thật.

---

## 19. THAY ĐỔI TÀI LIỆU

| Phiên bản | Ngày | Thay đổi |
|---|---|---|
| 1.0 | 2026-10-30 | Bản đầu tiên — tổng hợp toàn bộ thiết kế đã chốt tới 30/10/2026 (bao gồm 3 bổ sung duyệt cùng ngày) |
