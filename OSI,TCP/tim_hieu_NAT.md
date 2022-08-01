# NAT
## Khái niệm: 
![image](https://user-images.githubusercontent.com/105496635/182116848-1b71f96f-3af7-40c1-85a3-a6a26686c360.png)

- NAT hay Network Address Translation là một kỹ thuật chuyển đổi đặc biệt. 
Theo đó kỹ thuật này có thể chuyển đổi IP nội miền sang IP ngoại miền. 
Quá trình chuyển đổi này tương tự như việc hỗ trợ mạng cục bộ Private dễ dàng truy cập vào mạng internet công cộng.
- Mạng lưới internet toàn cầu ngày một phát triển mạnh mẽ.
Hiện nay vẫn chưa có một thống kê nào thực sự tính khác cho biết có bao nhiêu lượng người truy cập và host đang hoạt động.
Tuy nhiên ước tính chắc chắn có khoảng trên 100 triệu host, toàn cầu tính đến đầu năm 2021 sớm đặt mốc 4.66 tỷ người.
Tốc độ phát triển nóng như vậy lại càng đòi hỏi sự tham gia của kỹ thuật NAT.
Nhờ có kỹ thuật này, mạng cục bộ LAN sẽ mở rộng liên kết nối tiếp thuận lợi hơn. 
Vậy nếu đã hiểu sơ qua NAT là gì, bạn hãy tìm hiểu tính năng chính của kỹ thuật NAT trong hệ thống mạng.

## Chức năng chính của NAT trong hệ thống mạng
![image](https://user-images.githubusercontent.com/105496635/182118253-b8152a90-56d4-4273-9601-3959969b0c64.png)
- Trong hệ thống mạng NAT có vai trò giữ vài trò di chuyển các gói tin giữa các lớp mạng khác nhau. Cụ thể NAT cần tiến hành
chuyển đổi IP từng gói tin và chuyển đến router cùng 1 số thiết bị khác
![image](https://user-images.githubusercontent.com/105496635/182119245-cab7141e-2ee7-420c-88eb-2975fe172b82.png)
  
 - Trong quá trình chuyển gói tin từ mạng công cộng public ngược lại NAT, NAT cần tiến hành thay đổi IP đích sang dạng IP nội bộ. Sau đó mới chuyển đi.
- Mặt khác, NAT còn hoạt động tương tự như một từờng lửa, hỗ trợ bảo mật IP của thiết bị. Giả sử máy tính bị gián đoạn khi kết nối với internet, IP public khi đó lập tức chuyển đổi thành IP thay thế mạng cục bộ.
# Tìm hiểu IP Public và IP Private
- Trong quá trình nghiên cứu khái niệm NAT là gì, bạn cần nắm rõ bản chất IP Public và IP Private.
### IP Public
![image](https://user-images.githubusercontent.com/105496635/182121476-2fd3e21d-4e1f-47ac-a935-93d01f84887a.png)

- IP Public chính là IP ngoại miền. Thực chất, đây là dạng địa chỉ cung cấp bởi tổ chức nắm quyền điều phối mạng internet. Chẳng hạn như phía nhà mạng cung cấp dịch vụ internet.

- Mỗi IP Public luôn mang tính duy nhất, cung cấp bởi phía nhà mạng internet. Điều này đồng nghĩa người dùng không thể tự động thay đổi IP.
### IP Private
- Từng thiết bị hoạt động trong hệ thống mạng nội bộ LAN đều có một địa chỉ IP Private riêng. Mỗi IP Private đều có khả năng liên kết với nhau hình thành mạng router. Tuy nhiên, chúng không kết nối trực tiếp với hệ thống internet bên ngoài.

![image](https://user-images.githubusercontent.com/105496635/182121745-526752e5-00fd-4963-aa80-883aa5e0798c.png)
 
 *Nếu muốn IP Private liên kết nối mạng internet bên ngoài, NAT cần tiến hành chuyển đổi từ IP Private sang IP Public.*
 
### Phân loại NAT 
- Kỹ thuật NAT hiện chia thành 3 loại cơ bản. Mỗi loại NAT lại ứng với đặc tính kỹ thuật riêng. 

### Static NAT
- Static NAT – kỹ thuật biến đổi IP này thành IP khác thông qua cách cố định từ IP sang IP Public. Quy trình này sẽ thực hiện hoàn toàn thủ công. Static NAT đặc biệt phát huy tác dụng khi thiết bị sở hữu địa chỉ cố định truy cập mạng internet từ bên ngoài.

![image](https://user-images.githubusercontent.com/105496635/182123447-ffdafaad-4b85-4351-bf10-b6656d35a8a9.png)


### Dynamic NAT
- Dynamic NAT hay NAT động. Đây là kỹ thuật chuyển đổi từ một địa chỉ IP sang kiểu IP khác hoàn toàn tự động. Cụ thể, NAT tĩnh có nhiệm vụ biến đổi đổi ip mạng cục bộ thành IP đăng ký hợp lệ.

### NAT Overload
- NAT Overload – một kiểu giao thức của NAT động. Số lượng lớn địa chỉ IP có thể quy về một IP Public qua hệ thống cổng Port. Mỗi Port thường chia thành các NAT ứng với các mức độ.

### List thuật ngữ liên quan đến NAT
![image](https://user-images.githubusercontent.com/105496635/182123609-9d2231b3-7d70-46a5-9b41-1d277f1342f0.png)

- Inside local: Địa chỉ IP ứng với mỗi thiết bị nằm trong mạng nội bộ nhưng không cung cấp bởi Network Information Center.
- Inside global: Kiểu địa chỉ IP đăng ký tại Network Information Center. Đây là địa chỉ phù hợp để thay thế cho IP Inside local.
- Outside local: Địa chỉ IP ứng với một thiết bị hoạt động tại mạng bên ngoài. Theo đó, những thiết bị thuộc mạng mạng bên trong có khả năng tìm thấy thiết bị khác hoạt động bên ngoài nhờ vào địa chỉ IP Outside local. Địa chỉ IP này không nhất thiết cần đăng ký tại - -- - Network Information Center. Bởi đôi khi nó có thể là một IP Private.
Outside global: Địa chỉ IP ứng với thiết bị hoạt động tại hệ thống mạng bên ngoài, hoàn toàn hợp lệ với mạng internet.

### Lý do nên sử dụng NAT 
Dynamic NAT có khả năng hình thành một ngăn cách mạng nội bộ với mạng bên ngoài. Có nghĩa NAT chỉ hỗ trợ dạng kết nối có nguồn gốc cụ thể trong Stub Domain. Như vậy, thiết bị ngoài mạng không thể kết nối với máy tính của bạn trừ trường hợp máy tính của bạn đã kết nối với thiết bị này trước đó.
![image](https://user-images.githubusercontent.com/105496635/182123815-ba00808e-f594-4bf2-9f8d-480090aac7f0.png)

- Bạn có quyền duyệt internet, liên kết đến một website nào đó hoặc download file. Còn những người dùng không áp dụng địa chỉ IP của bạn sẽ không được hỗ trợ chức năng tương tự.

- Trong khi đó, Static NAT lại hỗ trợ thiết bị đi ngoài kết nối với hệ thống máy tính trên Stub Domain. Chẳng hạn khi cần dịch chuyển từ Inside Global Address sang Inside Local Address, Static NAT có nhiệm vụ hỗ trợ kết nối.

- Nhiều NAT Router sẽ bổ sung bộ lọc và traffic logging. Trong đó, bộ lọc cho phép tổ chức của bạn kiểm soát hoạt động truy cập website doanh nghiệp hiệu quả hơn. Trường hợp muốn tạo tệp tin, bạn nên dùng đến traffic logging.

- Trong một vài trường hợp, NAT có thể nhầm lẫn giữa các server proxy với nhau. Thế nhưng, giữa NAT và server proxy vẫn có sự khác biệt dễ nhận thấy. Vì vậy, NAT không thể nhầm lẫn giữa thiết bị nguồn và thiết bị đích. Mọi người gần như không thể nhận ra NAT hoạt động như một thiết bị trung gian.

- Thông thường, máy chủ proxy hoạt động tại tầng thứ tư của mô hình OSI Reference Model. Còn NAT lại hoạt động ở tầng thứ ba trong mô hình mạng Network protocol. Khi hoạt động tại vị trí cao dễ khiến server proxy vận hành chậm hơn so với thiết bị NAT.


- Lợi ích to lớn mà NAT đem đến cho người dùng là hỗ trợ quản trị mạng theo hướng hiệu quả hơn. Chẳng hạn, bạn có quyền di chuyển máy chủ web tới một máy chủ khác.

## Đánh giá về NAT

### Ưu điểm
- NAT sở hữu ưu điểm lớn về mặt tiết kiệm địa chỉ IPv4. Khi lượng người truy cập internet tăng lên dễ dẫn đến tình trạng thiếu hụt IPv4. Lúc này, kỹ thuật NAT có khả năng tăng giảm số lượng IP cần dùng.
- Hỗ trợ ẩn địa chỉ IP trong mạng lưới LAN.
- NAT giúp chia sẻ tài nguyên kết nối internet cho nhiều thiết bị trong cùng mạng LAN thông qua một IP Public.
- Hỗ trợ nhà quản lý mạng trong quá trình lọc gói tin, xét duyệt quyền truy cập tới bất cứ một port nào.
### Hạn chế 
- Áp dụng kỹ thuật NAT khiến công việc CPU thực hiện tăng lên (hoạt động liên tục để thay đổi IP). Như vậy, độ trễ trong switching cũng đông người tăng cao, tác động tiêu cực đến tốc độ đường truyền mạng.
- Kỹ thuật NAT chưa thể che giấu hoàn toàn địa chỉ IP trong mạng LAN, nguồn gốc IP cũng chưa thể truy vấn tận gốc IP.
- Trong quá trình ẩn IP, NAT cũng đồng thời làm một vài ứng dụng sử dụng IP bị gián đoạn.
