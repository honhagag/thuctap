 # Tìm hiểu về giao thức định tuyến, tập trung vào định tuyến tĩnh.
# 1. Khái niệm:
    - Định tuyến tĩnh là quá trình router chuyển hóa dữ liệu từ mạng đích tới địa chỉ dựa vào IP đích của gói dữ liệu 
    - Kỹ thuật định tuyến đơn giản, dễ thực hiện, ít hao tốn tài nguyên mạng  và xử lí CPU trên router.
    Tuy nhiên kỹ thuật này không hội tụ với các thay đổi diễn ra trên mạng và không thích hợp với những mạng có quy mô lớn 
- Ưu điểm:
    + Sử dụng ít bandwidth hơn định tuyến động.
    + Không tiêu tốn tài nguyên để tính toán và phân tích gói tin định tuyến.
- Nhược điểm:
    + Không có khả năng tự động cập nhật đường đi.
    + Phải cấu hình thủ công khi mạng có sự thay đổi.
    + Phù hợp với mạng nhỏ, rất khó triển khai trên mạng lớn.
- Một số tình huống bắt buộc dùng định tuyến tĩnh:
    + Đường truyền có băng thông thấp
    + Người quản trị mạng cần kiểm soát các kết nối.
    + Kết nối dùng định tuyến tĩnh là đường dự phòng cho đường kết nối dùng giao thức định tuyến động.
    + Chỉ có một đường duy nhất đi ra mạng bên ngoài (mạng stub).
    + Router có ít tài nguyên và không thể chạy một giao thức định tuyến động.
    + Người quản trị mạng cần kiểm soát bảng định tuyến và cho phép các giao thức classful và classless.
    
# 2. Cấu hình tuyến ngoại tuyến
![image](https://user-images.githubusercontent.com/105496635/182106776-56d57c98-b5fc-49d4-8b2f-44dd77dd3e4e.png)
- Hình trên là hai router, R1 sử dụng cổng f0/0 đấu xuống mạng LAN có subnet 192.168.1.0/24. Tương tự, R2 sử dụng cổng f0/0 đấu xuống PC có subnet 192.168.2.0/24. Subnet sử dụng cho kết nối leased-line nối giữa hai router là 192.168.3.0/24. Đầu tiên, chúng ta phải cấu hình đặt địa chỉ IP cho các cổng của router, cũng như IP và Default-gateway cho các PC. Default-gateway hiểu đơn giản là IP của cổng của router gần nhất mà PC đó kết nối trực tiếp đến.
Cấu hình định tuyến tĩnh trên router Cisco được thực hiện bằng cách sử dụng lệnh có cú pháp như sau
Router (config) # ip route destination_subnet subnetmask{IP_next_hop|output_interface} 
- Trong đó:
    - destination_subnet: mạng đích đến.
subnetmask: subnet – mask của mạng đích.

    I - P_next_hop: địa chỉ IP của trạm kế tiếp trên đường đi.

output_interface: cổng ra trên router.

AD: chỉ số AD của route khai báo, sử dụng trong trường hợp có cấu hình dự phòng.

Trong ví dụ hình trên, từ R1 muốn đi đến mạng 192.168.2.0/24 thì phải đi ra khỏi cổng f1/0. Để thể hiện điều đó vào bảng định tuyến phải thực hiện cấu hình:

R1 (config) # ip route 192.168.2.0 255.255.255.0 f1/0

hoặc

R1 (config) # ip route 192.168.2.0 255.255.255.0 192.168.3.2

R2 muốn đi đến mạng 192.168.1.0/24 thì phải đi ra khỏi cổng f1/0:

R2 (config) # ip route 192.168.1.0 255.255.255.0 f1/0

hoặc

R2 (config) # ip route 192.168.1.0 255.255.255.0 192.168.3.1

Sau khi đã cấu hình xong các route cho các mạng 192.168.1.0/24 và 192.168.2.0/24, kiểm tra bảng định tuyến trên mỗi router: Bảng định tuyến của R1:

R1#show ip route

C 192.168.1.0/24 is directly connected, FastEthernet0/0

S 192.168.2.0/24 [1/0] via 192.168.3.2

C 192.168.3.0/24 is directly connected, FastEthernet1/0

Bảng định tuyến của R2:

R2#show ip route

S 192.168.1.0/24 [1/0] via 192.168.3.1

C 192.168.2.0/24 is directly connected, FastEthernet0/0

C 192.168.3.0/24 is directly connected, FastEthernet1/0

Kí tự “S” ở đầu dòng thể hiện rằng các thông tin định tuyến này được học vào bảng định tuyến thông qua định tuyến tĩnh và các dòng mô tả các mạng kết nối trực tiếp được ký hiệu bởi kí tự “C” – connected – kết nối trực tiếp.

# 3. Default route

- Được dùng để định tuyến mặc định tất cả dữ liệu đến một mạng bất kỳ đi theo đường nào đó. Nhưng nếu mạng đó đã có đường đi trong bảng định tuyến, thì gói tin sẽ ưu tiên đi theo đường đi rõ ràng trước.

Router (config) # ip route 0.0.0.0 0.0.0.0 {ip next-hop | exit interface}
