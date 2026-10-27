# Phần 2. Nội dung file README.md

```markdown
# 🚀 Hệ Thống Giám Sát & Tưới Tự Động Cho Trang Trại Lan (Smart-Farm)

*Hệ thống IoT thông minh giúp tự động hóa quy trình chăm sóc, giám sát nhiệt độ và điều khiển tưới tiêu tối ưu cho trang trại Lan.*

---

## 1. Hướng dẫn cài đặt và cấu hình

Chạy các câu lệnh sau trên Terminal để cài đặt môi trường và các thư viện phụ thuộc:

```bash
# Cập nhật hệ thống và cài đặt Python
sudo apt update && sudo apt install python3-pip -y

# Cài đặt các thư viện kết nối cảm biến và MQTT
pip install Adafruit-DHT paho-mqtt requests


-------------
CẬP NHẬT
## 7. Lưu ý quan trọng (Handling & Maintenance)

> ⚠️ **CẢNH BÁO VỀ BỘ NHỚ RAM & NHẬT KÝ VẬN HÀNH:**
> 
> Trong quá trình hệ thống Smart Farm chạy liên tục 24/7, tệp ghi nhật ký (Log file) có thể phình to làm chiếm dụng bộ nhớ RAM của vi điều khiển, dẫn đến nguy cơ hệ thống bị treo hoặc phản hồi chậm.
> 
> **Quy trình xử lý an toàn:**
> 1. **Cơ chế tự động:** Hệ thống đã được cấu hình tự động đẩy (backup) nhật ký cũ lên Cloud và giải phóng bộ nhớ đệm (Cache) vào lúc 00:00 mỗi ngày.
> 2. **Giải phóng RAM thủ công (khi sự cố xảy ra):**
>    - Mở Terminal và kiểm tra dung lượng RAM: `free -h`
>    - Thực hiện xóa bộ nhớ đệm an toàn mà không cần khởi động lại máy bằng lệnh:
>      ```bash
>      sudo sync && echo 3 | sudo tee /proc/sys/vm/drop_caches
>      ```
> 3. **Lưu ý an toàn:** Tuyệt đối **không ngắt nguồn điện đột ngột** khi RAM đang đầy để tránh làm hỏng thẻ nhớ (MicroSD) và mất dữ liệu lịch sử tưới tiêu.
