# WebServer
- WebServer là máy chủ được cài đặt các chương trình phục vụ các ứng dụng web. Webserver có khả năng tiếp nhận các request và gửi phản hồi đến client thông qua các giao thức http hoặc các giao thức khác. Có nhiều web server khác nhau như Apache, Nginx, ISS,
- Webserver được dịch ra là máy chủ, mỗi máy chủ có một IP khác nhau và có thể đọc được ngôn ngữ * .htm, * .html... Máy chủ cho phép một trang web để xem HTTP,HTTP(HyperText Transfer Porotol) là giao thức chuyển dữ liệu lên web.
- Webserver phải là một máy tính có dung lượng lớn, tốc độ rất cao để lưu trữ dữ liệu web. Nó điều hành trơn chu cho một máy tính hoạt động trên Internet, thông qua các cổng giao tiếp riêng biệt của máy chủ. Các web server này phải hoạt động liên tục để cung cấp dữ liệu cho mạng máy tính của mình
#### Web server hoạt động
   ![image](https://user-images.githubusercontent.com/105496635/184080316-7f7f21b3-9967-4f85-b0c8-045bd061a16f.png) 
   Bất cứ khi nào bạn xem một trang web trên internet, có nghĩa bạn đang yêu cầu nó từ một trang webserver. Khi nhận được URL nó sẽ tiến hành gửi thông tin mà mình yêu cầu đến server để phản hồi lại

## 1. Những phần quan trọng của web Server
- Về phần cứng:
Máy chủ web server sẽ được kết nối với internet và truy cập bằng một tên miền giống như mozilla.org. Đây cũng là nơi lưu trữ các file thành phần của một website (như file ảnh, CSS, Javascript và HTML). Và có thể chuyển chúng tới thiết bị người dùng cuối cùng.
- Về phần mềm 

Web server sẽ bao gồm những phần để điều khiển người dùng truy cập tới các file lưu trữ trên một HTTP server. Một HTTP server là một phần mềm có thể hiểu được các URL và giao thức trình duyệt đang sử dụng. Bất cứ lúc nào trình duyệt cần đến file dữ liệu trên máy chủ. Trình duyệt sẽ gửi yêu cầu file đó thông qua HTTP. 

Với phần cứng và phần mềm bạn có thể xây dựng được một web server ở mức đơn giản hoặc cầu kì để sử dụng cho mình. 

## 2. Chức năng của Web Server 
- Xử lí dữ liệu thông qua giao thức HTTP: Xử lí nhà cung cấp thông tin cho khách hàng thông qua các máy tính cá nhân thông qua các giao thức http. Nội dung được chia sẻ từ máy chủ web  là những nội dung định dạng HTML. Các thẻ style sheets, hình ảnh, những đoạn mã script hỗ trợ nội dung văn bản thôi…. Bạn có thể hiểu đơn giản là khi bạn truy cập vào Bizfly.vn. Máy chủ sẽ cung cấp đến cho bạn tất cả dữ liệu về trang web đó thông qua lệnh giao tiếp.
- Kết nối linh hoạt: Máy tính nào nó cũng là máy chủ, nếu nó cài phần mềm server và có mạng internet
- Chương trình chuyển đổi thông minh: Phần mềm web cũng như các phần mềm khác. Cho phép nguoif dùng cài đặt hoạt động trên các máy tính có khả năng 
- Lưu dữ liệu trên các hình thức thuê các máy chủ nhỏ hoặc thuê VPS hoặc hosting

## 3. Cách WebServer trao đổi với người dùng
1. Trình duyệt phân giải tên mình thành địa chỉ IP
- Trình duyệt web của bạn trước tiên phải xác định địa chỉ IP tên miền đã trỏ về. Trình duyệt sẽ yêu cầu thông tin từ một hoặc nhiều máy chủ DNS. Máy chủ DNS sẽ cho trình duyệt biết địa chỉ IP nào tên miền sẽ trỏ đến cũng là nơi đặt trang web
- Lúc này này trình duyệt web đã biết thông tin địa chỉ IP của Web và nó yêu cầu URL để từ Webserver 
2. WebServer gửi lại client Trang yêu cầu
Web Server nó sẽ gửi thông tin từ Client yêu cầu. Nêu nó không tồn tại nó sẽ gửi thông báo phù hợp
3. Trình duyệt hiện thị Web   
- Trình duyệt bạn sẽ hiển thị các tập tin như html,css và render hiển thị trang theo yêu cậu

## 4. Cách thức để công khai một trang web
- Muốn công khai một trang web bất kỳ, bạn luôn cần đến máy chủ web tĩnh và máy chủ web động.
- Máy chủ web tĩnh: Thường là một server kèm theo HTTP server. Sở dĩ gọi server tĩnh là bởi đơn giản file gửi đến không hề thay đổi tình trạng web.
- Máy chủ web động: Gồm một máy chủ web tĩnh kèm theo một số phần mềm mở rộng.
- Mỗi khi xây dựng một trang web cuối, bạn dễ dàng quan sát application server tự động điền đầy đủ nội dung vào HTLM tempate. Tuy nhiên, đó không phải tài liệu thực.

## 5. Cách thức lưu trữ file và giao tiếp thông qua HTTP trong web server

![image](https://user-images.githubusercontent.com/105496635/184089250-46fec7c3-e0ca-4c70-866c-f47186c34e20.png)

Web server có nhiệm vụ chính là thực hiện lưu trữ file của website
Trong quá trình tìm hiểu web server là gì, bạn cần lưu ý tham khảo cơ chế lưu trữ và giao tiếp thông qua HTTP.

## 6. Cách lưu trữ các file
Web server có nhiệm vụ chính là thực hiện lưu trữ file của website. Bao gồm toàn bộ file HTML và một số file liên quan khác. Xét trên khía cạnh kỹ thuật, tất cả file đều có thể lưu trên máy tính. Thế nhưng nếu muốn thuận lợi hơn, bạn nên lưu trữ chúng trên web server.
## 7.Giao tiếp thông qua HTTP
Ngoài chức năng lưu trữ, web server còn có thể giao tiếp thông qua HTTP. Cụ thể, HTTP hỗ trợ cách thức truyền siêu văn bản giữa hai thiết bị. Hãy hiểu đơn giản nó là tập hợp nhiều quy tắc truyền thông giữa hai thiết bị, cụ thể ở đây là hai máy tính. HTTP giống như giao thức nguyên văn, không phân cấp.
- Textual: Gồm toàn bộ lệnh văn bản thuần túy, người dùng dễ dàng đọc.
- Stateless: Gồm máy chủ và máy khách không lưu lại thao tác thực hiện trước đó.
HTTP đề ra quy tắc rõ ràng với cả người dùng và hệ thống máy chủ giao tiếp. Như vậy trong quá trình thực hiện giao tiếp, bạn cần ghi nhớ một vài điểm dưới đây.
- Chỉ máy khách mới có quyền người yêu cầu đến máy chủ. Đồng thời, chỉ có máy chủ có thể phản hồi yêu cầu của máy khách.
- Nếu tiến hành gửi một file qua HTTP, máy khách phải cung cấp chính xác URL của file.
- Máy chủ web có trách nhiệm phản hồi tất cả yêu cầu HTTP, đặc biệt là thông báo lỗi.
Trên hệ thống máy chủ web, máy chủ HTTP cần thực hiện xử lý và phản hồi yêu cầu. Khi yêu cầu gửi đến, máy chủ HTTP thứ nhất cần kiểm tra URL xem có khớp với file hay không. Nếu khớp, máy chủ lập tức gửi nội dung file về trình duyệt. Trường hợp không khớp, máy chủ sẽ tạo file phù hợp.


## Apache HTTP server
- Apache là gì? Web server Apache là phần mềm nổi tiếng trên thế giới được phát triển bởi Quỹ Apache Software. Đây là phần mềm có mã nguồn mở, hỗ trợ hầu hết các hệ điều hành như Windows, Mac OS X, FreeBSD, Unix, Linux,... Trên thế giới có khoảng hơn 60% máy tính chạy trên phần mềm này.
- Phần mềm máy chủ Apache có cấu trúc dạng module nên thực hiện rất dễ dàng. Người dùng có thể sửa đổi, bổ sung các module khác vào server (nếu cần).

## Web server Nginx
Nginx là gì? Web server Nginx là một gợi ý tiếp theo về một máy chủ có mã nguồn mở miễn phí. Phần mềm bao gồm máy chủ POP3 và IMAP. Có ưu điểm là tính ổn định, hiệu suất cao, cấu hình thân thiện và sử dụng tài nguyên thấp. Nó sử dụng kiến trúc lập trình theo sự kiện, có khả năng mở rộng để xử lý các yêu cầu chứ không dùng các chuỗi phức tạp. Nginx hiện đang lưu trữ khoảng 7.5% các tên miền trên khắp thế giới.

![image](https://user-images.githubusercontent.com/105496635/184092442-bedfb532-7f26-4791-b3a4-f62188292c5c.png)


## Web server IIS
IIS là gì? Web server IIS là một sản phẩm của Microsoft và cũng có nhiều tính năng tương tự như Apache bên trên. Tuy nhiên, nó không phải là mã nguồn mở cũng như việc chỉnh sửa các module không hề đơn giản.

![image](https://user-images.githubusercontent.com/105496635/184092528-1ad7e313-85f6-4a8e-bf64-e31ac15caa6d.png)

## Web server CentOS
CentOS là viết tắt của Community Enterprise Operating System (Hệ điều hành Doanh nghiệp Cộng đồng). Một trong những Bản phân phối Linux do Gregory Kurtzer khởi xướng. Nó cung cấp Hệ điều hành nguồn mở và miễn phí cấp doanh nghiệp. Cũng tương thích về chức năng với Red Hat Enterprise Linux (RHEL). Các nhà phát triển CentOS sử dụng mã nguồn RHEL và tạo ra một sản phẩm rất giống với nó. Hỗ trợ kỹ thuật cho CentOS chỉ được cung cấp thông qua cổng thông tin cộng đồng và web.

![image](https://user-images.githubusercontent.com/105496635/184271972-ed07b343-7ca6-4b28-8d0d-2eda2a822763.png)

## Web server LiteSpeed
Web server LiteSpeed có rất nhiều tính năng giống như Apache. LiteSpeed có khả năng tải các file cấu hình Apache trực tiếp đồng thời hoạt động như một Drop-in Replacement Apache với các Control Panel của Hosting. LiteSpeed có thể được thay thế với web server Apache trong khoảng 15 phút với Downtime bằng 0. Web server LiteSpeed còn có khả năng thay thế tất cả tính năng của Apache và đơn giản hóa việc sử dụng.

![image](https://user-images.githubusercontent.com/105496635/184274613-15e0d1bc-5595-4d13-a7bf-3af021bb29fb.png)

