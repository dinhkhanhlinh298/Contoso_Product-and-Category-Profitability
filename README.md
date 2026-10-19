# Contoso_Product-and-Category-Profitability
Phân tích lợi nhuận qua danh mục sản phẩm để tìm ra nguyên nhân khiến lợi nhuận sụt giảm giai đoạn 2007-2009. Dự án sử dụng bộ dữ liệu Contoso phục vụ học tập; kết quả không phản ánh hoạt động của một doanh nghiệp thực tế.
## 1. Bài toán
Lợi nhuận gộp giảm từ 719,9 triệu USD năm 2007 xuống 539,5 triệu USD năm 2009, tương đương 180,4 triệu USD (25,1%). Phân tích tập trung trả lời:
- Mức giảm đến từ biến động doanh thu hay biên lợi nhuận gộp?
- Sản lượng và giá bán bình quân (ASP) đóng góp như thế nào vào biến động doanh thu?
- Nhóm sản phẩm và kênh bán hàng nào cần được ưu tiên xem xét?

*Phạm vi* gồm 8 nhóm sản phẩm và 4 kênh bán hàng: Store, Online, Catalog và Reseller.
## 2. Công cụ
### Công cụ chính: Power BI desktop
- Làm sạch dữ liệu: thay thế bảng DIMStore thiếu StoreKey thành bảng đầy đủ; xóa các khoảng trắng thừa; merge 3 bảng DIMProduct, DIMProductCategory và DIMProductSubCategory làm 1 để đảm bảo mô hình Star Schema; đổi kiểu dữ liệu các cột không đúng; giữ null cho các cột số dùng để tính toán, thay "N/A" cho các cột text hiển thị tránh lỗi Empty.
- Tổ chức mô hình dạng Star Schema với bảng FACT ở giữa, xung quanh là các bảng DIM.
- Phân tích khám phá dữ liệu (EDA): thực hiện Descriptive cho các biến CAT, NUM chính và Diagnostic để đào sâu tương quan giữa các biến.
- Làm dashboard báo cáo kết quả quân tích.
### Công cụ hỗ trợ: Claude AI
- Tạo skill để lên Logic tree theo nguyên tắc MECE.
- Hỗ trợ viết DAX và tạo bảng phức tạp.
- Hỗ trợ đưa ra hướng phân tích dưới sự kiểm soát của người dùng.
## 3. Phát hiện chính
- Lợi nhuận gộp giảm đáng kể: giảm 180,4 triệu USD, tuong đương 25,1% từ 2007 - 2009.
- Tác động của doanh thu chiếm ưu thế: tác động của doanh thu chiếm khoảng 97% mức giảm lợi nhuận gộp; tác động biên lợi nhuận chỉ chiếm khoảng 3%.
- ASP giảm dù sản lượng tăng: ASP giảm 29,4%; tác động của ASP lên doanh thu khoảng -378 triệu USD, trong khi tác động của sản lượng khoảng +73,2 triệu USD.
- Mức giảm tập trung ở hai nhóm sản phẩm: *Cameras and camcorders* và *Home Appliances* cộng lại giảm khoảng 150 triệu USD, tương đương 83,2% mức giảm toàn công ty.
- Store đóng góp lớn nhất theo kênh: Store giảm khoảng 165,1 triệu USD, tương đương 91,5% mức giảm toàn công ty; trong khi Online tăng 15,7 triệu USD.
## 4. Khuyến nghị
- Ưu tiên rà soát giá bán và khuyến mãi tại Store đối với 2 nhóm *Cameras and camcorders* và *Home Appliances*.
- Đánh giá phương án thiết lập giá sàn và cơ chế duyệt khuyến mãi, có xét đến giá vốn, sức cầu và khả năng cạnh tranh trước khi áp dụng.
- Đề xuất lập dashboard theo dõi ASP theo nhóm ngành x kênh bán hàng, cảnh báo khi lệch ngưỡng mục tiêu.
## Tài liệu dự án
- [Storytelling — Phát hiện và khuyến nghị](StoryTelling.pdf)
- [Báo cáo phân tích Power BI](DAR.pdf)
- [Phân tích khám phá dữ liệu](EDA.pdf)
- [Logic Tree](Logic%20Tree.pdf)
- [Mô hình dữ liệu](Data%20Model.png)
- [Taxonomy](Taxonomy%20%281%29.png)

*Tác giả:* Đinh Khánh Linh  
Dự án học tập sử dụng bộ dữ liệu mẫu Contoso.
