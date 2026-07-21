# Cấu trúc `.claude` cho QC AI Agent

Thư mục này cấu hình Claude Code để agent hiểu quy trình kiểm thử thủ công (Manual QC). Cấu trúc song song với [`.agent/`](../.agent/) (Antigravity) và [`.cursor/`](../.cursor/) (Cursor IDE), nhưng adapt theo chuẩn Claude Code.

## Cấu trúc

| Thư mục | Mục đích | Cách dùng trong Claude Code |
|---------|----------|------------------------------|
| `commands/` | Workflow step-by-step | Gõ `/` trong chat → chọn lệnh (vd: `/generate-manual-testcases`) |
| `skills/` | Kỹ năng chuyên biệt | Claude tự nạp khi phù hợp (dựa trên `description` trong `SKILL.md`), hoặc gõ `/tên-skill` |
| `rules/` | Quy tắc bắt buộc | Tài liệu tham chiếu — nội dung đã được lồng ghép trực tiếp vào skill/command tương ứng |

## Slash commands có sẵn

| Lệnh | Mô tả |
|------|-------|
| `/generate-requirements-from-website` | Sinh tài liệu Requirements từ website/module |
| `/generate-testcases-from-requirements` | Sinh test case nhanh (QUICK mode) từ requirements |
| `/generate-manual-testcases-rbt` | Sinh test case theo AI-RBT 6 bước (FULL mode) |
| `/generate-manual-testcases` | Luồng toàn trình: phân tích → Q&A → sinh test case RBT |

## Khác biệt so với `.agent/` và `.cursor/`

- Skill `generate_testcases` (ở `.agent/skills/` và `.cursor/skills/`) đã được **hợp nhất vào skill `rbt_manual_testing`** (kèm `references/test_design_techniques.md`) để tránh phân mảnh — Claude Code chỉ cần nạp 1 skill duy nhất cho toàn bộ quy trình FULL RBT.
- Các command và skill trỏ path nội bộ về `.claude/skills/...` (thay vì `.cursor/skills/...`), và có thêm phần `## Yêu cầu / requirements` với `$ARGUMENTS` để nhận input trực tiếp khi gọi slash command.

## Quan hệ với `.agent/` và `.cursor/`

Nội dung skills/rules được đồng bộ ý tưởng từ `.agent/` và `.cursor/`, nhưng đã adapt format cho Claude Code. Khi cập nhật quy tắc hoặc quy trình cốt lõi, nên cập nhật đồng thời ở cả 3 thư mục (`.agent/`, `.cursor/`, `.claude/`) để tránh lệch hành vi giữa các nền tảng.
