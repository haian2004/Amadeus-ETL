# 🛫 Dự án Amadeus-ETL: Quy trình ETL cho dữ liệu du lịch bằng SSIS

**Amadeus-ETL** là một dự án mô phỏng quy trình **ETL (Extract – Transform – Load)** sử dụng công cụ **SQL Server Integration Services (SSIS)**. Dự án được thiết kế để minh họa cách dữ liệu (giả lập từ hệ thống như Amadeus) được trích xuất, biến đổi và nạp vào kho dữ liệu phục vụ phân tích.

---

## 📁 Cấu trúc thư mục dự án
```plaintext
Amadeus-ETL/
├── Amadeus ETL/ # Dự án chính trong SSIS
│ ├── Amadeus ETL.database
│ ├── Amadeus ETL.dtproj # File mở dự án trong Visual Studio
│ ├── Package1.dtsx # Gói xử lý ETL mẫu
│ ├── Project.params
│ └── order_header.dtsx # Gói xử lý dữ liệu đơn hàng
│
├── Nhóm 6 - Cơ sở dữ liệu nâng cao.pdf/docx # Báo cáo tổng quan nhóm
├── Nhóm 6 - Data Extraction.pdf/pptx # Slide trình bày lý thuyết
├── Meta.sql # Tạo bảng metadata
├── Stage.sql # Tạo bảng staging
├── Jade.sql # Tạo bảng đích (data mart)
├── README.md # Tài liệu này
```

---

## 🎯 Mục tiêu dự án

- Mô hình hóa toàn bộ quy trình ETL từ trích xuất, chuyển đổi đến tải dữ liệu.
- Thực hành xây dựng pipeline ETL bằng SSIS.
- Áp dụng các khái niệm: staging, metadata, data warehouse schema (Kimball).
- Trình bày lý thuyết kết hợp thực hành qua báo cáo và slide nhóm.

---

## 🔧 Thành phần chính

### 🛠️ 1. **Gói ETL trong SSIS**
- `Package1.dtsx`: Pipeline ETL mẫu
- `order_header.dtsx`: Gói ETL thực hiện trích xuất đơn hàng

### 🧾 2. **Câu lệnh SQL**
- `Meta.sql`: Tạo bảng metadata
- `Stage.sql`: Tạo bảng staging lưu dữ liệu thô
- `Jade.sql`: Tạo bảng đích dùng cho phân tích

### 📄 3. **Tài liệu & Slide**
- `Nhóm 6 - Cơ sở dữ liệu nâng cao.pdf`: Báo cáo chi tiết dự án
- `Nhóm 6 - Data Extraction.pptx`: Slide trình bày quy trình ETL và lý thuyết

---

## 💡 Công nghệ sử dụng

- 🧱 **Microsoft SQL Server Management Studio (SSMS)**
- 💼 **SQL Server Integration Services (SSIS)**
- 📊 **T-SQL**
- 🧾 **Microsoft Word & PowerPoint** (cho tài liệu và slide)

---

## 👥 Thông tin nhóm

- **Tên nhóm:** Nhóm 6 – Môn Cơ sở dữ liệu nâng cao  
- **Thành viên GitHub:** [Nguyễn Hải An](https://github.com/haian2004)  
- **Trường học:** [Đại Học Y tế Công Cộng]

---

## 📌 Ghi chú

- Dự án không gọi dữ liệu trực tiếp từ API Amadeus mà sử dụng dữ liệu mô phỏng.
- Đây là sản phẩm phục vụ học tập – không sử dụng cho mục đích thương mại.
- File `.dtsx` cần mở bằng Visual Studio có tích hợp SSIS.

---

## ✅ Hướng dẫn sử dụng

1. **Tải về dự án:**
```bash
git clone https://github.com/haian2004Amadeus-ETL.git
```
2. **Mở trong Visual Studio (có SSIS):**
Vào File → Open → Project/Solution → chọn Amadeus ETL.dtproj
3. Chạy các file SQL theo thứ tự:
- Meta.sql → Tạo bảng metadata
- Stage.sql → Tạo bảng staging
- Jade.sql → Tạo bảng đích

# 📘 Tài liệu tham khảo:
- Sách Building a Data Warehouse With Examples, Chương 7–8.
- Slide giảng viên & giáo trình môn học.
