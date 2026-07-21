# Cấu trúc `.cursor` cho QC AI Agent

Thư mục này cấu hình Cursor IDE để agent hiểu quy trình kiểm thử thủ công (Manual QC). Cấu trúc song song với `.agent/` (dùng cho Antigravity) nhưng theo chuẩn Cursor.

## Cấu trúc

| Thư mục | Mục đích | Cách dùng trong Cursor |
|---------|----------|------------------------|
| `commands/` | Workflow step-by-step | Gõ `/` trong Agent chat → chọn lệnh (vd: `/generate-manual-testcases`) |
| `skills/` | Kỹ năng chuyên biệt | Agent tự nạp khi phù hợp, hoặc gõ `/tên-skill` / `@skill` |
| `rules/` | Quy tắc bắt buộc | Tự áp dụng theo `alwaysApply` hoặc glob pattern |

## Slash commands có sẵn

| Lệnh | Mô tả |
|------|-------|
| `/generate-requirements-from-website` | Sinh tài liệu Requirements từ website/module |
| `/generate-testcases-from-requirements` | Sinh test case nhanh (QUICK mode) từ requirements |
| `/generate-manual-testcases-rbt` | Sinh test case theo AI-RBT 6 bước (FULL mode) |
| `/generate-manual-testcases` | Luồng toàn trình: phân tích → Q&A → sinh test case RBT |

## Ví dụ sử dụng

```
/generate-requirements-from-website

URL: https://example.com/login
Module: Đăng nhập
Email: test@example.com / Password: Abc@12345
```

```
/generate-manual-testcases-rbt

Dự án: Loyalty Program
Đính kèm: @requirements_loyalty.md
```

## Quan hệ với `.agent/`

- `.agent/` — cấu trúc gốc (Antigravity / slash command khác)
- `.cursor/` — bản tương thích Cursor (commands, skills, rules)

Nội dung skills được đồng bộ từ `.agent/skills/`. Khi cập nhật skill, nên cập nhật cả hai thư mục hoặc chỉ `.cursor/skills/` nếu chỉ dùng Cursor.

## Lưu ý workspace

Cursor chỉ quét `.cursor/commands/` ở **thư mục workspace root** (folder bạn mở trong Cursor).

- Mở trực tiếp `QC-AI-Agent---Manual-main` → commands trong folder này sẽ hiện.
- Mở folder cha `AI Agent` → cần có thêm `AI Agent/.cursor/commands/` (đã symlink tới các file ở đây).

Sau khi thêm/sửa commands: **Cmd+Q** thoát hẳn Cursor rồi mở lại, hoặc chạy `Developer: Reload Window`.
