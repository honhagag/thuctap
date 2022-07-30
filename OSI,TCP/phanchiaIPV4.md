 # Phân tích IPV4:
 1. Địa chỉ ip là gì
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
