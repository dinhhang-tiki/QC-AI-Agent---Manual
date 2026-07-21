# Manual Testing Rules

Luật áp dụng **bắt buộc** cho mọi tác vụ sinh Manual Test Case trong dự án này (skill `rbt_manual_testing`, các slash command `/generate-*`).

## 1. Test Data

- CẤM dùng các mô tả chung chung (ví dụ: "Nhập email hợp lệ", "Nhập password sai", "Mã giảm giá hết hạn").
- BẮT BUỘC dùng dữ liệu cụ thể, mô phỏng thực tế (ví dụ: `test_user_01@domain.com`, `Abc@12345`, `EXPIRED_COUPON_2023`, `avatar_5mb.png`).

## 2. Test Steps

- Hành động nguyên tử (atomic), mỗi step chỉ 1 hành động.
- Ví dụ: "1. Nhập email: abc@test.com → 2. Nhập password: 123456 → 3. Click Đăng nhập".

## 3. Quy tắc bao phủ (Coverage)

Mỗi module phải đảm bảo quét đủ các lớp test sau:
1. Happy path
2. Negative
3. Boundary (giá trị biên)
4. Edge cases (trường hợp hiếm)
5. Security/Permission (phân quyền/bảo mật)
6. Validation (kiểm tra format, required fields)

## 4. Format đầu ra & Naming

- Định dạng xuất: bảng Markdown (ưu tiên) hoặc CSV/Excel khi user yêu cầu, phân tách bằng dấu phẩy (`,`).
- Header: `TC ID`, `Module`, `Risk Level`, `Test Scenario`, `Pre-Condition`, `Test Steps`, `Test Data`, `Expected Result`, `Priority`.
- Naming convention cho TC ID: `[TÊN_DỰ_ÁN]_[TÊN_MODULE]_TC_[SỐ_THỨ_TỰ_3_CHỮ_SỐ]` (ví dụ: `TIKI_LOGIN_TC_001`).
