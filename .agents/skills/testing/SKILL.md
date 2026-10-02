---
name: testing
description: Viết và chạy Unit Test cho các API bằng Pytest.
---
**Đầu vào:** `main.py` và các file trong thư mục `routes/`.
**Đầu ra:** File `test_main.py`.

**Quy trình:**
1. Tạo file `test_main.py` tại thư mục gốc.
2. Dùng `TestClient` của FastAPI để viết test case cho các đường dẫn chính.
3. Chạy lệnh `pytest` để kiểm tra.