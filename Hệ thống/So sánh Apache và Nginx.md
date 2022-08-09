# Khái quát
## Apache là gì?
 Apache tên gọi đầy đủ là Apache HTTP Server. Đây là một web server mã nguồn mở miễn phí và được sử dùng phổ biến hiện nay. Nếu sử dụng Apache, ban chỉ cần thao tác đơn giản 
là nhập URL hoặc IP và ấN Enter thì server sẽ tiếp nhận URL hoặc IP mà ban đã nhập

![image](https://user-images.githubusercontent.com/105496635/183541904-0c6afb1d-5350-45c8-96da-f8101a37499f.png)

 Apache hoạt động tốt trên các hệ điều hành phổ biến hiện nay như Windows, Linux, Unix, Novell Netware cùng các hệ điều hành khác
 
 
 ## Nginx là gì ?
 
 - Nginx, đọc là "engine e-x", là một phần mềm web mã nguồn mở. Ban đầu nó dùng để phục vụ web HTTP. Tuy nhiên ngày nay nó dùng để phục vụ everse proxy, HTTP load 
balancer và email proxy như IMAP, POP3, và SMTP.

![image](https://user-images.githubusercontent.com/105496635/183542833-21e775e4-986b-4bab-9d61-27b816f0d6a0.png)


# So sánh Nginx và Apache
- Đặc điểm
 -  CÓ thể nói Apache và Nginx đều rất coi trọng bảo mật,

||Apache|Nginx||
|-|-|-|-|
|Vai trò|||Kết luận|
|Mức độ phổ biến|- Năm 2012 tổng số web sử dụng Apache chiếm hơn 65% |- Năm 2012 chiếm khoảng 44%|Với thời đại phát triển thì người dùng chuyển sang Nginx nhiều hơn nên con số này không chênh lệch quá cao|
|Tốc độ|- Tốc độ truy cập vào web sử dụng Apache còn sử lí chậm hơn, nên cần được cải thiện|- Trái lại với Apache, Ngin được xếp hạng là nhanh chống hơn|
|Kết nối đồng thời|![image](https://user-images.githubusercontent.com/105496635/183549067-4d38181d-8d99-48c2-95ca-0627d02c79f5.png)|![image](https://user-images.githubusercontent.com/105496635/183549108-52682f28-8584-40ee-be09-533dedc616cc.png)| Đối với 25 người dùng ảo, trang web Nginx có thể ghi 200 yêu cầu mỗi giây, cao hơn 2,5 lần so với Apache (80 yêu cầu mỗi giây). Rõ ràng, nếu bạn có một trang web lưu lượng truy cập cao chuyên dụng, Nginx là một lựa chọn an toàn hơn.|
|Tính linh hoạt|Với vieevj sử dụng .htaccess nên Apache có thể linh hoạt tùy chỉnh|Nginx không hỗ trợ .htaccess||
|Các thông số khác|||Trước đây, Nginx không hỗ trợ tốt lắm cho hệ điều hành Windows, không giống như Apache. Tuy nhiên, điều này không còn nữa. Ngoài ra, Apache cũng từng bị coi là khá yếu về cân bằng tải và reserve proxy. Nhưng mọi thứ bây giờ đã thay đổi|
||||Với những so sánh trên thì thấy được cả hai dạng máy chủ thì vẫn dùng hữu ích theo cách riêng của chúng ta|


# Apache và Nginx nên sử dung máy chủ nào
Cả hai webserver hiện nay, đều có thể cạnh tranh với nhau trong hầu hết các tiêu chí.

Đối với nội dung tĩnh NGINX là vua, nhưng đối với nội dung động nó kém hơn một chút.

NGINX nổi bật với một số tính năng cao cấp của nó (media streaming, reverse proxying for non-HTTP protocols)

Người dùng shared hositng có thể thích sự tiện lợi của file .htaccess Apache.

Và Apache có khá nhiều dynamic module (NGINX mới chỉ bắt đầu thêm dynamic module)

NGINX được sử dụng chủ yếu cho VPS hosting, dedicated hosting, hoặc container cluster.

Với các website có lượt truy cập cao có nhu cầu phục vụ rất nhiều nội dung tĩnh và / hoặc streaming media sẽ hướng tới NGINX.

Nhưng đa phần cả 2 sẽ hoạt động tốt trong hầu hết mọi trường hợp

Bất kể với web server nào, hãy chọn một nhà cung cấp hosting tốt nhất trên nền tảng Linux.

Với VPS tôi khuyên bạn nên dùng Vultr, còn với Shared hosting Bluehost, HawkHost đều đáng sử dụng.

