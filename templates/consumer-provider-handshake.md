# Consumer-Provider Handshake

**Nhóm / Service:** Team 10 / Access Gate (Consumer) & Core Policy (Provider)

## 1. Xác nhận Contract
- Đã chạy spectral linter không có lỗi severity error.
- Thống nhất các response lỗi theo format ProblemDetails.
- Thống nhất cách xử lý idempotency-key.

## 2. Xác nhận Mock Testing
- Provider (Core Policy) đã cung cấp `openapi.yaml` chính xác, có chứa properties và example.
- Consumer (Access Gate) đã viết smoke test gọi thành công Mock server của Provider.
- Token xác thực giả lập đã được thống nhất là gửi qua header `Authorization: Bearer mock-token`.

## 3. Quyết định kỹ thuật
- Nếu Provider sập/timeout, Consumer sẽ mở cổng bằng bộ rules fallback cục bộ (đã chốt ở Lab 2).
- Giới hạn tải: Access Gate có thể chịu 100 quẹt/giây.

## Chữ ký
- **Provider (Đại diện):** Lê Minh Hiếu
- **Consumer (Đại diện):** Lê Minh Hiếu
- **Witness (Trợ giảng / Giảng viên):** ___________________
