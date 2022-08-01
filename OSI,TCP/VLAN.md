# VLAN

# 1. VLAN là gì
  - VLAN là viết tắt của Virtual Local Area Network hay còn gọi là mạng LAN ảo. Mạng LAN ảo (VLAN) là một nhóm các máy tính được kết nối với cùng một mạng nhưng không ở  gần nhau. Sử dụng VLAN cho phép sử dụng tài nguyên mạng hiệu quả hơn và có thể hữu ích khi có quá nhiều thiết bị cho một mạng.
  - Một VLAN được định nghĩa là một nhóm logic các thiết bị mạng và được thiết lập dựa trên các yếu tố như chức năng, bộ phận, ứng dụng… của công ty. Về mặt kỹ thuật, VLAN là một miền quảng bá được tạo bởi các switch. Bình thường thì router đóng vai trò tạo ra miền quảng bá. Đối với VLAN, switch có thể tạo ra miền quảng bá.
  - ![image](https://user-images.githubusercontent.com/105496635/182057208-7cb113d4-b96f-4728-b29c-f996861cffce.png)

# 2. Phân loại VLAN
   - Port - based VLAN: là cách cấu hình VLAN đơn giản và phổ biến. Mỗi cổng của Switch được gắn với một VLAN xác định (mặc định là VLAN 1), do vậy bất cứ thiết bị host nào gắn vào cổng đó đều thuộc một VLAN nào đó.
   - MAC address based VLAN: Cách cấu hình này ít được sử dụng do có nhiều bất tiện trong việc quản lý. Mỗi địa chỉ MAC được đánh dấu với một VLAN xác định.
   - Protocol – based VLAN: Cách cấu hình này gần giống như MAC Address based, nhưng sử dụng một địa chỉ logic hay địa chỉ IP thay thế cho địa chỉ MAC. Cách cấu hình không còn thông dụng nhờ sử dụng giao thức DHCP.
# 3. VLAN hoạt động như thế nào
- VLAN được tạo bằng cách thêm tag hoặc header vào mỗi frame Ethernet. Tag này cho mạng biết frame sẽ được gửi đến VLAN nào. Các thiết bị trong những VLAN khác nhau không thể nhìn thấy lưu lượng của nhau trừ khi chúng đều kết nối với router được cấu hình cho phép việc này.

# 4. VLAN có cần thiết không?
Hiện nay, VLAN đóng một vai trò rất quan trọng trong công nghệ mạng LAN. Để thấy rõ được lợi ích của VLAN, chúng ta hãy xét trường hợp sau :

 - Giả sử một công ty có 3 bộ phận là: Engineering, Marketing, Accounting, mỗi bộ phận trên lại trải ra trên 3 tầng. Để kết nối các máy tính trong một bộ phận với nhau thì ta có thể lắp cho mỗi tầng một switch. Điều đó có nghĩa là mỗi tầng phải dùng 3 switch cho 3 bộ phận, nên để kết nối 3 tầng trong công ty cần phải dùng tới 9 switch. Rõ ràng cách làm trên là rất tốn kém mà lại không thể tận dụng được hết số cổng (port) vốn có của một switch. Chính vì lẽ đó, giải pháp VLAN ra đời nhằm giải quyết vấn đề trên một cách đơn giản mà vẫn tiết kiệm được tài nguyên.
