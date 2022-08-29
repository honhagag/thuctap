# I. SMTP
## 1. SMTP là gì?
- SMTP (Simple mail Tranfer Protocol) là giao thức gửi thư đơn giản hóa. Như vậy, nhìn vào tên cũng thấy được chức năng chính của SMTP chính là gửi mail. Còn nhận mail, truy xuất dữ liệu về mail sẽ có giao thức IMAP hay POP3 đảm nhận trách nhiệm .
- Việc gửi mail được giao thức SMTP thực hiện thông qua TCP hoặc IP vì vậy người dùng có thể an tâm hề khả năng bảo mật và tính tiện
- Sử dụng giao thức SMTP giúp người dùng nâng cao hiệu suất làm việc. Bởi chúng ta hỗ trợ việc gửi lượng lớn thư viện điện tử chỉ trong thời gian ngắn. Nhờ thế người dùng tiết kiệm thời gian và công sức gửi thư thủ công
- Giao thức SMTP còn cho phép gửi tệp tin đánh kèm với khả năng lưu trữ lớn
- Port mặc định
   - 25 - không mã hóa
   - mã hóa SSL/TLS - SMTPS

![image](https://user-images.githubusercontent.com/105496635/187155450-8080806f-685c-419c-8993-148b085c3d31.png)

## 2. SMTP Server là gì
- Máy chủ SMTP là một dịch vụ gửi email số lượng lớn với tốc độ cao mà không giới hạn. Cũng có thể hiểu đơn giản, máy chủ giúp người dùng thực hiện thao tác gửi thư. Hiện này các hộp máy chủ miễn phí như Gmail hay hộp thư email đi kèm hosting
- Thông thường, máy chủ SMTP gửi thư thông qua port 45. Tuy nhiên ở Châu Âu, phương thức được sử dụng rộng rãi, thay thế cho SMTP của Gmail là x400. Ngoài ra còn có nhiều máy chủ gửi mail hỗ trợ phương thức mở rộng là ESMTP. Đây là giao thức gửi tập tin hỗ trợ với nhiều tập tin đa phương tiện dưới dạng một cách đơn giản, nhanh chống
- Khi ta sử dụng hệ thống Email, người dùng cần hiểu rõ phương thức được hỗ trợ để nâng cao hiệu xuất, khai thác tối đa các chức năng của chúng, từ đó tạo ra một email chuyên nghiệp. Bên cạnh đó người dùng cũng chú ý đến khả năng gửi tập tin, các loại định dạng file đã gửi, dung lượng lưu trữ. Tất cả giúp tạo nên tạo nên một tổng thể hoàn hảo giải pháp trao đổi thông tin qua  email doanh nghiệp

## 3. Phương thức hoạt động của của SMPT là gì 

- Hình dưới là mô hình quản lí mail khi dùng SMTP 

![image](https://user-images.githubusercontent.com/105496635/187160768-99c11085-f8af-4660-a6a3-b5320257cd71.png)

- Email được gửi lời mời bởi mail client và tác nhân người dùng (Mail User Agent - MUA)đến mail server là tác nhan gửi thư, sử dụng  SMPT trên port 587. Những nhà cung cấp mail box vẫn cho phép người dùng sử dụng port 25

- Agent - MSA),sử dụng SMTP trên port TCP 587. Những nhà cung cấp mail box vẫn cho phép gửi thư trên port truyền thống 25.
- MSA gửi thư đến đại lí truyển thư (Mail transfer Agent - MTA). Thông thường, 2 tác nhận này là đều xuất phát từ cùng một phần mềm được khởi chạy với các tùy chọn khác nhau trên cùng một máy. Quá trình xử lí cục bộ có thể được thực hiện trên một máy vật lí duy nhất.
- MTA sử dụng DNS để tra cứu MX record cho miền của người nhần (phần bên phải của @). MX record chứa tên MTA của mục tiêu. Dựa trên server đích và các yếu tố khác, - - MTA sẽ chọn máy chủ người nhận và kết nối với nó để hoàn tất quá trình trao đổi thư.
- Việc truyền thư có thể xảy ra trong một kết nối duy nhất giữa 2 MTA hoặc qua 1 chuỗi các hệ thống trung gian.
- Tại bước cuối cùng, thư được giao cho đại lí chuyển phát thư (Mail Delivery Agent) để chuyển về local. MDA lưu thư dưới dạng mailbox có liên quan. Cũng như khi gửi, việc tiếp nhận này có thể được thực hiện bằng một hoặc nhiều máy tính.
- Sau khi được gửi đến máy chủ thư cục bộ, thư được lưu trữ để truy xuất hàng loạt bằng mail client đã xác thực (MUA).

## 4. Lợi ích của SMTP

- Giao thức SMTP mang lại cho người dùng 3 lợi ích chính
    - Tăng tỉ lệ thành công hơn khi gửi mail 
    - Người dùng không cần  cài đặt máy chủ nếu dùng hosting
    - Hầu hết email của người dùng đều được đánh dấu mail an toàn. Vì thế, số lượng email gửi vào junk, spam giảm đáng kể


# II, POP3

## 1. POP3 là gì
- POP3 Post Office Protocol version 3 là giao thức dùng để kết nối đến server và tải mail xuống máy tính cá nhân thông qua một ứng duhng mail như Outlook, Thunderbird, Windows Mail, Mac Mail...
- Thông thường, email client sẽ có tùy chọn mail muốn giữ server hay không sau khi tải về hay không. Nếu người dùng truy cập một tài khoản trên nhiều thiết bị, thì nên giữ lại bản coppy trên server nếu không thiết bị thứ 2 sẽ không tải về mail vì nó đã bị xóa khi tải về thiết bị 1
- POP3 là giao thức 2 chiều
- Port mặc định của POP3:
   - 110 - port không mã hóa
   - 995 - SSL/TLS port có thể gọi là port POP3S
   
## 2. Cơ chế hoạt động

- Kết nối đến Server
- Nhận toàn bộ mail
- Lưu cục bộ như mail mới
- Xóa mail trên server
- Ngắt kêu nối Server

## 3. Ưu nhược điểm
### Ưu điểm
- Mail được lưu cục bộ, tức có thể lưu ngay khi cả không có kết nối internet
- Kết nối internet dùng để gửi và nhân mail
- Tiết kiệm không gian lưu trữ của mail server

### Nhược điểm
- Mỗi lần nhận mail POP sẽ dowload về local mà mặc định nó sẽ xóa cái mail cũ, nên sẽ không thể sử dụng nhiều thiết bị để cài truy cập



# IMAP
## 1. IMAP là gì
- IMAP Internet Message Access Protocal: là 1 giao thức kéo mail về mail client, khác biệt với POP3, nói chỉ kéo emaik headers về, nội dung mail vẫn còn trên server
- Đây là kênh liên lạc 2 chiều, thay đổi email trên client sẽ được chuyển lên server. Sau này giao thức này phổ biến hơn nhờ nhà cung cấp mail thế giới - Gmail _ khuên dùng thay vì POP3
- Do không phải rải email về máy cụ bộ nên IMAP cho phép người dùng đưng nhập vào nhiều email client hay nhiều web mail để xem cùng 2 email
- Port mặc định của IMAP cho phép người dùng đăng nhạp vào nhiều email client hay nhiều webmail để xem cùng 1 email
- Port mặc định của IMAP
   - 143 - port không mã hóa
   - 993 -SSL/TLS port, cũng có thể được gọi là IMAPS
  
 ## 2. Cơ chế hoạt động
 - Kết nối đến server 
 - Lấy nội dung được xử yêu cầu từ người dùng và lưu đệm cục bộ
 - Xử lí các biên tập từ người dùng ví dụ như
 




















