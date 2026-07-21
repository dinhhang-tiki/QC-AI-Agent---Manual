---
name: generate-requirements-from-website
description: Sinh tài liệu Requirements từ website/module
---

# Sinh Requirements từ Website/Module

> **BẮT BUỘC:** Đọc skill `requirements_analyzer` tại `.cursor/skills/requirements_analyzer/SKILL.md` trước khi bắt đầu.

Workflow phân tích module/trang web và sinh tài liệu Yêu cầu (Requirements) chi tiết cho kiểm thử hoặc phát triển.

## Các bước thực hiện

1. **Tiếp nhận thông tin**
   - Đọc skill `requirements_analyzer` để nắm chuẩn đầu ra.
   - Lấy URL, tên module, mô tả/hình ảnh từ người dùng.
   - Hỏi thông tin đăng nhập hoặc trạng thái đặc biệt nếu cần.

2. **Khảo sát hệ thống**
   - Dùng browser tools/MCP hoặc `read_url_content` để truy cập module.
   - Inspect HTML, DOM, form, nút, thông báo lỗi.
   - Không đoán trường thông tin nếu không thấy trên UI thực tế.

3. **Phân tích chức năng**
   - User flows, trường tĩnh/động, quy tắc nghiệp vụ (mandatory, format, giới hạn ký tự).

4. **Biên soạn Requirements**
   - Tổng quan, Yêu cầu chức năng, Quy tắc trường dữ liệu, Luồng xử lý, Phi chức năng (nếu quan sát được).

5. **Trình bày**
   - Markdown, Tiếng Việt có dấu.
   - Xuất file `requirements_{module_name}.md` khi user yêu cầu.

## Ràng buộc

- Không dùng định dạng in đậm (`**`) trong nội dung tạo ra.
- Test Data và field phải lấy từ UI thực tế, không suy diễn.
