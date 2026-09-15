# 📊 Đọc nến & Chart cơ bản

## 🕯️ Nến Nhật (Candlestick)

Mỗi cây nến thể hiện 4 mức giá trong một khung thời gian: giá mở cửa (Open),
giá đóng cửa (Close), giá cao nhất (High), giá thấp nhất (Low).

- **Thân nến (body)**: khoảng cách giữa Open và Close.
  - 🟢 Nến xanh (tăng): Close > Open — phe mua thắng thế trong khung đó.
  - 🔴 Nến đỏ (giảm): Close < Open — phe bán thắng thế trong khung đó.
- **Râu nến (wick/shadow)**: phần giá đã chạm tới nhưng bị đẩy lùi lại, thể
  hiện vùng giá bị từ chối. Râu càng dài, mức độ giằng co/từ chối càng mạnh.
  - 🔽 Râu dài phía dưới: giá bị đẩy xuống rồi bật lại mạnh — dấu hiệu phe mua
    nhập cuộc, hoặc là cú "quét thanh khoản" (xem file 09).
  - 🔼 Râu dài phía trên: giá bị đẩy lên rồi bị bán lại mạnh — dấu hiệu phe bán
    nhập cuộc.
- **Thân nến dài, không râu (hoặc râu rất ngắn)**: xu hướng dứt khoát, một
  phe áp đảo hoàn toàn trong khung thời gian đó.

## 🕯️ Các mô hình nến (Candlestick Patterns)

### 1️⃣ Mô hình nến đơn (Single Candlestick Patterns)

Phản ánh sự biến động giá trong một khung thời gian duy nhất, thường phát
tín hiệu đảo chiều hoặc tiếp diễn khi xuất hiện ở vùng S/R quan trọng.

| Mô hình | Minh hoạ | Đặc điểm | Ý nghĩa |
|---|---|---|---|
| 🌀 Doji (Con xoay) | <img src="images/candles/doji.svg" width="70"> | Open ≈ Close, thân rất mỏng, có râu trên/dưới | Lưỡng lự, tranh chấp mạnh giữa phe mua/bán, không bên nào thắng thế — cảnh báo xu hướng hiện tại sắp đảo chiều |
| 🔨 Hammer (Búa) | <img src="images/candles/hammer.svg" width="70"> | Thân nhỏ ở trên, râu dưới rất dài (≥ 2-3 lần thân), râu trên rất ngắn/không có | Xuất hiện ở **đáy** downtrend → báo hiệu đảo chiều **tăng** |
| 🪢 Hanging Man (Người treo cổ) | <img src="images/candles/hanging-man.svg" width="70"> | Hình dạng giống Hammer | Xuất hiện ở **đỉnh** uptrend → báo hiệu đảo chiều **giảm** |
| 🔨⤴️ Inverted Hammer (Búa ngược) | <img src="images/candles/inverted-hammer.svg" width="70"> | Thân nhỏ ở dưới, râu trên rất dài, râu dưới rất ngắn/không có | Xuất hiện cuối downtrend → báo hiệu đảo chiều **tăng** |
| ⭐️💥 Shooting Star (Sao băng) | <img src="images/candles/shooting-star.svg" width="70"> | Hình dạng giống Inverted Hammer | Xuất hiện ở **đỉnh** uptrend → báo hiệu đảo chiều **giảm** mạnh (phe mua đẩy giá lên nhưng bị phe bán dập tắt) |
| 🟩🟥 Marubozu (Nến cường lực) | <img src="images/candles/marubozu.svg" width="100"> | Thân rất dài, gần như không có râu | Lực mua (nến xanh) hoặc lực bán (nến đỏ) áp đảo hoàn toàn → xu hướng hiện tại tiếp diễn |

### 2️⃣ Mô hình nến đôi & tổ hợp (Multiple Candlestick Patterns)

Kết hợp từ 2-3 nến trở lên, độ tin cậy thường cao hơn nến đơn.

| Mô hình | Minh hoạ | Đặc điểm | Ý nghĩa |
|---|---|---|---|
| 🟢🔴 Bullish Engulfing (Nhấn chìm tăng) | <img src="images/candles/bullish-engulfing.svg" width="110"> | Nến đỏ nhỏ, theo sau bởi nến xanh lớn nuốt trọn thân nến trước | Xuất hiện ở vùng hỗ trợ → đảo chiều **tăng** |
| 🔴🟢 Bearish Engulfing (Nhấn chìm giảm) | <img src="images/candles/bearish-engulfing.svg" width="110"> | Nến xanh nhỏ, theo sau bởi nến đỏ lớn nuốt trọn thân nến trước | Xuất hiện ở vùng kháng cự → đảo chiều **giảm** |
| ✂️⬆️ Tweezers Bottom (Nhíp đáy) | <img src="images/candles/tweezers-bottom.svg" width="110"> | 2 nến có cùng mức giá thấp nhất | Vùng hỗ trợ cứng, giá không phá được đáy chung → chuẩn bị đảo chiều tăng |
| ✂️⬇️ Tweezers Top (Nhíp đỉnh) | <img src="images/candles/tweezers-top.svg" width="110"> | 2 nến có cùng mức giá cao nhất | Vùng kháng cự cứng, giá không phá được đỉnh chung → chuẩn bị đảo chiều giảm |
| ☁️⬇️ Dark Cloud Cover (Mây đen che phủ) | <img src="images/candles/dark-cloud-cover.svg" width="110"> | Nến xanh dài → nến sau gap up nhưng đóng cửa giảm sâu, lấn > 50% thân nến trước | Xuất hiện ở đỉnh → đảo chiều **giảm** mạnh |
| 🗡️⬆️ Piercing Line (Đường xuyên) | <img src="images/candles/piercing-line.svg" width="110"> | Nến đỏ dài → nến sau gap down nhưng đóng cửa tăng vượt > 50% thân nến trước | Xuất hiện ở đáy → đảo chiều **tăng** |
| 🌅 Morning Star (Sao mai) | <img src="images/candles/morning-star.svg" width="150"> | Nến đỏ dài → nến thân nhỏ (Doji/Spinning top, có gap) → nến xanh dài phục hồi | Bộ 3 nến đảo chiều **tăng**, độ tin cậy rất cao |
| 🌆 Evening Star (Sao hôm) | <img src="images/candles/evening-star.svg" width="150"> | Nến xanh dài → nến thân nhỏ (có gap) → nến đỏ dài xác nhận | Bộ 3 nến đảo chiều **giảm**, độ tin cậy rất cao |

> [!TIP]
> Lưu ý khi giao dịch với mô hình nến:
> - **Không giao dịch đơn lẻ**: đặt mô hình nến trong bối cảnh thị trường
>   (vùng S/R, MA, Volume) thay vì chỉ dựa vào một cây nến.
> - **Khung thời gian**: mô hình ở khung lớn (Daily, 4H) đáng tin cậy hơn
>   nhiều so với khung nhỏ (1m, 5m).
> - **Chờ nến xác nhận**: với mô hình đảo chiều, đợi nến tiếp theo đóng cửa
>   xác nhận hướng đi trước khi vào lệnh.

## 📶 Khối lượng giao dịch (Volume)

Volume là tổng khối lượng coin được mua bán trong một khung thời gian,
thường hiển thị dạng cột ngay dưới biểu đồ giá (cột xanh khi nến tăng, cột
đỏ khi nến giảm). Volume cho biết **có bao nhiêu người/tiền thật sự đứng sau
một cây nến** — một cây nến đẹp nhưng volume nhỏ giọt đáng tin cậy thấp hơn
nhiều so với cây nến cùng hình dạng nhưng volume tăng vọt.

- **Xác nhận breakout**: giá phá vỡ vùng S/R kèm volume tăng đột biến →
  breakout đáng tin. Phá vỡ với volume thấp → nghi ngờ false breakout, dễ bị
  đảo ngược lại ngay sau đó (xem "Quét hai đầu" ở file 09 và Liquidity Sweep
  ở file 11).
- **Volume climax**: volume đột biến cực lớn sau một chuỗi tăng/giảm dài
  thường là dấu hiệu kiệt sức (exhaustion) của xu hướng — khả năng đảo chiều
  hoặc điều chỉnh mạnh sắp tới.
- **Volume divergence**: giá tạo đỉnh/đáy mới nhưng volume của đợt đó lại
  giảm dần so với đợt trước → xu hướng đang yếu đi dù giá vẫn đang đi, cần
  thận trọng khi vào lệnh đuổi theo.

> [!TIP]
> Luôn nhìn volume song song với nến, đừng đọc nến một mình. Một cây nến
> phá vỡ mạnh nhưng volume nhỏ giọt thường là bẫy hơn là tín hiệu thật.

## 📏 Support & Resistance (S/R)

- 🟩 **Support (hỗ trợ)**: vùng giá mà lực mua từng đủ mạnh để chặn đà giảm,
  giá có xu hướng bật lên khi chạm tới.
- 🟥 **Resistance (kháng cự)**: vùng giá mà lực bán từng đủ mạnh để chặn đà
  tăng, giá có xu hướng bị đẩy xuống khi chạm tới.

> [!NOTE]
> S/R không phải một đường kẻ chính xác tuyệt đối mà là một **vùng giá** —
> giá thường xuyên "xuyên qua" một chút rồi mới phản ứng thật. Một vùng S/R
> bị phá vỡ dứt khoát (breakout) có thể đổi vai trò: hỗ trợ cũ trở thành
> kháng cự mới và ngược lại.

## 🕳️ Fair Value Gap (FVG) — cơ bản

FVG là một khoảng trống giá hình thành khi thị trường di chuyển quá nhanh
theo một hướng, để lại một "lỗ hổng" chưa được giao dịch cân bằng (thường
xác định bằng khoảng trống giữa bóng nến 1 và bóng nến 3 trong một chuỗi 3
nến di chuyển mạnh). Thị trường có xu hướng quay lại lấp đầy vùng FVG trước
khi tiếp tục xu hướng chính — nhiều trader dùng vùng này làm điểm chờ vào
lệnh theo xu hướng lớn thay vì đuổi giá.

> [!NOTE]
> FVG chỉ là một mảnh ghép nhỏ trong bức tranh lớn hơn về cách tổ chức/cá
> mập để lại dấu vết trên biểu đồ giá. Xem chi tiết ở
> [🧭 11-smart-money-concepts.md](11-smart-money-concepts.md) (Liquidity,
> Order Block, BOS/CHoCH, Premium/Discount zone).

## 📈 Xác định xu hướng (Trend)

- 📈 **Uptrend**: đáy sau cao hơn đáy trước, đỉnh sau cao hơn đỉnh trước.
- 📉 **Downtrend**: đỉnh sau thấp hơn đỉnh trước, đáy sau thấp hơn đáy trước.
- ➡️ **Sideway**: giá dao động trong một vùng, không tạo đỉnh/đáy mới rõ ràng.

> [!IMPORTANT]
> Luôn xác định trend ở khung thời gian **lớn hơn** (Daily/4H) trước khi tìm
> điểm vào lệnh ở khung nhỏ hơn — đây chính là câu hỏi số 1 trong checklist
> vào lệnh (file 04).

## 📉 Các chỉ báo kỹ thuật phổ biến (Indicators)

Chỉ báo kỹ thuật được tính toán từ giá/volume quá khứ — luôn là công cụ
**hỗ trợ đọc lại quá khứ (lagging)**, không dự đoán tương lai. Chia làm 3
nhóm theo cách hiển thị trên chart.

### 🔵 Nhóm vẽ đè lên biểu đồ giá (Overlay)

| Chỉ báo | Tên đầy đủ | Đo gì | Cách đọc nhanh |
|---|---|---|---|
| MA | Moving Average (đường trung bình động) | Xu hướng giá trung bình qua N kỳ | Giá nằm trên MA = thiên hướng tăng; MA ngắn cắt lên MA dài (golden cross) = tín hiệu tăng, cắt xuống (death cross) = tín hiệu giảm |
| BOLL | Bollinger Bands (dải Bollinger) | Biến động (volatility) quanh đường trung bình | Dải co hẹp lại = biến động thấp, chuẩn bị bùng nổ; giá chạm dải ngoài không tự động là đảo chiều, cần xác nhận thêm bằng nến/volume |
| SAR | Parabolic SAR | Điểm dừng & đảo chiều xu hướng | Chấm nằm dưới nến = đang uptrend, chấm nằm trên nến = đang downtrend; chấm nhảy sang phía đối diện = cảnh báo đổi xu hướng, hay dùng làm mốc trailing stop |
| AVL | Average Line | Đường trung bình giá rút gọn (một số sàn như Binance cung cấp riêng) | Đọc tương tự MA, dùng tham khảo xu hướng nhanh, không thay thế MA/EMA chuẩn |
| SuperTrend | SuperTrend (thường viết tắt SUPER/SUPPER) | Xu hướng dựa trên biên độ biến động thật ATR | Một đường bám sát giá, đổi màu xanh/đỏ khi xu hướng đổi chiều; đường này cũng thường dùng làm mốc trailing stop |

### 🟣 Nhóm dao động (Oscillator — hiển thị khung phụ riêng)

| Chỉ báo | Tên đầy đủ | Đo gì | Cách đọc nhanh |
|---|---|---|---|
| MACD | Moving Average Convergence Divergence | Động lượng qua chênh lệch giữa 2 đường EMA | Đường MACD cắt lên Signal = tín hiệu mua, cắt xuống = tín hiệu bán; Histogram co lại = động lượng yếu đi; phân kỳ MACD-giá = cảnh báo đảo chiều |
| RSI | Relative Strength Index | Tốc độ & độ lớn thay đổi giá, dao động 0-100 | Trên 70 = quá mua (overbought), dưới 30 = quá bán (oversold); phân kỳ RSI-giá là tín hiệu đáng chú ý |
| KDJ | Stochastic mở rộng (3 đường K, D, J) | Vị trí giá đóng cửa so với biên độ cao/thấp gần đây | J vượt mạnh ra ngoài khoảng 0-100 = tín hiệu cực đoan hơn K/D; J cắt K/D theo hướng nào thường báo hiệu theo hướng đó |
| WR | Williams %R | Tương tự Stochastic nhưng đảo trục, dao động 0 đến -100 | Gần 0 = quá mua, gần -100 = quá bán |

### 🟢 Nhóm khối lượng

| Chỉ báo | Tên đầy đủ | Đo gì | Cách đọc nhanh |
|---|---|---|---|
| OBV | On-Balance Volume | Dòng tiền tích luỹ qua volume theo hướng giá | OBV tăng cùng chiều với giá = xác nhận xu hướng; giá tạo đỉnh/đáy mới nhưng OBV không xác nhận (phân kỳ) = xu hướng đang yếu, cẩn trọng khi vào lệnh đuổi theo |

> [!WARNING]
> Không dùng một chỉ báo đơn lẻ để quyết định vào lệnh. Càng nhồi nhiều chỉ
> báo lên chart càng dễ rối tín hiệu ("indicator paralysis") — chọn tối đa
> 1-2 chỉ báo phù hợp phong cách của mình, dùng để **bổ trợ** cho nến, S/R,
> volume và cấu trúc thị trường (file 11), không thay thế checklist 5 câu
> hỏi ở [✅ 04-quy-tac-vao-lenh.md](04-quy-tac-vao-lenh.md).

## 🔍 Đa khung thời gian (Multi-timeframe)

```mermaid
flowchart TD
    A["🗓️ Daily/4H\nXác định TREND"] --> B["🕐 1H/15m\nTìm ĐIỂM VÀO LỆNH"]
    B --> C["⏱️ 5m hoặc nhỏ hơn\nTINH CHỈNH entry\n(chỉ khi đã thành thạo)"]

    classDef big fill:#3b82f6,stroke:#1e40af,color:#fff
    classDef mid fill:#10b981,stroke:#065f46,color:#fff
    classDef small fill:#f59e0b,stroke:#92400e,color:#fff
    class A big
    class B mid
    class C small
```

Nguyên tắc: dùng khung lớn để xác định **hướng đi** (trend), dùng khung nhỏ
hơn để tìm **điểm vào lệnh** có lợi (entry) theo đúng hướng đó.

| Khung | Vai trò |
|---|---|
| 🗓️ Daily / 4H | Xác định xu hướng chính, vùng S/R quan trọng |
| 🕐 1H / 15m | Tìm điểm vào lệnh cụ thể theo hướng của khung lớn |
| ⏱️ 5m hoặc nhỏ hơn | Tinh chỉnh điểm vào chính xác (chỉ dùng khi đã thành thạo, dễ nhiễu tín hiệu) |

> [!WARNING]
> Tránh chỉ nhìn một khung thời gian duy nhất — đây là nguyên nhân phổ biến
> khiến trader mới vào lệnh ngược xu hướng lớn mà không hề biết.
