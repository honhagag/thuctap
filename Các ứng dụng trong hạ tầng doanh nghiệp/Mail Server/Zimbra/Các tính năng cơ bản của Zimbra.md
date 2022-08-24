# Zimbra
## 1. Zimbra là gì
- Zimbra được biết đến là bộ phận thành phần bao gồm máy chủ email và máy khách website. Zimbra Collaboration Suite là một trong những mã nguồn mở miễn phí nổi tiếng về tính năng ,độ ổn định và bảo mật cao.
- Nó không chỉ đơn giản là tên của một ứng dụng về email mà còn là một giải pháp, một hệ thống khá hoàn chỉnh để triển khai môi trường chia sẻ công tác phục vụ cho quản lý và công việc. Zimbra được tin dùng bởi hơn 5.000 công ty và doanh nghiệp quốc doanh, và trên 500 triệu người dùng cuối tại hơn 130 quốc gia

## 2. Các tính năng chính của Zimbra
- Thư điển tử: một hệ thống thư điện tử Gmail gồm Mail server (SMTP, POP3, IMAP, Antivirus, Antispam, openLDAP, backup,… Bao gồm đầy đủ các tính năng như auto-reply, auto-forward, mail filter, …) và Mail client (Zimbra desktop và Zimbra Web Client).
- Lịch công tác (calendar): lịch cá nhân và lịch nhóm, tự động gửi mail mời họp,…
- Sổ địa chỉ (Contacts): sổ cá nhân và sổ chung của nhóm.
- Danh mục công việc (Task): của cá nhân và nhóm.
- Tài liệu (Documents): tài liệu dưới dạng wiki của cá nhân hoặc soạn tập thể
- Cặp hồ sơ (Briefcase): lưu file dùng riêng hoặc chung.
- Chat: chat nội bộ trong mạng LAN hoặc trên Internet.
- Tất cả các mục trên đều có phần lưu trên máy chủ để có thể dùng chung được và truy cập được từ bất kỳ đâu có Internet
- Bao gồm một kho các Zimlet (tương tự các extensions) mà các quản trị viên có thể chọn cài để bổ xung tính năng cần thiết. Mọi người có thể tự viết các Zimlet để kết nối hệ thống Zimbra với các hệ thống thông tin khác hoặc mở rộng tính năng. Đây có lẽ là một trong những điểm mạnh nhất của Zimbra.
- Quản trị hệ thống qua giao diện web khá đầy đủ và chi tiết với nhiều tiện ích.

## 3. Điểm nổi bật của Zimbra
- Sự riêng tư
  - Zimbra có thể được triển khai trong trung tâm dữ liệu hoặc trong môi trường điện toán đám mây, đáp ứng các yêu cầu về chủ quyền dữ liệu và thỏa mãn nhu cầu riêng tư của doanh nghiệp.

- Tính bảo mật
  - Zimbra mang đến giải pháp đột phá cho quy trình xác thực 2 nhân tố, mã hóa email, truyền thông bảo mật qua TLS, HTTPs,…. Nó cũng dễ dàng tích hợp với các ứng dụng bảo mật của bên thứ ba.
- Tính linh hoạt
  - Khả năng triển khai không giới hạn. Triển khai tại trung tâm dữ liệu riêng của bạn, thông qua một máy chủ ảo riêng hay công khai, hoặc kết nối với một đối tác cung cấp dịch vụ lưu trữ Zimbra.

- Khả năng truy cập
  - Bạn có thể truy cập tài khoản Zimbra của mình vào bất kỳ lúc nào, tại bất cứ đâu, và từ bất kỳ thiết bị nào.

- Khả năng tương thích
  - Cho phép người dùng sử dụng Microsoft Outlook để đồng bộ hóa hộp thư, lịch công tác, sổ địa chỉ và danh mục công việc thông qua Trình kết nối Zimbra dành cho Outlook.

- Cộng tác Zimbra
  - Chat cho phép các thành viên nhóm bạn liên lạc với nhau khi đang di chuyển trong khi Zimbra Drive, Zimbra Web Client và Zimbra Desktop lại cho phép bạn dễ dàng lưu trữ, chia sẻ và cộng tác trên mọi loại tập tin.

- Chi phí vận hành
  - Tiết kiệm tiền đối với chi phí cấp phép và quản lý.

- Dễ quản lý
  - Tiết kiệm thời gian và tiền bạc với hệ thống quản lý dễ dàng của Zimbra. Giao diện dễ nhìn và việc quản lý máy chủ thư Zimbra cực kì dễ dàng.

- Opensouce
  - Nguồn mở là điểm trọng tâm của Zimbra. Các công ty có thể sử dụng phiên bản Zimbra Open Source Edition, hoặc nâng cấp lên Zimbra Network Edition để sử dụng các tính năng như đồng bộ hóa di động.

- Tích hợp
  - Dễ dàng tích hợp với Zimlet và API của Mail Zimbra.

- Cộng đồng
  - Cộng đông của Zimbra có hơn 60.000 thành viên và mạng lưới gồm hơn 1.900 đối tác trên toàn cầu.

## 4. Kiến trúc
- Về kiếm trúc Zinbra vẫn sử dụng các phần mềm chức năng phổ biến như  OpenLDAP, Postfix, SpamAssassin, Amavisd, Tomcat,... cùng với 1 số thành phần mềm để tạo nên hệ thống tích hợp chặt chẽ. Có thể dùng OpenLDAP mà dùng window Active Directory, hoặc import user  từ 1 máy chủ Exchange sang.
- Hiện tại Zinbra Server có các bài cài viết redhat, fedora, centos,... nếu chỉ cài trên một máy thì khá đơn giản và nhanh
- Zinbra có thể cài nhiều theo cấu trúc khác nhau từ 1 hệ thống nhỉ nhiều account trên một máy chủ duy nhất cho đến hệ thống hàng nghìn account trên nhiều máy chủ có chức năng khá nhau, có khả năng mở rộng thêm máy chủ dễ dàng
- Zimbra có 1 kho các Zimlet (một thứ tương tự các extensions của Firefox) mà các quản trị mạng có thể chọn cài để bổ xung tính năng. mọi người có thể tự viết các zimlet để kết nối hệ thống zimbra với các hệ thống thông tin khác hoặc mở rộng tính năng. Đây có lẽ là 1 trong những điểm mạnh nhất sẽ gây nghiện cho người dùng giống như extensions của firefox vây.
- Quản trị hệ thống qua giao diện web khá đầy đủ và chi tiết với nhiều tiện ích. Ví dụ có thể tạo hàng ngàn account trong vài phút









