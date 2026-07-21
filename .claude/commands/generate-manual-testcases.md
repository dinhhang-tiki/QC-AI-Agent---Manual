---
description: Luồng toàn trình phân tích, Q&A và sinh test case RBT
---

# Sinh Manual Test Cases Toàn Trình (FULL RBT + Human-in-the-loop)

> **BẮT BUỘC:** Đọc 2 skills trước khi bắt đầu:
> - `.claude/skills/requirements_analyzer/SKILL.md`
> - `.claude/skills/rbt_manual_testing/SKILL.md`

Workflow điều phối kiểm thử thủ công từ A-Z: làm rõ requirement trước khi sinh test case.

## Nguyên tắc

- **Mode:** FULL — nhiều bước, **bắt buộc dừng** chờ user
- **Ngôn ngữ:** Tiếng Việt
- Không suy diễn logic nghiệp vụ thiếu — phải Q&A

## Các bước

### Bước 1: Phân tích yêu cầu
- Skill `requirements_analyzer`
- Trích xuất Happy Path, Alternate Path, Exception Path

### Bước 2: Xác nhận (Human-in-the-loop)
- In danh sách câu hỏi Q&A / cần làm rõ
- **[PAUSE — BẮT BUỘC]**
- Hỏi: *"Bạn muốn làm rõ Q&A trước, hay sinh test case theo giả định hiện tại?"*
- **Không chuyển Bước 3 nếu user chưa phản hồi**

### Bước 3: Đánh giá rủi ro & kỹ thuật
- Skill `rbt_manual_testing` (Mode FULL RBT)
- Risk Level (High/Medium/Low)
- EP, BVA, Decision Table, State Transition

### Bước 4: Sinh Test Case
- Bảng ISTQB đầy đủ fields
- Test Data cụ thể: `test_user_01@domain.com`, `Abc@12345`
- Xuất bảng Markdown (đề xuất `.xlsx` nếu user cần file)

## Bảng output

```
| TC ID | Module | Risk Level | Test Scenario | Pre-Condition | Test Steps | Test Data | Expected Result | Priority |
```

- TC ID: `{project_name}_{module_name}_TC_001`

## Yêu cầu / requirements

$ARGUMENTS
