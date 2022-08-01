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
 
 ![image](https://user-images.githubusercontent.com/105496635/182057816-ed5c55c2-9804-4052-905a-afac7493f0bf.png)
 Như hình vẽ trên ta thấy mỗi tầng của công ty chỉ cần dùng một switch, và switch này được chia VLAN. Các máy tính ở bộ phận kỹ sư (Engineering) thì sẽ được gán vào VLAN Engineering, các PC ở các bộ phận khác cũng được gán vào các VLAN tương ứng là Marketing và kế toán (Accounting). Cách làm trên giúp ta có thể tiết kiệm tối đa số switch phải sử dụng đồng thời tận dụng được hết số cổng (port) sẵn có của switch.
 
 # 5. Lợi ích của VLAN
 - Tiết kiệm băng thông của hệ thống mạng: VLAN chia mạng LAN thành nhiều đoạn (segment) nhỏ, mỗi đoạn đó là một vùng quảng bá (broadcast domain). Khi có gói tin quảng bá (broadcast), nó sẽ được truyền duy nhất trong VLAN tương ứng. Do đó việc chia VLAN giúp tiết kiệm băng thông của hệ thống mạng.
- Tăng khả năng bảo mật: Do các thiết bị ở các VLAN khác nhau không thể truy nhập vào nhau (trừ khi ta sử dụng router nối giữa các VLAN). Như trong ví dụ trên, các máy tính trong VLAN kế toán (Accounting) chỉ có thể liên lạc được với nhau. Máy ở VLAN kế toán không thể kết nối được với máy tính ở VLAN kỹ sư (Engineering).
- Dễ dàng thêm hay bớt máy tính vào VLAN: Việc thêm một máy tính vào VLAN rất đơn giản, chỉ cần cấu hình cổng cho máy đó vào VLAN mong muốn.
- Giúp mạng có tính linh động cao: VLAN có thể dễ dàng di chuyển các thiết bị. Giả sử trong ví dụ trên, sau một thời gian sử dụng công ty quyết định để mỗi bộ phận ở một tầng riêng biệt. Với VLAN, ta chỉ cần cấu hình lại các cổng switch rồi đặt chúng vào các VLAN theo yêu cầu. VLAN có thể được cấu hình tĩnh hay động. Trong cấu hình tĩnh, người quản trị mạng phải cấu hình cho từng cổng của mỗi switch. Sau đó, gán cho nó vào một VLAN nào đó. Trong cấu hình động mỗi cổng của switch có thể tự cấu hình VLAN cho mình dựa vào địa chỉ MAC của thiết bị được kết nối vào.

# 6. Khi nào bạn cần một VLAN?
Bạn cần cân nhắc việc sử dụng VLAN trong các trường hợp sau:
- Bạn có hơn 200 máy tính trong mạng LAN
- Lưu lượng quảng bá (broadcast traffic) trong mạng LAN của bạn quá lớn
- Các nhóm làm việc cần gia tăng bảo mật hoặc bị làm chậm vì quá nhiều bản tin quảng bá.
- Các nhóm làm việc cần nằm trên cùng một miền quảng bá vì họ đang dùng chung các ứng dụng. Ví dụ như một công ty sử dụng điện thoại VoIP. Một số người muốn sử dụng điện thoại có thể thuộc một mạng VLAN khác, không cùng với người dùng thường xuyên.
- Hoặc chỉ để chuyển đổi một switch đơn thành nhiều switch ảo.

# 7. Tại sao không chia subnet?

- Một câu hỏi thường gặp đó là tại sao không chia subnet (mạng con) thay vì sử dụng VLAN? Mỗi VLAN nên ở subnet của riêng mình. VLAN có ưu điểm hơn subnet ở chỗ các máy tính tại những vị trí vật lý khác nhau (không quay lại cùng một router) có thể nằm trong cùng một mạng. Hạn chế của việc chia subnet với một router đó là tất cả máy tính trên subnet đó phải được kết nối tới cùng một switch và switch đó phải được kết nối tới một cổng trên router.

Với VLAN, một máy tính có thể được kết nối tới switch này trong khi máy tính khác có thể kết nối tới switch kia mà tất cả các máy tính vẫn nằm trên VLAN chung (miền quảng bá).

# 8. Làm thế nào các máy tính trên VLAN khác nhau có thể giao tiếp với nhau?
- Các máy tính trên VLAN khác nhau có thể giao tiếp với một router hoặc một switch Layer 3. Do mỗi VLAN là subnet của riêng nó, router hoặc switch Layer 3 phải được dùng để định tuyến giữa các subnet.

# 9. Cổng trunk là gì?
- Khi một liên kết giữa hai switch hoặc giữa một router và một switch truyền tải lưu lượng của nhiều VLAN thì cổng đó gọi là cổng trunk.

- Cổng trunk phải chạy giao thức đường truyền đặc biệt. Giao thức được sử dụng có thể là giao thức độc quyền ISL của Cisco hoặc IEEE chuẩn 802.1q.

# 10. Cài đặt VLAN
- Tạo VLAN
   - Bước 1. Đăng nhập vào tiện ích dựa trên web và chọn VLAN Management > VLAN Settings.

    - Bước 2. Trong khu vực VLAN Table, bấm vào Add để tạo một VLAN mới. Một cửa sổ sẽ xuất hiện.

    - Bước 3. VLAN có thể được thêm vào theo hai phương thức khác nhau như được hiển thị bởi các tùy chọn bên dưới. Chọn phương thức mong muốn:

      - VLAN - Sử dụng phương pháp này để tạo một VLAN cụ thể.
      - Range - Sử dụng phương pháp này để tạo một phạm vi cho VLAN.

           ![image](https://user-images.githubusercontent.com/105496635/182060761-79810a62-10c9-4ce5-bcf4-d87d1242afa6.png)

    - Bước 4. Nếu bạn đã chọn VLAN ở bước 3, hãy nhập VLAN ID vào trường VLAN ID. Phạm vi phải nằm trong khoảng từ 2 đến 4094. Trong ví dụ này, VLAN ID sẽ là 4.

    - Bước 5. Trong trường VLAN Name, nhập tên cho VLAN. Trong ví dụ này, VLAN Name sẽ là Accounting. Tối đa 32 ký tự có thể được sử dụng.

    - Bước 6. Chọn hộp kiểm VLAN Interface State để kích hoạt trạng thái interface VLAN. Nó đã được chọn theo mặc định. Nếu không, VLAN sẽ bị tắt và không có gì có thể được truyền hoặc nhận thông qua VLAN.

    - Bước 7. Tích vào hộp kiểm Link Status SNMP Traps nếu bạn muốn kích hoạt việc tạo SNMP trap. Điều này được kích hoạt theo mặc định.
     
     ![image](https://user-images.githubusercontent.com/105496635/182060841-1000dce0-f430-4473-b319-8ff34ffde3fe.png)
     
    - Bước 8. Nếu bạn chọn Range trong bước 3, hãy nhập phạm vi cho các VLAN trong trường VLAN Range. Phạm vi có sẵn là 2 - 4094. Trong ví dụ này, VLAN Range là từ 3       đến 52
     ![image](https://user-images.githubusercontent.com/105496635/182060912-848a2788-170e-49e7-8aa4-89e8fcc5d99f.png)      
     
     - Bước 9. Nhấn vào Apply

# 10. Xóa VLAN
- Bước 1. Đăng nhập vào tiện ích dựa trên web và chọn VLAN Management > VLAN Settings.

- Bước 2. Chọn hộp kiểm bên cạnh VLAN bạn muốn xóa.

- Bước 3. Nhấn Delete để xóa VLAN đã chọn.
- Xóa VLAN
Bước 1. Đăng nhập vào tiện ích dựa trên web và chọn VLAN Management > VLAN Settings.

Bước 2. Chọn hộp kiểm bên cạnh VLAN bạn muốn xóa.

Bước 3. Nhấn Delete để xóa VLAN đã chọn.

![image](https://user-images.githubusercontent.com/105496635/182061501-dd362143-2d2e-4f19-a07b-29fc0dc47a86.png)

# 11. VLAN cung cấp những gì?
 - VLAN giúp tăng hiệu suất mạng LAN cỡ trung bình và lớn vì nó hạn chế bản tin quảng bá. Khi số lượng máy tính và lưu lượng truyền tải tăng cao, số lượng gói tin quảng bá cũng gia tăng. Bằng cách sử dụng VLAN, bạn sẽ hạn chế được bản tin quảng bá.

 - VLAN cũng tăng cường tính bảo mật bởi vì thực chất bạn đặt một nhóm máy tính trong một VLAN vào mạng riêng của chúng.

# 13. Rủi ro bảo mật tiềm ẩn khi sử dụng VLAN
- Mặc dù VLAN mang lại nhiều lợi ích, nhưng có một rủi ro bảo mật tiềm ẩn cần lưu ý. Nếu người dùng độc hại bằng cách nào đó có được quyền truy cập vào một thiết bị được kết nối với router, họ có thể hình dung ra lưu lượng truy cập đến các VLAN khác mà họ không nên có quyền truy cập trong một quá trình được gọi là tấn công VLAN hopping. Để ngăn chặn điều này, hãy đảm bảo rằng bạn bảo mật đúng cách cho tất cả các thiết bị trên mạng của mình và chỉ cho phép những người dùng đáng tin cậy truy cập chúng.

- VLAN có thể là một công cụ hữu ích trong việc quản lý và bảo mật các mạng lớn. Tuy nhiên, như với bất kỳ công nghệ nào, có những rủi ro tiềm ẩn cần lưu ý. Hãy chắc chắn xem xét những điều này khi quyết định có sử dụng VLAN trên mạng của bạn hay không.


            - Nguồn tham khảo: https://quantrimang.com/vlan-la-gi-lam-the-nao-de-cau-hinh-mot-vlan-tren-switch-cisco-64830#:~:text=VLAN%20l%C3%A0%20vi%E1%BA%BFt%20t%E1%BA%AFt%20c%E1%BB%A7a,thi%E1%BA%BFt%20b%E1%BB%8B%20cho%20m%E1%BB%99t%20m%E1%BA%A1ng.








