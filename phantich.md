# Phần 1. Phân tích hệ thống Smart Farm

## 1. Xác định Input và Output của hệ thống
- **Input (Dữ liệu đầu vào):**
  - Tín hiệu đo lường nhiệt độ và độ ẩm không khí từ cảm biến môi trường.
  - Tín hiệu đo độ ẩm đất từ cảm biến cắm tại gốc các chậu lan.
  - Trạng thái nguồn điện và thông số phản hồi từ thiết bị máy bơm.
- **Output (Tín hiệu đầu ra):**
  - Lệnh kích hoạt/ngắt Rơ-le (Relay) để điều khiển máy bơm nước và hệ thống phun sương.
  - Thông báo trạng thái vận hành và cảnh báo sự cố gửi về ứng dụng quản lý của người nông dân.
  - Nhật ký (log) dữ liệu lưu trữ lịch sử vận hành hệ thống.

## 2. Sơ đồ phối hợp phần cứng hệ thống Smart Farm
- **Cảm biến (Input):** Đo đạc dữ liệu môi trường thực tế (Nhiệt độ, Độ ẩm) ➔ Chuyển tín hiệu về Vi xử lý.
- **Bộ xử lý trung tâm (SoC/CPU):** Tiếp nhận dữ liệu ➔ Phân tích, so sánh với ngưỡng cài đặt ➔ Quyết định ra lệnh điều khiển.
- **Thiết bị chấp hành (Output):** Bộ điều khiển Rơ-le nhận lệnh từ CPU ➔ Đóng/ngắt nguồn điện ➔ Bật/tắt Máy bơm tưới Lan.

---
