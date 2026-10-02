---
name: database-design
description: Thiết kế cơ sở dữ liệu cho hệ thống quản lý thư viện dựa trên tài liệu yêu cầu.
---
**Đầu vào:** File `docs/requirements.md` (hoặc `docs/customer-requirement.md`)
**Đầu ra:** Mã SQL tạo bảng và Sơ đồ thực thể liên kết (ERD).

**Quy trình thực hiện:**
1. Phân tích tài liệu yêu cầu để xác định các thực thể chính. Bắt buộc phải có: Sách (Books), Độc giả (Readers), Phiếu mượn/trả (Borrow_Records).
2. Thiết kế các trường dữ liệu (columns), kiểu dữ liệu và ràng buộc cho từng bảng. Chú ý các trường quan trọng: số lượng sách còn lại, ngày mượn, hạn trả, tiền phạt quá hạn.
3. Thiết lập Khóa chính (Primary Key) và Khóa ngoại (Foreign Key) giữa các bảng.
4. Sinh ra mã SQL (chuẩn MySQL/PostgreSQL) để tạo các bảng này (CREATE TABLE).
5. Sinh ra mã Mermaid (Mermaid.js) để vẽ sơ đồ ERD.

**Quy tắc bảo vệ (Guardrails):**
- Chỉ được sinh ra mã SQL và mã sơ đồ ERD. Tuyệt đối KHÔNG viết code Python/FastAPI ở bước này.
- Các bảng phải tuân thủ chuẩn hóa cơ sở dữ liệu (Normalization).
- Mật khẩu của người dùng/độc giả phải được lưu trữ dưới dạng băm (hashed).