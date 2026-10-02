---
name: ai-integration
description: Tích hợp AI (OpenAI/Gemini) để tạo Chatbot tra cứu và tóm tắt sách.
---
**Đầu vào:** `models.py`, các file routes, và yêu cầu AI.
**Đầu ra:** File `services/ai_service.py` và API endpoint mới cho Chatbot.

**Quy trình:**
1. Tạo hàm gọi API của LLM (OpenAI hoặc Gemini) trong `services/ai_service.py`.
2. Cấu hình Prompt Template: "Bạn là thủ thư AI. Chỉ trả lời thông tin dựa trên dữ liệu sách được cung cấp. Không bịa đặt tình trạng sách."
3. Tạo API `POST /chat` trong thư mục routes. Logic: Lấy câu hỏi -> Truy vấn CSDL tìm sách liên quan -> Gửi ngữ cảnh cho AI -> Trả kết quả.

**Quy tắc bảo vệ:**
- Không gửi thông tin cá nhân (password, số điện thoại) của độc giả cho AI.
- Phải dùng file `.env` để bảo mật API Key.