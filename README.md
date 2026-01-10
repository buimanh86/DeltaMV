Dự án Phân tích Hành vi và Lộ trình Tiêm chủng (DeltaMV Project)
1. Tổng quan dự án
Dự án được thực hiện nhằm xây dựng hệ thống báo cáo chuyên môn về tiêm chủng theo đặt hàng từ DeltaMV Knowledge Solutions – đơn vị nghiên cứu thị trường chuyên sâu về chiến lược hành vi y tế.
Mục tiêu chính là chuyển hóa tập dữ liệu khảo sát thô cực kỳ phức tạp thành các Insight chiến lược giúp doanh nghiệp hiểu rõ tâm lý khách hàng, lý do lựa chọn thương hiệu vắc xin và hiệu quả của các kênh tư vấn tại điểm tiêm.
2. Bài toán kinh doanh
• Thách thức: Dữ liệu nguồn là file Excel chứa kết quả khảo sát "Exit Interview" với 3.885 trường dữ liệu chồng chéo, được thiết kế theo dạng ma trận khảo sát nên không thể sử dụng trực tiếp để phân tích.
• Giải pháp: Triển khai quy trình ETL toàn diện để bóc tách dữ liệu thô, xây dựng mô hình dữ liệu chuẩn và trực quan hóa lên Dashboard.
3. Công nghệ sử dụng
• Ngôn ngữ lập trình: Python 3.10 (Thư viện chính: Pandas).
• Công cụ BI: Power BI Desktop (Xây dựng DAX nâng cao và Dashboard tương tác).
• Quản lý dữ liệu: Excel (đóng vai trò vùng lưu trữ trung gian cho các bảng Fact/Dim).
• Môi trường phát triển: Visual Studio Code.
4. Kiến trúc dữ liệu (Data Architecture)
Dự án tuân thủ mô hình Snowflake Schema để tối ưu hóa khả năng truy vấn và đảm bảo tính chính xác khi phân tích đa chiều.
• ETL Process: Sử dụng thuật giải Python để tách dữ liệu ma trận thành 13 bảng STG (Staging) như: Actual Injection, Brand Choice, Recommendation, Advertisement....
• Modeling: Thiết lập hệ thống hơn 23 bảng Dimension (Dim_Brand, Dim_Disease, Dim_AgeGroup...) kết nối với các bảng Fact để phục vụ báo cáo.
5. Các đầu ra chính (Main Outputs)
Hệ thống báo cáo bao gồm 06 trang phân tích chuyên sâu trên Power BI:
1. Page 3 - Tỉ lệ tiêm vắc xin: Phân tích số lượng và tỷ trọng tiêm theo từng loại bệnh tại khu vực Hà Nội & TP.HCM.
2. Page 4 - Chi tiết Thương hiệu (Brand Share): Tỷ trọng thị phần của các hãng vắc xin (GSK, MSD, Sanofi...) theo từng loại bệnh.
3. Page 7 - Dự định vs. Thực tế: So sánh tỷ lệ khách hàng có chủ đích tiêm ban đầu và kết quả tiêm thực tế.
4. Page 8 - Phân tích Shingles (Zona thần kinh): Tập trung vào đối tượng trên 50 tuổi, tỷ lệ khuyến nghị của bác sĩ và thời gian tiêm mũi 2.
5. Page 12 - Chuyển đổi hành vi: Khảo sát những người không có chủ đích tiêm ban đầu nhưng đã quyết định tiêm sau khi được tư vấn.
6. Page 13 - Hiệu quả quảng cáo: Đánh giá các hình thức quảng cáo (Stand-up displays, Banners, TV...) tại điểm tiêm
