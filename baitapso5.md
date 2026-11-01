# BÁO CÁO MẪU GIAO TIẾP BẤT ĐỒNG BỘ & LỊCH TRÌNH LÊN LỊCH GỬI (ASYNC COMMUNICATION)
> **Dự án:** Quản lý Giao tiếp Bất đồng bộ Doanh nghiệp  
---

## 1. Tin nhắn mẫu theo Phong cách Asynchronous Communication

Áp dụng quy tắc **Tránh lỗi No-Hello**, gộp toàn bộ bối cảnh, lỗi chi tiết, hướng xử lý và tài liệu đính kèm vào **01 tin nhắn duy nhất** để đồng đội ở múi giờ khác có đủ thông tin xử lý ngay khi mở máy mà không cần hỏi lại:

```text
[URGENT / FIX BUG] Yêu cầu hỗ trợ xử lý lỗi API Authentication trên hệ thống Staging

Chào [Tên Đồng Đội],

1. Bối cảnh & Hiện trạng:
Hệ thống Staging đang gặp lỗi 500 khi người dùng thực hiện đăng nhập qua Google OAuth. Lỗi này làm nghẽn luồng kiểm thử tính năng mới của nhóm Tester.

2. Môi trường & Chi tiết lỗi:
- Environment: Staging (v1.2.4)
- Endpoint bị lỗi: POST /api/v1/auth/google
- Error Logs: "Token Verification Failed - Invalid Signature (Code: 50012)"
- Ảnh chụp màn hình & File Log: [https://drive.google.com/drive/folders/sample-log-id](https://drive.google.com/drive/folders/sample-log-id)

3. Hướng nghi vấn & Đề xuất giải pháp:
Có thể Secret Key của OAuth trên môi trường Staging đã bị hết hạn hoặc lệch cấu hình `.env` sau đợt Deploy tối qua.

4. Yêu cầu hỗ trợ (Call to Action):
Nhờ bạn kiểm tra lại cấu hình Secret Key trên Server Staging và cập nhật lại file `.env` giúp nhóm. 

Cảm ơn bạn rất nhiều! Bạn cứ thư thả kiểm tra và phản hồi lại kết quả qua Thread này khi bắt đầu ca làm việc nhé.
