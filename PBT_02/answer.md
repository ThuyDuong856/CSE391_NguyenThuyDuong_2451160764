# Phiếu bài tập 02  

## Phần A 

### Câu A1: 
```
1.type="email" → ô nhập text, tự kiểm tra ký tự @ và định dạng domain → Dùng cho form đăng ký tài khoản.
2. type="number" → ô nhập có nút tăng/giảm, tự kiểm tra chỉ có nhập số → dùng để chọn số lượng sản phẩm.
3. type="tel" → ô nhập text, tự bật bàn phím số trên mobile → dùng để nhập số điện thoại.
4. type="url" → ô nhập text, tự kiểm tra có chứa giao thức hợp lệ (như http:// hoặc https://) → dùng cho nhàn bán hàng điền link website doanh nghiệp hoặc link trang cá nhân.
5. type="date" → ô nhập hiển thị bảng chọn lịch, tự kiểm tra tính hợp lệ của ngày tháng → dùng để chọn ngày tháng.
6. type="color" → ô hiển thị bảng chọn màu, tự trả về mã màu HEX → dùng làm bộ lọc tìm kiếm màu sắc.
7. type="range" → thanh trượt kéo ngang, tự giới hạn trong hkoangr min/max → dùng làm bộ lọc tìm kiếm theo giá tiền.
8. type="search" → ô nhập có nút xóa nhanh "x", tự tối ưu phím Search trên thiết bị → dùng cho thanh tìm kiếm sản phẩm.
9. type="file" → ô có nút tải file, tự lọc định dạng tệp qua tag accept → dùng để tải ảnh review sản phẩm.
10. type="password" → ô nhập ẩn ký tự thành dấu chấm tròn bảo mật → dùng để điền mật khẩu đăng nhập/thanh toán.
```

### Câu A2:  
1.TH1: Báo lỗi. Vì thuộc tính required bắt buộc trường hợp này không để trống  
2. TH2: Báo lỗi. Vì giá trị "abc" thiếu ký tự @ và phần domain để tạo thành 1 email hợp lệ.  
3. TH3: Báo lỗi. Vì giá trị 15 đã vượt giới hạn tối đa được thiết lập ở thuộc tính `max="10"`  
4. TH4: Báo lỗi. Vì giá trị "abc123" không khớp với biểu thức chính quy `[0-10].  
5. TH5: báo lỗi. Vì độ dài chuỗi "123" ngắn hơn mức tối thiểu `minlength="8"`.  

So sánh kết quả với dự đoán:  
- TH1: hiện popup "Please fill out this field" 
- TH2: hiện popup "Please include an '@' in the email address" 
- TH3: hiện popup "Value must be les than or equal to 10"
- TH4: hiện popup "Pleasematch the requested format"
- TH5: hiện popup "Please lengthen this text to 8 characters..."


### Câu A3:  
1. - Chỉ dẫn âm thanh: giúp Screen Reader đọc đúng tên ô nhập khi người dùng trỏ tới thay vì chỉ đọc "ô trống"
   - Dễ thao tác: cho phép click vào dòng chữ của label để kích hoạt ô nhập liệu (thuận tiện cho người khuyết tật về vận động hoặc người dùng di động)
2. Dùng `<fieldset>`+``<legend>` khi dùng để nhóm các ô nhập có cùng chủ đề trong 1 form lớn
Ví dụ: Nhóm "Địa chỉ nhận hàng" (gồm số nhà, đường, cơ quan) để người dùng không bị nhầm lẫn với nhóm "Thông tin thanh toán".
3. - `Arial-label` dùng cho các nút chỉ có icon mà không có chữ, để báo cho máy tính biết đó là nút gì.
   - Không dùng khi có `<label>` rồi vì nó gây thừa thãi và có thể ghi đè mất nội dung của `<label>`, làm Screen Reader hoạt động không ổn định.
  
### Câu A4:  
1.Thuộc tính `loading="lazy"`  
- Tác dụng: trì hoãn việc tải ảnh cho đến khi người dùng cuộn trang đến gần vị trí của ảnh đó
- Cải thiện: tốc độ tải trang ban đầu, tiết kiệm băng thông cho người dùng
- không nên dùng cho những ảnh nằm ở đầu trang vì sẽ làm chậm hiển thị ngay lập tức
2. - Cung cấp nhiều thẻ `<source>` trong `<video>` vì mỗi trình duyệt hỗ trợ định dạng video khác nhau.
  Cung cấp nhiều source giúp đảm bảo video chạy được trên mọi trình duyệt. Trình duyệt sẽ chọn file đầu tiên hôc trợ.
  -3 format phổ biến: MP4(H.246), WebM, Ogg
3. Thuộc tính `alt` trên `<image>` dùng để hiển thị thay thế hình ảnh lỗi và giúp Screen Reader đọc mô tả ảnh cho người khiếm thị.
  alt cho 3 trường hợp:
  - Ảnh iPhone 16: `alt="Điện thoại iPhone 16 màu xanh Teal dung lượng 128GB"`
  - Ảnh trang trí: `alt=""`
  - Ảnh biểu đồ Q1/2026: `alt="Biểu đồ doanh thu Quý 1 năm 2026 tăng trưởng 15% so với cùng kỳ"


### Câu A5:  
- Cách 1: dùng cho các ảnh là 1 phần của nội dung nhưng không cần tiêu đề bổ trợ 
hoặc chú thích riêng biệt. Ảnh này thường đi kèm ngay trong đoạn văn hoặc là 1 thành phần giao diện  
Ví dụ: ảnh minh họa trong 1 bài viết, một tấm ảnh chèn giữa đoạn văn mô tả tính năng đề người đọc dễ hình dung
- Cách 2: dùng khi ảnh là 1 đơn vị nội dung độc lập,cần có chú thích đi kèm để giải thích rõ hơn và có thể di chuyển vị trí trong bài mà không làm mất ý nghĩa của đoạn văn xung quang.
- Ví dụ:Trang chi tiết sản phẩm,ảnh chính của sản phẩm kèm theo chú thích về mẫu và giá tiền ngay bên dưới để khẳng định thông 


## Phần C

### Câu C1:  
- Lỗi 1:Dòng 2 - Input "Tên" không có `<label for="...">`, vi phạm accessibility.
  Sửa: `<label for="name">Tên:</label> <input type="text" id="name" name="name" required>
- Lỗi 2:Dòng 4 - Input "Email" thiếu cả nhãn `<label>` và thuộc tính `required`, người dùng Screen Reader không biết đây là ô gì.
  Sửa:`<label for="email">Email:</label> <input type="email" id="email" name="email" required placeholder="Email của bạn">`
- Lỗi 3:Dòng 6 - Input "Mật khẩu" thiếu `minlength` và `required`, dẫn đến rủi ro bảo mật (mật khẩu quá ngắn hoặc trống).
  Sửa:`<label for="pw">Mật khẩu:</label> <input type="password" id="pw" name="pw" required minlength="8" placeholder="Mật khẩu">`
- Lỗi 4:Dòng 7 - Input "Nhập lại mật khẩu" dùng chung thuộc tính với ô trên nhưng thiếu id và label, gây khó khăn cho việc truy cập và so sánh sau này.
 Sửa:`<label for="re-pw">Nhập lại mật khẩu:</label> <input type="password" id="re-pw" name="re-pw" required placeholder="Nhập lại mật khẩu">`
- Lỗi 5:Dòng 9 - Input "Phone" đang dùng `type="text"`, không tối ưu bàn phím số trên mobile và thiếu `pattern` để kiểm tra định dạng.
  Sửa:`<label for="phone">Phone:</label> <input type="tel" id="phone" name="phone" pattern="[0-9]{10}" placeholder="Số điện thoại 10 số">`
- Lỗi 6:Dòng 11 -  Thẻ `<select>` thiếu thuộc tính `name` (dữ liệu không gửi đi được) và các `<option>` thiếu thuộc tính `value`
  Sửa:`<label for="city">Thành phố:</label> <select id="city" name="city"><option value="hn">Hà Nội</option><option value="hcm">TP.HCM</option></select>`
- Lỗi 7:Dòng 16 -  Thẻ `<label>` cho "Điều khoản" không có thuộc tính `for` và thiếu thẻ `<input type="checkbox">` bên trong hoặc liên kết tới.
  Sửa:`<input type="checkbox" id="terms" name="terms" required> <label for="terms">Tôi đồng ý điều khoản</label>`
- Lỗi 8:Cả Form - Thẻ `<form>` thiếu thuộc tính `action` và `method`, dẫn đến việc không xác định được dữ liệu gửi đi đâu và gửi như thế nào.
  Sửa:<form action="#" method="POST">











