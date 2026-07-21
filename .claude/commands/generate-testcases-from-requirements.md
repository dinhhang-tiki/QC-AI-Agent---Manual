---
description: Sinh test case nhanh (QUICK mode) từ requirements
---

# Sinh Manual Test Cases Nhanh (QUICK Mode)

> **BẮT BUỘC:** Đọc skill `rbt_manual_testing` tại `.claude/skills/rbt_manual_testing/SKILL.md`. Dùng **Mode QUICK**.

Sinh test cases nhanh từ requirements đã rõ ràng — một lượt, không chờ user giữa chừng.

## Nguyên tắc

- **Mode:** QUICK (1 lượt duy nhất)
- Phù hợp module đơn giản, requirements rõ
- Nếu requirements mơ hồ/phức tạp → đề xuất chuyển `/generate-manual-testcases-rbt`
- Output: **Tiếng Việt**

## Các bước

1. Đọc requirements user cung cấp
2. Xác định Happy Path, Negative, Boundary, Edge cases
3. Áp dụng EP, BVA, Decision Table, State Transition
4. Field-Level Validation: TC riêng cho **từng** trường input
5. Sinh test cases đầy đủ fields (TC ID, Module, Scenario, Pre-condition, Steps, Expected, Test Data, Priority)
6. Xuất bảng Markdown

## Bảng output

```
| TC ID | Module | Test Scenario | Pre-Condition | Test Steps | Test Data | Expected Result | Priority |
```

## Quy tắc

- Test Data cụ thể: `test_login_01@domain.com`, không placeholder
- TC ID: `[DỰ_ÁN]_[MODULE]_TC_[SỐ]`
- Bao gồm Positive, Negative, Boundary, Edge cases

## Yêu cầu / requirements

$ARGUMENTS
