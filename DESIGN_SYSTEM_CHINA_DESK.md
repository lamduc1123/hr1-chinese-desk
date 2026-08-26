# 🎨 DESIGN GUIDELINE: HR1VIETNAM CHINA DESK (`chinese.hr1vietnam.com`)
*Đồng bộ 100% với Design System của HR1 Education Hub (`education.hr1vietnam.com`)*

---

## 1. Creative Formula & Triết lý Thiết kế

```
HR1 Editorial Atlas Foundation (Nền tảng Tạp chí Hàn lâm)
+ HR1 Red Brand Core (#B11116)
+ China Desk Headhunting & FDI Sourcing Authority
+ Sharp Editorial Typography (Be Vietnam Pro + Noto Sans SC + Lora Serif)
+ Brutalist Hard-Shadow Interactions (Đổ bóng cứng 7px/12px/22px Ink Navy)
```

---

## 2. Bảng màu chuẩn thương hiệu (Color Palette)

| Mã màu | Tên gọi | Giá trị HEX | Vai trò trên giao diện |
| :--- | :--- | :--- | :--- |
| **HR1 Red** | Màu chủ đạo | `#B11116` | Nút bấm chính, viền active, icon highlight, accent serif |
| **Deep Red** | Đỏ đậm | `#892226` | Top site ribbon, shadow nền media, tag chuyên sâu |
| **Warm Paper** | Nền giấy ngà | `#F7F4EE` | Màu nền chính toàn trang (đặc trưng Education Hub) |
| **Paper 2** | Nền thẻ phụ | `#EEE9DF` | Nền các thẻ phụ, viền hover, card thứ cấp |
| **Ink Navy** | Xanh đen mực | `#101828` | Chữ tiêu đề chính, khối Dark section, màu đổ bóng cứng |
| **Graphite** | Xám đậm | `#20242C` | Đoạn văn bản mô tả chính |
| **Muted** | Xám trung tính | `#667085` | Chú thích phụ, metadata ngày đăng, tag nhỏ |
| **Line** | Đường kẻ viền | `rgba(16,24,40,.16)` | Viền chia section, viền header, viền ô lưới |

> 🚫 **Nguyên tắc:** Tuyệt đối không dùng gradient tím/neon/cyan công nghệ, không bo tròn quá đà (chủ yếu dùng góc vuông sắc nét hoặc bo nhẹ `rounded-none / rounded-sm` kết hợp bóng cứng).

---

## 3. Kiểu chữ & Typography

- **Phông chữ không chân (Sans):** `Be Vietnam Pro` (kết hợp `Noto Sans SC` cho ký tự tiếng Trung).
- **Phông chữ có chân điểm nhấn (Serif Accent):** `Lora` (Dùng cho các từ khóa cảm xúc, con số thống kê lớn).
- **Section Label / Micro Label:** Uppercase + tracking rộng (`letter-spacing: .18em`) có thanh gạch ngang đỏ phía trước `--`.
- **Section Index Motif:** Số thứ tự La Mã/Ả Rập kích thước khổng lồ phong cách Outline Serif (`-webkit-text-stroke: 1px var(--red); font-family: 'Lora'`).

---

## 4. Các Signature UI Elements được thừa hưởng từ Education Hub

1. **Site Ribbon (Dải băng trên cùng):** Nền `#892226` chữ trắng hoa tinh tế.
2. **Hero Rail (Ray chữ dọc bên trái mép trang):** `CHINA DESK → TALENT HUB • HR1 • 2026`.
3. **Metric Strip:** Băng số liệu 4 cột chạy ngang với font số Lora Serif lớn và hiệu ứng count-up.
4. **Kinetic Marquee:** Dải băng chữ chạy vô tận màu đỏ HR1 (`EXECUTIVE SEARCH • FACTORY RPO • BILINGUAL TALENT...`).
5. **Brutalist Buttons & Cards:** Khi hover nút hoặc card sẽ nhấc lên `-5px` và đổ bóng cứng `box-shadow: 7px 7px 0 var(--ink)`.
6. **Optimized Job Cards:** Bố trí theo hệ lưới editorial, thẻ tag tối giản, nút xem chi tiết dẫn về link gốc.
7. **WeChat QR Modal & Direct Lead Capture:** Form tư vấn phong cách hồ sơ chuyên nghiệp.
