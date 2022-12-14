# So sánh
## 1. Giống nhau
IMAP là viết tắt của Internet Message Access Protocol.

POP là viết tắt của Post Office Protocol.

Cả hai giao thức đều là giao thức email. Chúng cho phép người dùng đọc các email cục bộ bằng một ứng dụng trung gian như Outlook, Thunderbird,…


## 2. Khác nhau
2.1. Cơ chế hoạt động
 - POP:
 
         Kết nối với máy chủ ( server )
         Lấy lại được tất cả các mail
         Lưu trữ cục bộ dưới dạng mail mới
         Xóa mail khỏi máy chủ (server)
         Ngắt kết nối.

Hoạt động pop là lưu trữ dữ liệu về máy tính của người dùng và xóa dữ liệu khỏi máy chủ. Tuy nhiên hầu hết các POP cũng cho phép người dùng sao lưu dữ liệu trên máy chủ

- IMAP:

      Kết nối với máy chủ (server).
      Đồng bộ với máy chủ, lấy nội dung được yêu cầu từ người dùng và lưu đệm cục bộ (chẳng hạn như danh sách mail mới, tổng kết tin nhắn hay nội dung của những email được chọn lựa kỹ càng)
      Xử lý các thao tác của người dùng, chẳng hạn như đánh dấu email đã đọc, xóa email,…
      Ngắt kết nối.

Hoạt động mặc định của IMAP là cho phép nhiều Email Client truy cập đến tất cả các mục mailbox trên máy chỉ và không tải các dữ liệu dó về máy tính


2.2 Port mặc định

IMAP
143 - không mã hóa 993 - mã hóa SSL/TLS - còn gọi là IMAPS

POP3S
110 - không mã hóa 995 - mã hóa SSL/TLS - còn được gọi là POP3S

2.3 Ưu, Nhược điểm POP và IMAP
||Ưu điểm|Nhược điểm|
|-|-|-|
|POP|Mỗi lần nhận mail, POP sẽ tải lá mail đó về máy tính cục bộ của người dùng (và mặc định xóa mail đó trên máy chủ ), và giao thức này hoạt động hoàn toàn độc lập nên bạn sẽ không thể sử dụng nhiều thiết bị để quản lý cùng một tài khoản email qua giao thức POP|Mail lưu trữ cục bộ, tức là có thể truy cập bất cứ lúc nào ngay cả khi không có kết nối Internet. Kết nối Internet chỉ dùng để gửi và nhận mail. Tiết kiệm không gian lưu trữ trên server. Được lựa chọn để lại bản sao mail trên server. Hợp nhất nhiều tài khoản email và nhiều server vào một hộp thư đến|
|IMAP|Vì IMAP lưu các email trên mail server, nên dung lượng hòm thư của bạn sẽ bị giới hạn bởi các nhà cung cấp dịch vụ mail. Nếu bạn có một lượng lớn email cần lưu trữ, bạn sẽ gặp nhiều vấn đề khi gửi nhận mail khi hòm thư bị đầy. IMAP sẽ không thể lưu trữ dữ liệu của bạn trên máy tính cục bộ. Ngoài ra, nếu sử dụng IMAP thì bạn cần phải có kết nối Internet nếu muốn truy cập email.|IMAP được tao ra để cho phép người dùng truy cập từ xa email lưu trữ trên một server. Cho phép nhiều máy khách hay người dùng quản lý cùng một hộp thư đến. Vì vậy, khi đăng nhập máy tính công ty, cá nhân, thiết bị di động sẽ luôn thấy cùng email và cấu trúc thư mục do chúng được lưu trên server và tất cả những thay đổi bạn tạo ra với các bản sao cục bộ ngay lập tức được đồng bộ với server. Xem nhanh hơn khi chỉ có các tiêu đề mail được tải về đến khi nội dung được yêu cầu rõ ràng. Mail được dự phòng tự động trên server. Tiết kiệm không gian lưu trữ cục bộ.|


## 3. Nên chọn giao thức nào loại nào
3.1 Bạn sẽ chọn với giao thức POP nếu :
Bạn muốn truy cập mail chỉ từ một thiết bị.

Bạn cần truy cập email thường xuyên dù có kết nối Internet hay không.

Không gian lưu trữ trên server hạn chế.

Bạn lo lắng về vấn đề mất mát dữ liệu do hỏng hóc trên các thiết bị cục bộ.

3.2 Bạn sẽ chọn với giao thức IMAP nếu :
Bạn muốn truy cập email từ nhiều thiết bị khác nhau.

Bạn có một kết nối Internet thường xuyên và tin cậy.

Bạn muốn xem nhanh các email mới hoặc những email trên server.

Không gian lưu trữ cục bộ hạn chế.

Bạn lo lắng về vấn đề dự phòng dữ liệu.


