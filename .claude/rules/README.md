# Quy tắc hoạt động (`rules/`)

Thư mục này lưu các quy tắc **bắt buộc** mà Claude Code phải tuân theo khi thực hiện tác vụ manual testing trong dự án này. Khác với Cursor (`alwaysApply` trong `.mdc`), Claude Code không tự động nạp file trong `rules/` — các skill (`rbt_manual_testing`, `requirements_analyzer`) và slash command đã lồng ghép nội dung tương đương trực tiếp trong hướng dẫn của chúng. File ở đây đóng vai trò tài liệu tham chiếu tập trung, dùng để đối chiếu hoặc copy-paste khi cần nhắc lại luật cho agent.

## Danh sách quy tắc

- **`manual_testing_rules.md`**: Luật bắt buộc khi sinh Manual Test Case — quy tắc Test Data, Test Steps, Coverage (6 lớp test), Format đầu ra & Naming Convention cho TC ID.

Cấu trúc này đồng bộ với [`.agent/rules/`](../../.agent/rules/) và [`.cursor/rules/`](../../.cursor/rules/).
