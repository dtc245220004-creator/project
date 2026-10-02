---
name: implementation
description: Sinh mã nguồn Backend (FastAPI/Python) dựa trên thiết kế cơ sở dữ liệu và yêu cầu.
---
**Đầu vào:** `docs/requirements.md` và `database/schema.sql`.
**Đầu ra:** Mã nguồn Python.

**Quy trình:**
1. Đọc kỹ cấu trúc bảng trong `schema.sql`.
2. Tạo file `models.py` chứa các class SQLAlchemy tương ứng với các bảng.
3. Tạo file `database.py` chứa cấu hình kết nối CSDL.
4. Tạo các API Endpoints trong thư mục `routes/` (ví dụ: `books.py`, `readers.py`, `borrow.py`) thực hiện CRUD và logic mượn/trả.
5. Tạo file `main.py` để khởi tạo ứng dụng FastAPI và đăng ký (include) các routes.

**Quy tắc bảo vệ:**
- Chỉ viết code Backend quản lý, CHƯA tích hợp chatbot AI ở bước này.
- Logic mượn sách phải trừ số lượng sách còn lại trong kho.