---


---

<h3 id="phần-1-phân-tích-chẩn-đoán-lỗi-theo-khung-create">Phần 1: Phân tích chẩn đoán lỗi theo khung CREATE</h3>
<p>Khung CREATE gồm các thành phần: C (Context - Bối cảnh), R (Role - Vai trò), E (Examples - Ví dụ), A (Action - Hành động), T (Type of Output - Định dạng đầu ra), E (Extras - Yêu cầu thêm/điều kiện).</p>
<ol>
<li>Bộ phận CSKH:</li>
</ol>
<ul>
<li>Câu lệnh hiện tại: “Viết tin nhắn xin lỗi khách vì hàng giao chậm.”</li>
<li>Thành phần thiếu: Character (Nhân vật/Giọng điệu), Adjustment (Phương án xử lý/đền bù), Type (Định dạng).</li>
<li>Nguyên nhân lỗi: Thiếu thông tin về mức độ đền bù (voucher, quà tặng) và giọng điệu cần dùng (thân thiện, đồng cảm) khiến AI chỉ viết được câu xin lỗi chung chung.</li>
</ul>
<ol start="2">
<li>Bộ phận Bán hàng:</li>
</ol>
<ul>
<li>Câu lệnh hiện tại: “Tư vấn cho anh khách mua laptop gaming.”</li>
<li>Thành phần thiếu: Extras (Thông tin chi tiết về khách), Request (Yêu cầu cụ thể), Examples (Ví dụ mẫu).</li>
<li>Nguyên nhân lỗi: Không có thông tin về tầm giá, nhu cầu chơi game cụ thể (Esports hay AAA) hay cấu hình mong muốn nên AI liệt kê lan man toàn bộ máy gaming có trong hệ thống.</li>
</ul>
<ol start="3">
<li>Bộ phận Kỹ thuật bảo hành:</li>
</ol>
<ul>
<li>Câu lệnh hiện tại: “Báo giá thay màn hình laptop vỡ cho khách.”</li>
<li>Thành phần thiếu: Character (Vai trò kỹ thuật viên), Type of Output (Định dạng bảng biểu), Adjustment (Chính sách linh kiện).</li>
<li>Nguyên nhân lỗi: Thiếu model máy cụ thể và quy định bảo hành, khiến AI không thể đưa ra con số chính xác mà phải trả lời vòng vo.</li>
</ul>
<h3 id="phần-2-nâng-cấp-chuẩn-hóa-câu-lệnh-master-prompt">Phần 2: Nâng cấp chuẩn hóa câu lệnh (Master Prompt)</h3>
<ol>
<li>Master Prompt cho bộ phận CSKH:</li>
</ol>
<blockquote>
<p>Bạn là chuyên viên chăm sóc khách hàng cao cấp của chuỗi bán lẻ TechShop. Hãy viết một tin nhắn SMS/Zalo gửi khách hàng để xin lỗi về việc đơn hàng bị giao chậm trễ 2 ngày so với dự kiến do sự cố kho vận. Tin nhắn cần thể hiện sự chân thành, nhận toàn bộ trách nhiệm, thông báo thời gian giao hàng mới chính xác (vào ngày mai), và kèm theo mã voucher giảm giá 100.000 VNĐ cho lần mua sắm tiếp theo như một lời đền bù. Giọng điệu lịch sự, cầu thị, ngắn gọn dưới 100 chữ.</p>
</blockquote>
<ol start="2">
<li>Master Prompt cho bộ phận Bán hàng:</li>
</ol>
<blockquote>
<p>Bạn là nhân viên tư vấn bán hàng chuyên nghiệp tại TechShop. Hãy tư vấn cấu hình laptop gaming phù hợp cho một khách hàng nam sinh viên có ngân sách từ 20 đến 25 triệu VNĐ, chuyên chơi game Valorant, EA Sports FC Online và làm đồ họa nhẹ. Hãy đề xuất cụ thể 2 dòng máy phù hợp nhất đang kinh doanh, nêu rõ ưu điểm về CPU, GPU, màn hình và tần số quét, đồng thời báo giá kèm các chương trình khuyến mãi hiện hành của cửa hàng. Trình bày dưới dạng danh sách rõ ràng, dễ đọc.</p>
</blockquote>
<ol start="3">
<li>Master Prompt cho bộ phận Kỹ thuật bảo hành:</li>
</ol>
<blockquote>
<p>Bạn là kỹ thuật viên trưởng tại trung tâm bảo hành TechShop. Hãy soạn một văn bản báo giá và quy trình thay thế màn hình laptop cho dòng máy Dell Precision (cụ thể là màn hình 15.6 inch Full HD chống lóa). Nội dung cần bao gồm: chi phí linh kiện chính hãng, phí dịch vụ thay thế, thời gian thực hiện (trong 2 giờ), và chính sách bảo hành 6 tháng cho linh kiện thay mới. Trình bày dưới dạng bảng báo giá chi tiết kèm các lưu ý quan trọng về dữ liệu cho khách hàng.</p>
</blockquote>

