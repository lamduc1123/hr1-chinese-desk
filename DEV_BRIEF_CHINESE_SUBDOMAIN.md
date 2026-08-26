# 📋 TECHNICAL BRIEF: SUBDOMAIN CHINESE DESK (`chinese.hr1vietnam.com`)

* **Dự án:** Xây dựng Subdomain / Landing Page phục vụ thị trường khách hàng & ứng viên Tiếng Trung của HR1Vietnam.
* **Tên miền dự kiến:** `chinese.hr1vietnam.com` (Tương tự `education.hr1vietnam.com`).
* **Định vị:** Tinh gọn, tối ưu chuyển đổi B2B (Doanh nghiệp FDI Trung Quốc/Đài Loan) và B2C (Ứng viên tiếng Trung).

---

## 🎯 DANH SÁCH HẠNG MỤC YÊU CẦU DÀNH CHO TEAM DEV

Để giảm thiểu tối đa khối lượng công việc cho Team DEV, các yêu cầu kỹ thuật được tinh gọn vào các nhiệm vụ chính sau:

---

### 1. Cấu hình Tên miền & DNS (Subdomain Routing)
* **Nhiệm vụ:**
  * Cấu hình DNS trỏ subdomain `chinese.hr1vietnam.com` về Hosting / Server chứa source Landing Page (hoặc CNAME trỏ về nền tảng dựng trang như Webflow/WordPress/Ladipage nếu dựng riêng).
  * Cài đặt chứng chỉ bảo mật **SSL (HTTPS)** cho subdomain.

---

### 2. Cung cấp API / Job Widget (Lọc Job Tiếng Trung)
Hiện tại website chính đã có chức năng tìm kiếm job tiếng Trung qua URL:
* `https://hr1vietnam.com/tim-viec?keywords=ti%E1%BA%BFng+trung`
* `https://hr1vietnam.com/search-job?keywords=chinese`

👉 **Yêu cầu kỹ thuật (Dev chọn 1 trong 2 phương án thuận tiện nhất):**

* **Phương án A (Khuyên dùng - REST API nhẹ):**
  * Dev cung cấp 1 API Endpoint: `GET /api/v1/jobs?keyword=chinese&limit=10&page=1`
  * Trả về danh sách JSON gồm các trường:
    ```json
    [
      {
        "id": "123",
        "title": "Phiên Dịch Tiếng Trung",
        "salary": "12 - 20 Triệu VND",
        "location": "Đồng Nai",
        "industry": "Electrical/Electronics Manufacturing",
        "tags": ["Chinese", "Translation"],
        "updated_at": "2026-08-20",
        "detail_url": "https://hr1vietnam.com/job/phien-dich-tieng-trung-123"
      }
    ]
    ```
* **Phương án B (Widget Iframe / JS Script nhúng):**
  * Nếu không xuất API, Dev đóng gói 1 đoạn script hoặc iframe nhúng hiển thị danh sách job đã được lọc sẵn từ khóa `Tiếng Trung` / `Chinese`.
  * Khi người dùng click vào thẻ Job, hệ thống tự động mở sang tab mới (`target="_blank"`) trỏ về trang chi tiết gốc trên website `hr1vietnam.com`.

---

### 3. Xử lý Dịch tự động sang Tiếng Trung (Client-side Translation)
* Để không phải can thiệp sửa đổi cấu trúc dữ liệu tiếng Việt/Anh trong CRM gốc:
* Frontend của `chinese.hr1vietnam.com` sẽ nhúng **Script dịch tự động phía trình duyệt** (ví dụ: Google Website Translator widget hoặc script JS dịch tự động các nội dung động từ API/Widget sang `zh-CN` - Tiếng Trung Giản thể).
* *Dev chỉ cần đảm bảo các thẻ Job render có class/id HTML rõ ràng để script dịch dễ nhận diện.*

---

### 4. Tiếp nhận Form Liên hệ B2B (Lead Capture)
* Trên trang sẽ có 1 Form gửi yêu cầu tuyển dụng của khách hàng doanh nghiệp Trung Quốc.
* **Nhiệm vụ:** Form khi submit sẽ gửi thông tin (Tên công ty, Người liên hệ, SĐT/WeChat, Vị trí cần tuyển, Địa điểm) về:
  * Email nội bộ phụ trách: `china.desk@hr1vietnam.com` (hoặc Webhook đẩy vào CRM hiện tại của HR1VN).

---

## ⏱️ OUTPUT MONG ĐỢI TỪ TEAM DEV
1. Xác nhận trỏ DNS `chinese.hr1vietnam.com`.
2. Endpoint API Job (hoặc Script Widget nhúng) kèm tài liệu mẫu data trả về.
3. Hướng dẫn kết nối Form submit B2B về Email/CRM.
