---
description: Sinh test case theo AI-RBT 6 bước (FULL mode)
---

# Sinh Manual Test Cases — AI-RBT FULL (6 bước)

> **BẮT BUỘC:** Đọc `.claude/skills/rbt_manual_testing/SKILL.md` (Mode FULL RBT) trước khi bắt đầu.

Quy trình **AI-RBT** 6 bước tuần tự từ tài liệu yêu cầu.

## Nguyên tắc

- **Mode:** FULL RBT — chạy tuần tự, không gộp bước
- **DỪNG** chờ user tại Bước 2 (Q&A) và Bước 4 (Review Scenarios)
- Chưa có requirements → hỏi user trước
- Output: **Tiếng Việt**

## Các bước (theo skill `rbt_manual_testing` → Mode FULL RBT)

### Bước 1: Khởi tạo ngữ cảnh
- Thu thập tên dự án, mô tả hệ thống, MVP, tài liệu yêu cầu
- Xác nhận hiểu bối cảnh → chờ user → Bước 2

### Bước 2: Phân tích & Q&A
- Happy / Alternate / Exception paths
- Ambiguities → câu hỏi Q1, Q2... kèm assumption
- **[PAUSE]** Chờ user trả lời → Bước 3

### Bước 3: Phân rã hệ thống
- Modules / Sub-modules, dependencies

### Bước 4: Traceability
- Map Module → REQ-01, REQ-02...
- Gap analysis, High-Level Scenarios
- **[PAUSE]** Chờ user review → Bước 5

### Bước 5: Sinh Test Case (RBT)
- Risk Level (High/Medium/Low) per module
- EP, BVA, Decision Table, State Transition
- Field-Level Validation: TC riêng từng trường
- Test Data cụ thể, không placeholder

### Bước 6: Chuẩn hóa
- Bảng: `| TC ID | Module | Risk Level | Test Title | Pre-Condition | Test Steps | Expected Result | Priority | Test Data |`
- Traceability Matrix + Ambiguities đã giải quyết

## Yêu cầu / requirements

$ARGUMENTS
