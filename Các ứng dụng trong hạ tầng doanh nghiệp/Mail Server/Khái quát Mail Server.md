# Mail Server

## Mục lục
[1. Mail Server là gì?](#1)

[2. Cách thức hoạt động của Mail Server](#2)

[2.1. Outgoing Mail Server là gì?](#2.1)

[2.2. Incoming Mail Server là gì?](#2.2)

[3. Tính năng nổi bật của Mail Server](#3)

[4. Phân loại Mail Server](#4)

[4.1. Mail Server Microsoft, Google là gì?](#4.1)

[4.2. Mail Server độc lập là gì?](#4.2)

[5. Tại sao nên sử dụng mail server?](#5)

[6. Các thuật ngữ thường đi kèm Mail Server](#6)

[6.1. TLS Mail Server là gì?](#6.1)

[6.2. SASL Mail Server là gì?](#6.2)


[6.3. Webmail là gì?](#6.3)

[6.4. SMTP-IN Queue là gì?](#6.4)

[6.5. Local Queue là gì?](#6.5)

[6.6. Local Mailboxes là gì?](#6.6)

[6.7. Email Authentication là gì?](#6.7)

[6.8. Mail Exchanger Record (MX) là gì?](#6.8)

[7. Nên đăng ký Mail Server ở đâu?](#7)

[8. Giải pháp thông minh cho nhu cầu sử dụng mail lớn](#8)

[8.1. Giải pháp Email Server riêng là gì?](#8.1)

[8.2. Ưu Điểm](#8)

## Tìm hiểu

<a name="1"> </a>
### 1, Mail Server là gì?

Mail Servr hay còn gọi là Email Server được cấu hình theo tên máy chủ doanh nghiệp để gủi thư và nhận thư điện tử. Bên cạnh những lưu trữ và sắp xếp trên internet, Mai Server là giao thức chuyên nghiệp để giao thư tín, quản lí truyền thông nội bộ, giao dịch thương mại,... Không chỉ thao tác nhanh an toàn và cẩn thận, Mail Server còn dảm bảo tính an toàn và khả năng khôi phục dữ liệu cao

![image](https://user-images.githubusercontent.com/105496635/185019064-ca11356d-bc23-4ee7-9253-d0ee8aa1e3fa.png)

Mail Server cơ bản vẫn là Đedicated Server (là máy chủ riêng) hay máy chủ ảo (Server điện toán đám mây) được cấu hình để biến thành một cỗ máy gửi và nhận thư điện tử. Nó cũng có đầy đủ các thông số như một Server bình thường như Ram, CPU, Storage,… ngoài ra, nó còn có các thông số khác liên quan đến yếu tố Email như số lượng tài khoản Email, Email fowarder, Mail list,…

<a name="2"></a>
### 2, Cách hoạt động của Mail Server 

![image](https://user-images.githubusercontent.com/105496635/185019670-7378533b-af88-4a1d-aadc-0e0d4deeb396.png)

Mail Server hoạt động theo 3 phương thức cơ bản gồm:

<a name="2.1"></a>
#### 2.1 Outgoing Mail Server là gì?
Outgoing Mail Server hay Mail Server gửi đi sử dụng giao thức SMTP (Simple Mail Transfer Protocol). Đây là giao thức dịch chuyển mail đơn giản được dùng để liên lạc với server từ xa. Đồng thời cho phép gửi nhiều thư cùng một lúc tới các server khác nhau.

<a naem="2.2"></a>
#### 2.2 Incoming Mail Server là gì?
 Giao thức này còn biết đến 2 hình thức:
 - POP3 (Post Office Protocol phiên bản 3) chuyển mail lưu ở máy tính Mail Client, thường là nội bộ máy tính thông qua ứng dụng như Outlook, Mac Mail, Windows Mail…
 - IMAP (Internet Message Access Protol): phương thức phức tạp hơn cho phép nhiều client kết nối tới MailBox. Email từ MailBox sẽ được sao cheps tới máy chủ client và bản gốc vẫn đươc lưu trên Mail Server

<a name="3"></a>
### 3, Tính năng nổi bật cảu Mail Server

![image](https://user-images.githubusercontent.com/105496635/185022989-cb15be07-8193-49ff-aac1-cadbd5b8a1e3.png)

Mail Server mang đến cho cá nhân và doanh nghiệp nhiều tính năng :
- Cho phép người dùng gửi Mail hay nhận Mail thông qua Internet với những tên miền cụ thể của từng tổ chức 
- Hạn chế tối đa được spam và chứa virus
- Đảm bảo thông tin nội bộ 
- Có thể thiết lập riêng bộ nhớ cho người dùng Mail Server
- Quản lí được toàn bộ nội dung mail của tất cả thành viên
- Thiết lập được chức năng sao lưu tự động. Đảm bảo luôn cần thông tin cần thiết


<a name="4"></a>
### 4, Phân loại Mail Server 
Mail Server có vai trò quan trọng trong quá trình kinh doanh của doanh nghiệp

<a name="4.1"></a>
#### 4.1. Mail Server Microsoft, Google là gì?
Mail server Microsoft và Google là 2 cái tên lớn đại diện cho dịch vụ này. Nền tảng xây dựng loại server mail này có quy mô lớn, hệ thống bảo mật chặt chẽ. Có thể quản lý tốt những dữ liệu hiện có. Người dùng có thể sử dụng được nhiều tiện ích khác nhau. Cũng chính vì thế mà giá cả sử dụng dịch vụ server mail loại này thường khá cao. Ví dụ: Email 365 (Microsoft), G Suite (Google),….Tuy nhiên giá cả của các dịch vụ này thường rất đắt, giá trung bình khoảng 5USD/Email /tháng, nếu doanh nghiệp của bạn có số lượng email lớn thì chi phí duy trì hàng tháng rất lớn.
<a name="4.2"></a>
#### 4.2. Mail Server độc lập là gì?
Mail Server độc lập là hệ thống Mail Server được thiết kế cho các tổ chức hoặc ISP xử lý khối lượng thư lớn, yêu cầu kiểm soát và linh hoạt hơn đối với các dịch vụ thư. Nó bổ sung các tính năng như hợp tác, đồng bộ hóa Outlook, quản trị từ xa, Webmail và Quản trị Web nâng cao hơn và kết nối cơ sở dữ liệu, cung cấp cho bạn sức mạnh và kiểm soát cần thiết cho các hoạt động quy mô lớn.
 
<a name="5"></a>
### 5, Tại sao nên sử dụng Mail Server

![image](https://user-images.githubusercontent.com/105496635/185024965-1ed96be3-15b5-4937-93e5-b77cafd32cda.png)

Bởi tình trạng spam mail, email gửi kèm những phần mềm độc hại đã làm ảnh hưởng đến tình hình an ninh mạng tại Việt Nam. Vì thế, việc bảo mật và an toàn luôn là vấn đề nhiều doanh nghiệp quan tâm. Và điều này đã khiến Mail Server được đánh giá cao hơn cả so với những máy chủ mail khác.

- Email với tên miền riêng của riêng công ty thể hiện sự chuyên nghiệp trong hoạt động.
- Tốc độ, bảo mật cao, kèm theo nhiều tiện ích.
- Kiểm tra mail mọi nơi: tại văn phòng (thông qua phần mềm duyệt mail) và tại bất kỳ nơi đâu (khi đi công tác), trên tất cả các loại trình duyệt mail (Outlook…)
- Có thể tùy biến các thông số và chức năng cho từng User.
- Ngăn chặn spam và virus cực kỳ hiệu quả.
- Có không gian lưu trữ riêng biệt, bất khả xâm phạm.
- Tính bảo mật cao nhờ trang bị giao thức SSL.
- Sử dụng IP riêng nên sẽ chống được việc vô cớ bị vào black list.
- Hỗ trợ tính năng Fowarder Email để cài đặt Email Offline.


<a name="6"></a>
### 6, Các thuật ngữ đi kèm với Mail Server

<a name="6.1"></a>
#### 6.1, TLS Mail Server là gì?
TLS là truyền tải thông tin (Transport Layout Security) TLS được hoạt động cùng với  tầng bảo mật SHL (Secure Sockets Layer ). Mục đích chính cung cấp phương thức vận tải di chuyển mã hóa cho đăng nhập chứng thực SASL

<a name="6.2"></a>
#### 6.2 SASL Mail Server là gì?
SASL là lớp xác thực và bảo mật đơn giản (Simple Authentication and Security Layer). Để xác thực người dùng. SASL thực hiện xác thực, sau đó TLS cung cấp vận chuyển mã hoá dữ liệu xác thực.


<a name="6.3"></a>
#### 6.3 Web Mail là gì?
Webmail là email trên nền website. Một số webmail mà các bạn có thường thấy như hotmail, gmail, yahoo mail. Webmail cho phép người dùng truy cập email bất cứ lúc nào.
<a name="6.4"></a>
#### 6.4 SMTP-IN Queue là gì?
Trước khi phân tán thư đến các Local queue hoặc Remote Queue, giao thức SMTP sẽ làm một thao tác sao lưu toàn bộ thư điện tử gửi đi từ email server của doanh nghiệp ở SMTP-IN Queue. Nói cách khác, SMTP-IN Queue chính là kho lưu trữ thông tin thư từ trước khi được gửi đi.

<a name="6.5"></a>
#### 6.5. Local Queue là gì?
Sau khi tiếp nhận thông tin thư từ, hệ thống sẽ tự động điều phối phân loại và xếp thư từ theo thứ tự ngay hàng thẳng lối trước khi chuyến vào hộp thư của người nhận. Việc xếp hàng các bức thư chính là Local Queue.

Để tăng cường khả năng bảo mật và giữ an toàn cho hệ thống email server, trước khi thư được gửi đến người dùng, local queue và remote queue sẽ tiến hành quét virut. Sau đó kiểm tra spam để chắc chắn về chất lượng thư gửi đi. Tránh trường hợp mail server bị các Blacklist liệt vào danh sách IP spam.


<a name="6.6"></a>
#### 6.6. Local Mailboxes là gì?
Local Mailboxes là hộp thư của các account có đăng kí tài khoản mail server của công ty.



<a name="6.7"></a>
#### 6.7. Email Authentication là gì?
Email Authentication là tính năng xác nhận danh tính của các user khi truy cập vào hộp thư email. Tính năng này giúp bạn bảo mật thông tin thư từ của chính mình. Nói cách khác Alternate Email là một dạng email dự phòng. Khi quên mật khẩu của mail server, bạn có thể sử dụng email này để giúp bạn lấy lại mật khẩu một cách nhanh chóng.

<a name="6.8"></a>
#### 6.8. Mail Exchanger Record (MX) là gì?
MX record có nhiệm vụ là chỉ đường cho email đi đến mail server của bạn. MX record thường đi kèm theo một A record sẽ trỏ về địa chỉ IP của mail server. Một thông số pref có giá trị số để chỉ ra mức độ ưu tiên của các mail server. Giá trị pref càng nhỏ thì mức độ ưu tiên càng cao.


<a name="7"> </a>

#### 7. Nên chọn mua Mail Server ở đâu

Với những nhà cung cấp dịnh vụ hiện nay thì chúng ta không thể thiếu những nhà cung cấp hàng đầu
Ví dụ như nhanhoa.com

<a name ="8"></a>
### 8. Giải pháp thông minh cho nhu cầu sủ dụng Mail Server

<a name ="8.1"></a>
#### 8.1, Giải pháp Email riêng 

- Giải pháp máy chủ Email rieegn dành cho doanh nghiệp

Xây dựng hệ thống Mail trên máy chủ Linux siêu tốc và an toàn hơn so với một số hệ điều hành khác như Window 
Đáp ứng đầy đủ về tính riêng tư và thuowgn hiệu doanh nghiệp


<a name ="8.2"></a>
#### 8.2. Ưu Điểm
- Server mail riêng biệt, Miễn phí 1 IP riêng
- Khả năng xứ lý với Email số lượng lớn hàng ngày
- Hệ thống mail bảo mật
- Control Panel quản lý và tạo Email cho nhân viên
- Thiết lập được dung lượng tối đa của từng Email
- Check Email được trên cả 2 trên Outlook Express(tại văn phòng công ty) hay Web Mail(khi đi công tác)
- Hỗ trợ Forwarder Email để setup Email Offline
- Nhân viên có thể tự thay đổi password riêng
- Kiểm tra được nội dung Email của nhân viên hay trưởng phòng
- Chống được virus cực kỳ hiệu quả
- Chống bị Spam mail cực kỳ hiệu quả
- Chống bomb mail















