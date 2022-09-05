# Iptables
## 1. Khái niệm  
- IPtables là ứng dụng tường lửa miễn phí trong Linux, cho phép thiết lập các quy tắc riêng để kiểm soát truy cập, tăng tính bảo mật. Khi sử dụng máy chủ, tường lửa là một trong những công cụ quan trọng giúp bạn ngăn chặn các truy cập không hợp lệ. Đối với các bản phân phối Linux như Ubuntu, Fedora, CentOS… bạn có thể tìm thấy công cụ tường lửa tích hợp sẵn IPtables.

![image](https://user-images.githubusercontent.com/105496635/188356161-7460d5e3-9de6-4204-94cf-773e30d1ef2e.png)

## 2. Một số tính năng tiêu biểu do Iptables cung cấp:
Tích hợp tốt với Kernel của Linux

Phân tích Package hiệu quả

Lọc Package

Cung cấp đầy đủ các tùy chọn để ghi nhận sự kiện hệ thống

Cung cấp kỹ thuật NAT

Ngăn chặn sự tấn công theo kiểu DoS


## 3. Thành phần cơ bản

Gồm 3 thành phần cơ bản
- Table 

Iptable sử dụng table để định nghĩa các rules cụ thể cho các gói tin. Các phiên bản Linux hiện nay có 4 loại table khác nhau:

   + Filter table
Table này quen thuộc và hay được sử dụng nhất. table này nhằm quyết định liệu gói tin có được chuyển đến địa chỉ đích hay không

   + Mangle table
Table này liên quan đến việc sửa header của gói tin, ví dụ chỉnh sửa giá trị các trường TTL, MTU, Type of Service

   + Table Nat
Table này cho phép route các gói tin đến các host khác nhau trong mạng NAT table cách thay đổi IP nguồn và IP đích của gói tin. Table này cho phép kết nối đến các dịch vụ không được truy cập trực tiếp được do đang trong mạng NAT

   + Table raw
1 gói tin có thể thuộc một kết nối mới hoặc cũng có thể là của 1 một kết nối đã tồn tại. Table raw cho phép bạn làm việc với gói tin trước khi kernel kiểm tra trạng thái gói tin

![image](https://user-images.githubusercontent.com/105496635/188356875-bb8f0767-b22f-4ee3-ade9-4bf097c014a0.png)


- Chains
Mỗi table được tạo với một số chains nhất định. Chains cho phép lọc gói tin tại các điểm khác nhau. Iptable có thể thiết lập với các chains sau:

   + Chain PREROUTING
Các rule thuộc chain này sẽ được áp dụng ngay khi gói tin vừa vào đến Network interface. Chain này chỉ có ở table NAT, raw và mangle

   + Chain INPUT
Các rule thuộc chain này áp dụng cho các gói tin ngay trước khi các gói tin được vào hệ thống. Chain này có trong 2 table mangle và filter

   + Chain OUTPUT
Các rule thuộc chain này áp dụng cho các gói tin ngay khi gói tin đi ra từ hệ thống. Chain này có trong 3 table là raw, mangle và filter

   + Chain FORWARD
Các rule thuộc chain này áp dụng cho các gói tin chuyển tiếp qua hệ thống. Chain này chỉ có trong 2 table mangle và table

   + Chain POSTROUTING
Áp dụng cho các gói tin đi network interface. Chain này có trong 2 table mangle và NAT

- Target
- Target hiểu đơn giản là hành động áp dụng cho các gói tin. Đối với những tin đúng theo rule mà chúng ta đặt thì các hành động (TAGET) có thể thực được đó là
   + ACCEPT
Chấp nhận gói tin, cho phép gói tin đi vào hệ thống

   + DROP
Loại bỏ gói tin, không có gói tin trả lời, giống như là hệ thống không tồn tại

   + REJECT
Loại bỏ gói tin nhưng có trả lời table gói tin khác, ví dụ trả lời table 1 gói tin “connection reset” đối với gói TCP hoặc bản tin “destination host unreachable” đối với gói UDP và ICMP

   + LOG
Chấp nhận gói tin nhưng có ghi lại log

Gói tin sẽ đi qua tất cả các rule chứ không dừng lại khi đã đúng với 1 rule đặt ra. Đối với những gói tin không khớp với rule nào cả mặc định sẽ được chấp nhận


## 3. Cấu hình cơ bản 
Một target sẽ được đưa ra khi có một gói tin được xác định. Targer cí thể là chuoix khác để khớp với một trong các giá trị sau:

ACCEPT: gói tin được phép đi qua
DROP gói tin không được phép đi qua
RETURN bỏ qua chuỗi hiện tại và quay trở lại quy tắc tiếp theo từ chuỗi mà nó được gọi













