 # Phân tích IPV4, IPV6:
 I. Địa chỉ ip là gì
 Địa chỉ IP là địa chỉ logic được sử dụng trong giao thức IP của lớp Internet thuộc mô hình TCP/IP (tương ứng với lớp thứ 3 – lớp network của mô hình OSI)
 2. Cấu trúc địa chỉ IP
-   Địa chỉ IP gồm 32 bit nhị phân, chia thành 4 cụm 8 bit (gọi là các octet). Các octet được biểu diễn dưới dạng thập phân và được ngăn cách nhau bằng các dấu chấm.

-    Địa chỉ IP được chia thành hai phần: phần mạng (network) và phần host.
    ![image](https://user-images.githubusercontent.com/105496635/181904030-ed9fe7ff-90fb-4ab7-a374-fc6171463c43.png)
   
  - Việc đặt địa chỉ IP phải tuân theo các quy tắc sau:
    + Các bit phần mạng không được phép đồng thời bằng 0.
     VD: địa chỉ 0.0.0.1 với phần mạng là 0.0.0 và phần host là 1 là không hợp lệ.

    + Nếu các bit phần host đồng thời bằng 0, ta có một địa chỉ mạng.
     VD: địa chỉ 192.168.1.1 là một địa chỉ có thể gán cho host nhưng địa chỉ 192.168.1.0 là một địa chỉ mạng, không thể gán cho host được.

    + Nếu các bit phần host đồng thời bằng 1, ta có một địa chỉ quảng bá (broadcast).
     VD: địa chỉ 192.168.1.255 là một địa chỉ broadcast cho mạng 192.168.1.0
     
 II. Địa chỉ IPv4

 1. Khái niệm
 - IPv4 (Internet Protocol Version 4) dịch ra có nghĩa là giao thức Internet Phiên bản thứ 4. IPv4 đã được bộ quốc phòng Hoa kỳ chuẩn hóa trong bản MIL-STD-1777.
 Giao thức Internet IP đã trải qua nhiều phiên bản khác nhau và phiên bản Ipv4 là phiên bản đầu tiên được sử dụng rộng rãi trên toàn thế giới và hiện vẫn còn đang là  nòng cốt của Internet trên toàn thế giới.
  - Ipv4 là giao thức mang tính hướng dữ liệu và được sử dụng cho hệ thống chuyển mạch gói. Ipv4 không quan tâm đến thứ tự truyền gói tin, cũng không đảm bảo gói tin sẽ  đến đích hay là có xảy ra tình trạng lặp gói tin ở đích đến hay không. Nó chỉ có cơ chế đảm bảo tính toàn vẹn dữ liệu bằng việc sử dụng những gói kiểm tra được thiết lập đi kèm với nó.
  - Địa chỉ Ipv4 là 1 địa chỉ đơn nhất đang được sử dụng bởi các thiết bị điện tử hiện nay để nhận diện và liên lạc với nhau trên Internet. Để đánh địa chỉ, Ipv4 sử dụng   32bit và chia ra làm 4 octet (mỗi octet có 8 bit = 1 byte). Dấu chấm được sử dụng để ngăn các octet với nhau.
 - Cấu trúc của địa chỉ IPv4 Về cấu tạo, địa chỉ IPv4 sẽ có 32 bit và được biểu diễn thành một dãy số nhị phân và chia thành 4 cụm. Mỗi cụm như vậy sẽ gọi là octet. Mỗi   octet sẽ là 8 bit và chúng được ngăn cách bằng dấu chấm (.)
 - Về hình dáng, cấu trúc của một địa chỉ IPv4 sẽ gồm 4 con số ở dạng thập phân tượng trưng cho 4 cụm. Địa chỉ này gồm 2 phần là phần mạng và phần host.
 
 
 ![image](https://user-images.githubusercontent.com/105496635/181904857-1f2e8482-e304-4b73-9cc8-5480cfacec91.png)

