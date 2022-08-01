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



