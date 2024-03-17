Đọc code : 
<img width="644" alt="image" src="https://github.com/shinyluck/CBJS/assets/76943559/cc8109bf-8b6a-45dc-b944-709f72f58875">

Ta thấy đuôi file đã bị filter bằng cách lấy đúng extension cuối, chặn các đuôi file thực thi như php", "phtml", "phar" . Thử upload các đuôi khác , ta thấy các đuôi file khác đều không phải là đuôi file thực thi 
-> Cần hướng khác

Dùng trick lỏ upload file htaccess ( bỏi vì không whitelist đuôi file) , thay đổi extension thực thi file php 


