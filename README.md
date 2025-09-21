📊 So sánh ARCH và GARCH trong Phân tích Chuỗi Thời gian
👋 Giới thiệu

Trong lĩnh vực tài chính, chuỗi thời gian thường thể hiện hiện tượng biến động cụm (volatility clustering):

Khi thị trường biến động mạnh thì các giai đoạn sau thường tiếp tục biến động mạnh.

Khi thị trường ổn định thì biến động nhỏ thường kéo dài.

Để mô hình hóa và dự báo hiện tượng này, các mô hình ARCH (Autoregressive Conditional Heteroskedasticity) và GARCH (Generalized ARCH) được sử dụng rộng rãi.

🎯 Mục tiêu

Giới thiệu và giải thích hiện tượng volatility clustering.

Trình bày chi tiết mô hình ARCH(q) và GARCH(p,q).

So sánh sự khác biệt giữa ARCH và GARCH.

Ứng dụng mô hình để phân tích dữ liệu lợi suất Bitcoin.

📚 Nội dung chính
1. Hiện tượng biến động cụm

Biến động mạnh → có xu hướng kéo dài.

Biến động nhỏ → cũng có xu hướng kéo dài.

Thường thấy trong lợi suất cổ phiếu, tỷ giá, giá hàng hóa.

2. ARCH (Engle, 1982)

Phương sai có điều kiện phụ thuộc vào nhiễu quá khứ.

Dùng để dự báo rủi ro (VaR), mô hình hóa biến động ngắn hạn.

Nhược điểm: cần bậc cao → dễ overfitting.

3. GARCH (Bollerslev, 1986)

Mở rộng của ARCH.

Phương sai có điều kiện phụ thuộc vào nhiễu quá khứ + phương sai quá khứ.

Hiệu quả hơn với ít tham số, mô hình hóa biến động dài hạn tốt hơn.

4. So sánh ARCH và GARCH
Đặc điểm	ARCH(p)	GARCH(p,q)
Phương sai	Chỉ phụ thuộc nhiễu quá khứ	Phụ thuộc cả nhiễu và phương sai quá khứ
Độ linh hoạt	Cần nhiều tham số nếu p lớn	Hiệu quả hơn với ít tham số
Ứng dụng	Biến động ngắn hạn	Biến động phức tạp, dài hạn
5. Ứng dụng trên dữ liệu Bitcoin

Nguồn: Bitcoin Historical Data
.

Dữ liệu gồm: Timestamp, Open, High, Low, Close, Volume.

Tiền xử lý: chuyển Timestamp, lấy giá đóng cửa, tính log-return.

So sánh mô hình GARCH(1,1) và GARCH(1,2) → Kết quả: GARCH(1,1) phù hợp hơn.

🛠️ Công nghệ sử dụng

Python (pandas, numpy, matplotlib, scipy)

ARCH/GARCH modeling (statsmodels hoặc arch package)
