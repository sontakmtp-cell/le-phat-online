# Le-Phat-online (Lễ Phật Online)

Dự án xây dựng **"Chốn An Nhiên"** — một không gian chùa Việt 3D trực tuyến trên Android, nơi người chơi chủ động đi lại, tham gia sinh hoạt chùa và khám phá văn hóa tâm linh, thay vì xem livestream một cách thụ động.

> Trạng thái hiện tại: **đã chốt định hướng thiết kế và phạm vi MVP, chưa lập trình game.** Giai đoạn đang chạy là `execution`.

## Cấu trúc thư mục

| Thư mục | Nội dung |
|---|---|
| `Docs/00-orchestrator/` | Tóm tắt phiên làm việc, điều phối tiến độ |
| `Docs/01-resource-audit/` | Kiểm kê nguồn lực hiện có |
| `Docs/02-niche-positioning/` | Phân tích ngách, chân dung người chơi mục tiêu |
| `Docs/03-value-proposition/` | Đề xuất giá trị theo từng nhóm người chơi |
| `Docs/04-business-model/` | Mô hình kinh doanh, giá, giả thuyết rủi ro |
| `Docs/05-mvp-design/` | Đặc tả MVP, kế hoạch thử nghiệm, phân chia việc người/máy |
| `Docs/06-conversion-loop/` | Kênh tiếp cận, nội dung, đường chuyển đổi |
| `Docs/execution/` | Đánh giá, bổ sung và nhiệm vụ phát triển kế tiếp |
| `Docs/game-design/` | **GDD** — tài liệu thiết kế trò chơi đầy đủ |
| `state/` | Trạng thái dự án dạng JSON (giai đoạn, quyết định, giả định) |

## Đọc từ đâu

1. `Docs/game-design/gdd.md` — bức tranh tổng thể về trò chơi.
2. `Docs/05-mvp-design/mvp-spec.md` — phạm vi MVP đã chốt (khi xung đột với GDD thì tài liệu này thắng).
3. `state/current-stage.json` — đang ở đâu, việc gì còn treo.

## Quy ước đánh dấu trong tài liệu

- **[CHỐT]** — đã được chủ dự án phê duyệt.
- **[ĐỀ XUẤT]** — hướng đưa ra, chưa duyệt.
- **[GT]** — giả thuyết, chưa kiểm chứng.
