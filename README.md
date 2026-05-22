# Phân tích dữ liệu xuất khẩu Việt Nam hỗ trợ nghiệp vụ LC

Repository này lưu trữ mã nguồn, dữ liệu xử lý, dashboard Power BI và tài liệu liên quan đến khóa luận tốt nghiệp:

**“Phân tích dữ liệu thương mại xuất khẩu của Việt Nam nhằm hỗ trợ nghiệp vụ thư tín dụng (LC) tại ngân hàng”**

---

# 1. Tổng quan đề tài

Đề tài tập trung phân tích dữ liệu xuất khẩu của Việt Nam trong giai đoạn 2019–2023 nhằm hỗ trợ đánh giá rủi ro ngành trong hoạt động tài trợ thư tín dụng (Letter of Credit – LC) tại ngân hàng thương mại.

Nghiên cứu sử dụng dữ liệu từ UN Comtrade, xử lý bằng Python trên Kaggle và trực quan hóa bằng Power BI nhằm xây dựng hệ thống dashboard phục vụ:

- Phân tích xu hướng xuất khẩu
- Đánh giá cơ cấu ngành hàng
- Đo lường mức độ tập trung xuất khẩu
- Đánh giá tính ổn định và khả năng phục hồi ngành
- Hỗ trợ phân loại rủi ro ngành trong nghiệp vụ LC

---

# 2. Mục tiêu nghiên cứu

Nghiên cứu hướng đến ba mục tiêu chính:

- Phân tích xu hướng và cơ cấu xuất khẩu của Việt Nam theo ngành hàng trong giai đoạn 2019–2023.
- Đánh giá mức độ tập trung, biến động và khả năng phục hồi của các nhóm ngành xuất khẩu thông qua các chỉ số phân tích dữ liệu.
- Đề xuất framework hỗ trợ đánh giá rủi ro ngành phục vụ hoạt động tài trợ thư tín dụng (LC) tại ngân hàng.

---

# 3. Nguồn dữ liệu

Nguồn dữ liệu chính:

- UN Comtrade Database
- Dữ liệu xử lý trên Kaggle/Python

Phạm vi dữ liệu:

- Quốc gia báo cáo: Việt Nam
- Loại giao dịch: Export
- Đối tác: World (W00)
- Giai đoạn: 2019–2023
- Phân loại hàng hóa: HS2

Các file dữ liệu sau xử lý được lưu trong thư mục `data/` và sử dụng làm đầu vào cho Power BI.

---

# 4. Pipeline phân tích dữ liệu

Quy trình nghiên cứu được xây dựng dựa trên CRISP-DM và điều chỉnh phù hợp với bài toán phân tích dữ liệu xuất khẩu:

1. Hiểu bài toán
2. Hiểu dữ liệu
3. Tiền xử lý dữ liệu
4. Thiết kế các độ đo phân tích
5. Xây dựng mô hình Star Schema
6. ETL vào Power BI
7. Thiết kế dashboard
8. Phân tích kết quả và diễn giải nghiệp vụ LC

---

# 5. Các chỉ số phân tích chính

Project sử dụng các chỉ số:

- Total Export Value
- YoY Growth
- Export Share
- CR5 / CR10
- Herfindahl–Hirschman Index (HHI)
- YoY Volatility
- Export Stability Index (ESI)
- Recovery Rate
- Risk Score

Các chỉ số được sử dụng để đánh giá mức độ tập trung, ổn định và rủi ro của từng nhóm ngành xuất khẩu.

---

# 6. Dashboard Power BI

Dashboard Power BI được xây dựng nhằm hỗ trợ trực quan hóa và phân tích dữ liệu xuất khẩu theo nhiều góc nhìn khác nhau.

Các nhóm dashboard chính bao gồm:

- Tổng quan xuất khẩu theo thời gian
- Cơ cấu ngành hàng xuất khẩu
- Mức độ tập trung xuất khẩu
- Độ ổn định và biến động ngành
- Framework phân loại rủi ro ngành hỗ trợ thẩm định LC

## Hướng dẫn mở dashboard

### Bước 1: Cài đặt Power BI Desktop

Tải Power BI Desktop tại:

https://powerbi.microsoft.com/

### Bước 2: Clone repository

```bash
git clone <repo-link>
```

### Bước 3: Mở file Power BI

Mở file:

```text
dashboard/LC_Export_Risk_Analysis.pbix
```

### Bước 4: Cập nhật đường dẫn dữ liệu (nếu cần)

Nếu Power BI báo lỗi đường dẫn dữ liệu:

- Chọn `Transform Data`
- Vào `Data Source Settings`
- Trỏ lại đến thư mục `data/`

### Bước 5: Refresh dữ liệu

Nhấn `Refresh` để tải lại dữ liệu dashboard.

---

# 7. Cấu trúc repository

```text
project/
│
├── dashboard/      # File Power BI (.pbix)
├── data/           # Dataset đã xử lý
├── notebooks/      # Notebook xử lý dữ liệu bằng Python
├── references/     # Tài liệu tham khảo và báo cáo nghiên cứu
├── reports/        # Ảnh dashboard, slide và báo cáo khóa luận
├── src/            # Source code hỗ trợ
└── README.md
```

---

# 8. Hướng dẫn chạy notebook Python

Các notebook được chia theo từng giai đoạn phân tích:

```text
01_data_understanding.ipynb
02_data_cleaning_preparation.ipynb
03_export_trend_structure_analysis.ipynb
04_concentration_volatility_risk_analysis.ipynb
05_powerbi_data_export.ipynb
```

Thứ tự chạy khuyến nghị:

1. 01_data_understanding.ipynb
2. 02_data_cleaning_preparation.ipynb
3. 03_export_trend_structure_analysis.ipynb
4. 04_concentration_volatility_risk_analysis.ipynb
5. 05_powerbi_data_export.ipynb

Các thư viện chính được sử dụng:

```text
pandas
numpy
matplotlib
```

---

# 9. Tài liệu tham khảo

Thư mục `references/` lưu các tài liệu và báo cáo được sử dụng trong quá trình nghiên cứu, bao gồm:

- UCP 600
- Báo cáo xuất nhập khẩu Việt Nam
- Niên giám thống kê
- Tài liệu về credit concentration risk
- Các nghiên cứu liên quan đến quản trị rủi ro ngành và hoạt động LC
