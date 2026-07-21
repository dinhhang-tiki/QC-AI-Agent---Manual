# Cấu trúc Thư mục `.agent`

Thư mục này chứa các thiết lập, quy tắc, kỹ năng và kịch bản hoạt động dành cho AI Agent phục vụ dự án kiểm thử tự động (QC AI Agent).

## Cấu trúc chi tiết

- **`rules/`**: Chứa các quy tắc bắt buộc AI phải tuân thủ nghiêm ngặt trong suốt quá trình làm việc với dự án (ví dụ: quy chuẩn đặt tên test case, quy tắc viết code Playwright, Cypress, v.v.).
- **`skills/`**: Định nghĩa các kỹ năng chuyên biệt mà AI Agent có thể sử dụng (ví dụ: phân tích test case, tự động sinh code page object, tối ưu hóa locator, v.v.).
- **`workflows/`**: Chứa các kịch bản thực thi step-by-step dưới dạng slash commands hoặc luồng làm việc tự động (ví dụ: sinh mã kiểm thử từ mô tả tiếng Việt, tạo pull request tự động, v.v.).

---
*Tài liệu này được tạo tự động bởi Antigravity.*
