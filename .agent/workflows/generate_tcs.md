---
description: generate_tcs
---

# TRIGGER: /generate_tcs

# INPUT REQURED:
- system_type (Web / Mobile / API)
- module_name
- project_name
- requirement_source 

# WORKFLOW STEPS:

## Step 1: Phân tích luồng (Analysis)
Sử dụng `requirements_analyzer_skill`. Đọc `requirement_source` và bóc tách thành 3 danh sách: Happy Path, Alternate Path, Exception Path.

## Step 2: Tìm điểm mờ & Q&A (PAUSE)
Dùng `requirements_analyzer_skill` để phát hiện Ambiguities.
- In ra danh sách các luồng ở Step 1.
- In ra danh sách câu hỏi Q&A.
- [STOP] Dừng Workflow, yêu cầu người dùng trả lời để làm rõ requirement.

## Step 3: Đánh giá Rủi ro (Risk Assessment)
Dùng `requirements_analyzer_skill`. Dựa trên xác nhận ở Step 2, gán nhãn Risk Level (High/Medium/Low) và số lượng Test Case dự kiến.

## Step 4: Tạo Test Case
Kích hoạt `generate_testcases_skill` và áp dụng NGHIÊM NGẶT rule `manual_testcases_rule`.
Tạo bảng Test Case đầy đủ dựa trên requirement đã chốt.

## Step 5: Xuất File
Tạo file `testcases_[module_name].csv` theo đúng định dạng CSV yêu cầu trong Rule.
Ghi dữ liệu, lưu file và thông báo hoàn tất.