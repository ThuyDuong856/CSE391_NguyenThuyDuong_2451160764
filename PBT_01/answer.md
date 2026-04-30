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

## Phần B

### Câu 3:  
-lỗi 1: Dòng 1- Thiếu từ khóa html trong DOCTYPE - Cách sửa: Sửa thành `<!DOCTYPE html>`  
- Lỗi 2: Dòng 2-Thiếu thuộc tính ngôn ngữ - Cách sửa:thên `<html lang="vi"`
- Lỗi 3: Dòng 4-Thẻ `<title>` chưa được đóng - Cách sửa:thêm `</title>`
- Lỗi 4: Dòng 5-Sai giá trị charset - Cách sửa:Sửa thành utf-8
- Lỗi 5: Dòng 8-Thẻ `<h1>` đóng sai cú pháp - Cách sửa: đổi `<h1>` ở cuối thành`</h1>`
- Lỗi 6: Dòng 10-Đặt `<header>` bên trong `<body>` sau thẻ`<h1>` - Cách sửa:đưa `<h1>` vào trong `<header>`
- Lỗi 7: Dòng 12-Thẻ `<a>` đóng sai- Cách sửa: đổi `<a>` thành `</a>`
- Lỗi 8: Dòng 18-Thuộc tính src thiếu dấu ngoặc kép- Cách sửa: sửa thành `src="iphone.jpg"`
- Lỗi 9: Dòng 20- Thẻ `<b>` và `<p>` đóng sai thứ tự- Cách sửa: sửa thành `<b>25.990.000đ</b></p>`
- Lỗi 10: Dòng 25- Dùng thẻ `<td>` cho tiêu đề bảng - Cách sửa: đổi sang thẻ `<th>`
- Lỗi 11: Dòng 35- Sử dụng 2 thẻ `<main> trên cùng 1 trang - Cách sửa: đổi thẻ `<main>` thứ 2 thành `<aside>`
- Lỗi 12: Dòng 39- Thẻ `<p>` trong footer chưa đóng- Cách sửa: thêm `</p>`

### Câu 4:  
2. Trong thẻ element table hiển thị:
   - Nội dung: bảng thông số kỹ thuật của iPhone
   - có dùng thẻ `<tbody>` và không dùng thẻ `<thead>`
3.   
- Form đó có: action:`/tim-kiem`, method: `get` (vì không hiện nên mặc định là get)
- input type được dùng: `type="text"`, `type="submit"`

## Phần C  
### Câu C1:  
```html
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chi tiết sản phẩm</title>
</head>
<body>
    <!-- Header: Chứa logo, tìm kiếm và điều hướng chính -->
    <header>
        <div class="logo">...</div>
        <nav aria-label="Main Navigation"> <!-- nav vì đây là khu vực điều hướng chính của website -->
            <ul>
                <li><a href="#">Danh mục</a></li>
                <li><a href="#">Khuyến mãi</a></li>
            </ul>
        </nav>
    </header>

    <main> <!-- main vì đây là nội dung chính, duy nhất của trang này -->
        
        <!-- Breadcrumb -->
        <nav aria-label="breadcrumb"> <!-- nav để trình đọc màn hình hiểu đây là thanh điều hướng phụ -->
            <ol> <!-- ol vì breadcrumb là danh sách có thứ tự từ cấp cao xuống thấp -->
                <li><a href="/">Trang chủ</a></li>
                <li><a href="/mobile">Điện thoại</a></li>
                <li aria-current="page">iPhone 16</li> <!-- aria-current để đánh dấu trang hiện tại -->
            </ol>
        </nav>

        <!-- Container chính của sản phẩm -->
        <section class="product-container"> <!-- section để gom nhóm các thành phần liên quan đến 1 chủ đề -->
            
            <!-- Khu vực ảnh sản phẩm -->
            <aside class="product-gallery"> <!-- aside vì đây là nội dung bổ trợ (hình ảnh) cho phần thông tin chính -->
                <figure> <!-- figure dùng để chứa ảnh có kèm chú thích hoặc nhóm ảnh liên quan -->
                    <img src="img1.jpg" alt="iPhone 16 mặt trước">
                    <!-- ... 4 ảnh còn lại -->
                    <figcaption>Hình ảnh chi tiết iPhone 16</figcaption> <!-- figcaption để chú thích cho nhóm ảnh -->
                </figure>
            </aside>

            <!-- Thông tin sản phẩm -->
            <article class="product-info"> <!-- article vì đây là nội dung độc lập, có thể mang đi nơi khác vẫn đủ nghĩa -->
                <h1>Tên sản phẩm iPhone 16</h1> <!-- h1 vì đây là tiêu đề quan trọng nhất của trang -->
                <p class="price">25.000.000đ</p> <!-- p cho các đoạn văn bản/thông tin ngắn -->
                <div class="rating"> <!-- div dùng để gom nhóm trang trí (sao) không mang ý nghĩa văn bản -->
                    <span>4.5/5 sao</span>
                </div>
                <section class="description">
                    <h2>Mô tả sản phẩm</h2> <!-- h2 cho tiêu đề phụ trong bài viết -->
                    <p>Mô tả tóm tắt về các tính năng nổi bật...</p>
                </section>
            </article>

            <!-- Bảng thông số kỹ thuật -->
            <section class="specifications">
                <h2>Thông số kỹ thuật</h2>
                <table> <!-- table vì đây là dữ liệu có cấu trúc hàng và cột -->
                    <tr>
                        <th>Màn hình</th> <!-- th cho tiêu đề của hàng/cột -->
                        <td>OLED 6.1 inch</td> <!-- td cho dữ liệu trong ô -->
                    </tr>
                    <tr>
                        <th>Chip</th>
                        <td>A18 Bionic</td>
                    </tr>
                </table>
            </section>

            <!-- Khu vực đánh giá/bình luận -->
            <section id="reviews">
                <h2>Đánh giá từ khách hàng</h2>
                <article class="comment"> <!-- Mỗi bình luận là một article độc lập -->
                    <header>
                        <strong>Người dùng A</strong> <!-- strong để nhấn mạnh tên người dùng -->
                        <time datetime="2024-10-20">20/10/2024</time> <!-- time để máy tính hiểu chính xác định dạng thời gian -->
                    </header>
                    <p>Sản phẩm rất tốt!</p>
                </article>
            </section>

        </section>

        <!-- Sidebar: Sản phẩm tương tự -->
        <aside class="related-products"> <!-- aside vì đây là nội dung liên quan nhưng nằm ngoài luồng chính của sản phẩm -->
            <h2>Sản phẩm tương tự</h2>
            <ul> <!-- ul vì danh sách sản phẩm gợi ý không cần thứ tự ưu tiên -->
                <li><a href="#">iPhone 15 Pro</a></li>
                <li><a href="#">Samsung S24</a></li>
            </ul>
        </aside>

    </main>

    <!-- Footer -->
    <footer> <!-- footer chứa thông tin cuối trang như bản quyền, liên hệ -->
        <p>&copy; 2024 Cửa hàng công nghệ. All rights reserved.</p>
        <address> <!-- address dùng cho thông tin liên hệ của chủ sở hữu -->
            Địa chỉ: 123 Đường ABC, Hà Nội.
        </address>
    </footer>
    
</body>
</html>
```
### Câu C2:  

Quan điểm "dùng `<div>` cho mọi thứ" là 1 tư duy thiên về hiển thị hình ảnh mà bỏ qua các giá trị cốt lõi của web là dữ liệu và khả năng tiếp cận. Việc sử dụng các thẻ semantic HTML thật sự hữu ích bởi:  
- Về mặt SEO, các công cụ thìm kiếm như Google dựa vào các thẻ ngữ nghĩa để hiểu cấu trúc nội dung. Thẻ `<main>`, `<article>`,... đóng vai trò như  những nhãn dán chỉ dẫn đâu là nội dung quan trọng nhất. Nếu chỉ dùng `<div>`, Google sẽ mất nhiều thời gian hơn để phân tích, dẫn đến việc xếp hạng trang web không tối ưu.
- Tính tiếp cận: có những người dùng khiếm thị sử dụng trình đọc màn hình dựa vào các thẻ `<nav>`, `,button>` hay `<header>` để phân biệt các phần của trang. Vậy nên 1 website toàn `<div>` sẽ khiến họ lạc lối vì không có điểm mốc định vị.
- Ví dụ: khi bạn dùng thẻ `<button>` thay vì `<div class="btn">` trình duyệt sẽ tự cung cấp các tính năng mặc định như cho phép nhấn bằng phím Enter/Space, tự động nhận tiêu điểm khi dùng phím Tab. Nếu dùng `<div>`, bạn phải viết thêm rất nhiều để tái lập lại những hành vi này, điều này sẽ trở nên tốn thời gian
- Tuy nhiên, `<div>` vẫn là lựa chọn phù hợp nhất trong các trường hợp thuần về dàn trang. Khi bạn cần một lớp bao quanh để tạo các hiệu ứng đồ họa mà lớp đó không mang ý nghĩa nội dung lúc này`<div>` là thẻ an toàn nhất.
