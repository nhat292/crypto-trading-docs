# Kiến thức nền tảng

Đây là những khái niệm bắt buộc phải hiểu rõ trước khi đặt lệnh đầu tiên bằng
tiền thật. Đừng bỏ qua vì thấy "cơ bản" — phần lớn cháy tài khoản của người
mới đến từ việc hiểu sai các khái niệm ở đây, đặc biệt là đòn bẩy và liquidation.

## Các loại lệnh (Order Types)

| Loại lệnh | Ý nghĩa | Khi nào dùng |
|---|---|---|
| Market Order | Khớp ngay theo giá thị trường hiện tại | Cần vào/thoát lệnh ngay, chấp nhận trượt giá (slippage) |
| Limit Order | Đặt trước một mức giá cụ thể, chỉ khớp khi giá chạm tới | Muốn kiểm soát giá vào lệnh, không vội |
| Stop-Loss (SL) | Tự động đóng lệnh khi giá đi ngược đến mức đã định | Bắt buộc phải có cho MỌI lệnh, giới hạn lỗ tối đa |
| Take-Profit (TP) | Tự động chốt lời khi giá đạt mục tiêu | Chốt lời theo kế hoạch, tránh tham lam giữ quá lâu |
| OCO (One-Cancels-the-Other) | Đặt đồng thời SL và TP, lệnh nào khớp trước thì hủy lệnh còn lại | Đặt lệnh xong rồi không cần theo dõi liên tục |

## Spot vs Margin vs Futures/Perpetual

| Loại hình | Bản chất | Rủi ro |
|---|---|---|
| Spot | Mua/bán coin thật, sở hữu trực tiếp | Chỉ mất tối đa số vốn bỏ ra, không có liquidation |
| Margin | Vay thêm tiền/coin từ sàn để giao dịch với vốn lớn hơn vốn thật có | Có thể mất nhiều hơn vốn ban đầu, bị gọi ký quỹ (margin call) |
| Futures/Perpetual | Hợp đồng phái sinh, đặt cược vào biến động giá bằng đòn bẩy, không sở hữu coin thật | Rủi ro cao nhất, dễ bị thanh lý (liquidation) toàn bộ vị thế |

**Lời khuyên cho người mới**: bắt đầu và thành thạo ở Spot trước. Chỉ chuyển
sang Futures/Margin khi đã có kỷ luật quản trị rủi ro vững (xem
[05-quan-tri-rui-ro.md](05-quan-tri-rui-ro.md)) và hiểu rõ cơ chế liquidation
bên dưới.

## Đòn bẩy (Leverage), Funding Rate, Liquidation

- **Đòn bẩy**: vay thêm vốn để mở vị thế lớn hơn số tiền thật có. Đòn bẩy
  x10 nghĩa là chỉ cần giá đi ngược ~10% là mất trắng phần vốn ký quỹ cho
  vị thế đó. Đòn bẩy càng cao, biên độ chịu đựng trước khi bị thanh lý càng
  nhỏ.
- **Funding Rate**: phí định kỳ (thường 8 giờ/lần) giữa bên Long và bên
  Short trên hợp đồng Perpetual, để giá hợp đồng bám sát giá Spot. Giữ lệnh
  càng lâu, chi phí funding cộng dồn càng đáng kể.
- **Liquidation (Thanh lý)**: khi lỗ chạm đến mức ký quỹ tối thiểu, sàn tự
  động đóng vị thế và mất toàn bộ phần ký quỹ đã bỏ vào lệnh đó. Đây là lý do
  các cây "râu nến" quét mạnh hay xảy ra quanh vùng thanh khoản dày đặc lệnh
  đòn bẩy (xem [09-doc-vi-ca-map-onchain.md](09-doc-vi-ca-map-onchain.md)).

## Ví & Bảo mật

- **Ví nóng (hot wallet)**: kết nối internet (ví trên sàn, ví app điện
  thoại/extension trình duyệt). Tiện lợi nhưng rủi ro bị hack cao hơn.
- **Ví lạnh (cold wallet)**: thiết bị phần cứng không kết nối internet
  thường xuyên. An toàn hơn cho lưu trữ dài hạn, không phù hợp để trade
  thường xuyên.
- **Nguyên tắc**: không để toàn bộ vốn trên sàn giao dịch. Bật 2FA (ưu tiên
  ứng dụng xác thực hơn SMS), không bao giờ chia sẻ seed phrase/private key
  với bất kỳ ai, cảnh giác với link giả mạo (phishing) giả danh sàn/dự án.

## Thuật ngữ cơ bản khác

- **Spread**: chênh lệch giữa giá mua (bid) và giá bán (ask).
- **Slippage**: chênh lệch giữa giá dự kiến và giá khớp thực tế, thường xảy
  ra khi thanh khoản mỏng hoặc dùng Market Order lúc biến động mạnh.
- **Volume**: khối lượng giao dịch, phản ánh mức độ quan tâm/thanh khoản.
- **Market Cap**: vốn hóa thị trường = giá x lượng cung lưu hành, dùng để so
  sánh quy mô giữa các coin.
