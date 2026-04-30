# PHIẾU BÀI TẬP 01

## Phần A

### Câu A1:

1.Các bước xảy ra khi gõ https://Shopee.vn vào trình duyệt  
  b1: DNS Lookup (Phân giải tên miền)  
  b2: TCP Handshake(Thiết lập kết nối)  
  b3: TLS Handshake (thiết lập bảo mật)  
  b4: HTTP Request (gửi yêu cầu)  
  b5: HTTP Response (Máy chủ phản hồi)  
  b6: Parsing & Render Tree (Dịch mã và dựng khung)  
  b7: Painting (iển thị lên màn hình)  
2. Tab Network trong DevTools của Chorme cho thấy:  
  Danh sách các file được tải  
  Trạng thái thành công hay thất bại  
  Kích thước của từng file  
  Thời gian tải của từng request và tổng thời gian load 
  <img width="1057" height="687" alt="Screenshot 2026-04-28 173605" src="https://github.com/user-attachments/assets/4786a96e-f23c-4e53-b5ae-df34e772ffeb" />

### Câu A2:
Trang web bị Google đánh giá SEO thấp vì sử dụng quá nhiều thẻ (div) vô nghĩa và hoàn toàn không sử dụng các thẻ HTML Semantic.  
Các lỗi:  
1.Sử dụng thẻ div thay vì các thẻ cấu trúc (header, main, footer)  
Các khối lớn như: header, main, footer đang dùng thẻ div vô nghĩa. Có thể thay thế bằng thẻ header, main, footer để định vị bố cục chuẩn.
2.Thanh điều hướng menu không dùng thẻ nav và ul  
Sửa thẻ div thành thẻ nav kết hợp với danh sách ul, li để máy biết đây là khu vực chứa các liên kết chính web  
3. Tiêu đề sản phẩm  
Tên sản phẩm "iphone 16 Pro" đang dùng thẻ div. Google không thể nhận diện đây là tên của nội dung  
4. Hình ảnh img thiếu thuộc tính alt

Sửa 
```html
 <header class="header">
    <div class="logo">ShopTLU</div>
    <nav class="menu"> <!--Lỗi 2-->
        <ul>
            <li><a href="/">Trang chủ</a></li>
            <li><a href="/products">Sản phẩm</a></li>
        </ul>
    </nav>
</header>

<main class="main">
    <article class="product">
        <h1 class="title">iPhone 16 Pro</h1>  <!--Lỗi 3-->
        <div class="price">25.990.000 đ</div>
        <div class="image"><img src="iphone.jpg" alt="Điện thoại iPhone 16 Pro chính hãng"></div>  <!--Lỗi 4-->
    </article> 
</main>

<footer class="footer">
    <p>© 2026 ShopTLU</p>
</footer>

```

### Câu A3:  
<img width="2560" height="1973" alt="z7773217026542_4c626a296173962c5cbeaac8554e4d6e" src="https://github.com/user-attachments/assets/edd560e3-e138-407a-945c-801e0aaec971" />


### Câu A4:  
Sự khác nhau:  
`<thead>`:Chứa tiêu đề của bảng(thường chứa các thẻ `<th>`). Luôn luôn hiển thị ở trên cùng  
`<tbody>`:Chứa phần nội dung, dữ liệu chính của bảng. Một bảng có thể có nhiều `<tbody>` để phân chia các nhóm dữ liệu  
`<footer>`: Chứa phần tổng kết hoặc ghi chú ở đáy 

Không nên dùng table để tạo layout trang web vì:
  - Vi phạm quy tắc Semantic và phá hủy SEO
  - Không thể tối ưu hiển thị trên di động
  - Làm chậm tốc độ tải trang



