# 📊 BÁO CÁO THU HOẠCH NGHIỆM THU BÀI LAB 3 (BƯỚC 3 — SUBMISSION ARTIFACT)

> **Họ và Tên Học viên:** Đỗ Quang Vinh
> **Mã Sinh Viên / Mã Học viên:** 2A202602989
> **Chủ đề Lựa chọn:** Trợ lý Học vụ & Tra cứu Lịch thi VinUni  

---

## 1. BẢNG CHẤM ĐIỂM AGENTIC FIT SCORING MATRIX (ĐÁNH GIÁ CHỦ ĐỀ)

| Tiêu chí Đánh giá | Mức độ (1 - 5) | Giải trình chi tiết lý do chọn điểm |
| :--- | :---: | :--- |
| **1. Multi-step Reasoning** | 4 / 5 | Agent cần thực hiện nhiều bước nối tiếp: tra cứu GPA → kiểm tra lịch thi → nếu sinh viên cần hỗ trợ thì đặt lịch tư vấn với cố vấn học vụ |
| **2. Tool Interaction** | 5 / 5 | Cần gọi ít nhất 2 công cụ: tool tra cứu điểm/lịch thi (academic_query) và tool đặt lịch hẹn với cố vấn (booking_advisor) |
| **3. Dynamic Decision** | 4 / 5 | Agent phải tự quyết định bước tiếp theo dựa trên kết quả tra cứu (ví dụ: nếu GPA thấp hơn ngưỡng thì đề xuất đặt lịch tư vấn, nếu không thì chỉ trả kết quả tra cứu) |
| **4. Long Horizon Goal** | 3 / 5 | Mục tiêu xuyên suốt là hỗ trợ sinh viên hoàn tất cả tra cứu lẫn đặt lịch trong một phiên làm việc liên tục |
| **TỔNG ĐIỂM AGENTIC FIT** | **16 / 20** | Vượt ngưỡng 12/20 → phù hợp triển khai Agentic System |

---

## 2. TRÍCH XUẤT KẾT QUẢ WATERFALL TRACE LOG (SAU KHI CHẠY TEST SUITE TRÊN API THẬT)

> ⚠️ **YÊU CẦU NGHIỆM THU:** Mở tệp `.env` điền `GEMINI_API_KEY` (hoặc `OPENAI_API_KEY`) để kết nối LLM thật trước khi thực thi `python src/app.py --all`. Bài nộp chỉ dùng Mock Offline Provider sẽ không đạt điểm nghiệm thực tế.

Dán 1 đoạn trích xuất log tiêu biểu từ file `docs/trace_waterfall.json` sinh ra từ phản hồi LLM API thật:

```json
[
  {
    "step": 1,
    "action_type": "TOOL_EXECUTION",
    "tool_name": "academic_query",
    "arguments": {
      "student_id": "SV2026001"
    },
    "observation": {
      "status": "SUCCESS",
      "student_id": "SV2026001",
      "data": {
        "full_name": "Nguyễn Văn An",
        "gpa": 3.85
      }
    },
    "latency_ms": 120.5
  }
]
```

---

## 3. TỔNG KẾT KẾT QUẢ NGHIỆM THU & NỘP BÀI

- [ ] Đã điền API Key thật trong `.env` và xác nhận Agent chạy mượt mà trên LLM API thật (Gemini/OpenAI).
- **Tổng số Test Cases đã chạy thành công:** ___ / 5 test cases.
- **Số lượt gọi Tool qua MCP Server chính xác:** ___ lượt.
- **Kết quả đẩy Repo nộp bài:** [ ] Đã Commit và Push mã nguồn thành công lên GitHub cá nhân.

---

> ✅ **HOÀN TẤT NỘP BÀI:** Sao chép đường link GitHub Repository cá nhân của bạn và dán vào ô nộp bài trên hệ thống LMS VLearn để hoàn tất Bài Lab 3!
