# Các lệnh  cơ bản và quy tắc
## Các lệnh cơ bản
- Kiểm tra xem ufw có được bật hay không:

           sudo ufw status

![image](https://user-images.githubusercontent.com/105496635/188384804-7ef3a19c-28ae-44c6-bebc-38a08b61af78.png)
  
       
Như ta đã thấy thì ufw chưa được bật

- Bật UFW:

Để bật ufw dùng lệnh sau:

           sudo ufw enable


![image](https://user-images.githubusercontent.com/105496635/188385095-37aa7d4c-1431-4447-9712-7e35ecdb275e.png)


Như trên ta thấy ufw đã được bật

- Dùng lệnh sau để xem trên ufw chặn hoặc cho phép nhưng gì:

             sudo ufw status

![image](https://user-images.githubusercontent.com/105496635/188385724-af87626c-e159-4cae-b436-e056e16cb68f.png)



- Tắt UFW:

Dùng lệnh sau để tắt:

          sudo ufw disable

![image](https://user-images.githubusercontent.com/105496635/188385943-a26c99c4-4cec-4278-918e-fe2eb8abe66b.png)


- Chặn địa chỉ IP:

Mình sẽ chặn địa chỉ IP: 172.16.1.222:

            sudo ufw deny from [ip muốn chặn]

![image](https://user-images.githubusercontent.com/105496635/188386441-ce580ae8-951a-4e10-86f8-1e8c9c42f19e.png)

- Chúng ta có thể dủng lệnh sau để xem IP đã chặn:

           sudo ufw status

![image](https://user-images.githubusercontent.com/105496635/188392197-344c8a8c-1f1d-454a-bb0e-79992dee3022.png)

- Chặn các mạng con:

Mình dùng lệnh sau để chặn mạng con 172.16.10.0/24:

![image](https://user-images.githubusercontent.com/105496635/188392391-b6cf86f3-5de5-432d-88d2-39da384df05d.png)



- Chặn các kết nối đến Network Interface:

Chúng ta dùng lệnh sau:

        sudo ufw deny in on eth0 from [ip muốn chặn]

![image](https://user-images.githubusercontent.com/105496635/188392574-c9dc3457-bf0c-41ad-9baa-31e18fd22985.png)


- Cho phép các IP kết nối:

Dùng lệnh sau để cho phép ip: 172.16.1.30

           sudo ufw allow from [IP muốn cho phép]

![image](https://user-images.githubusercontent.com/105496635/188392876-37b916ae-ff2e-465d-9c88-f2f5b783eb68.png)




- Dùng lệnh sau để xem danh những IP được cấp phép:

       sudo ufw status


![image](https://user-images.githubusercontent.com/105496635/188393297-718938dd-7ef0-4540-b34d-c7555b799826.png)

Xóa các quy tắc UFW:

Để xóa các quy tắc đã thiết lập trước đó ta dùng lệnh sau, ở đây mình sẽ xóa quy tắc cho IP: 172.16.1.30 kết nối:


        sudo ufw delete allow from [IP]


![image](https://user-images.githubusercontent.com/105496635/188393908-c1371ebd-1a19-44f5-8a5a-150f14583873.png)

- Ngoài ra chúng ta co thể dùng ID của các quy tắc để xóa chúng, xem thông tin các quy tắc:

          sudo ufw status numbered


![image](https://user-images.githubusercontent.com/105496635/188394314-a6559195-6862-4409-a964-423d4d85b37f.png)


- Chạy lệnh sau để xóa quy tắc theo ID , ở đây mình sẽ xóa quy tắc ở ID:1:

         sudo ufw delete 1

![image](https://user-images.githubusercontent.com/105496635/188394642-1486f234-61ed-4606-bdce-c7fd970dea16.png)

- Liệt kê các ứng dụng có sẵn:

Để liệt kê nhưng cấu hình có sẵn dùng lệnh sau:

              sudo ufw app list


![image](https://user-images.githubusercontent.com/105496635/188394902-78fd2334-00ab-4c88-92a8-427d5a57bbea.png)



- Cho phép SSH:

Cho phép tất cả các kết nối SSH đến trên cổng SSH mặc định:

          sudo ufw allow OpenSSH

- Chỉ định số cổng chính xác của dịch vụ SSH, thường được đặt thành 22 theo mặc định:

          sudo ufw allow 22

![image](https://user-images.githubusercontent.com/105496635/188395707-0bca2cd5-4c1e-40f2-a9b5-398e05a96a2d.png)



Cho phép SSH đến từ địa chỉ hay mạng con cụ thể:

Lệnh sau sẽ chỉ cho phép các kết nối SSH đến từ địa chỉ IP:172.16.1.31:

    sudo ufw allow from 172.16.1.31 proto tcp to any port 22

![image](https://user-images.githubusercontent.com/105496635/188395851-6e84c1a2-2aea-4264-8809-94dc25bacc01.png)


Lệnh sai cho phép mạng con kết nối SSH:

sudo ufw allow from 172.16.1.0/24 proto tcp to any port 22

![image](https://user-images.githubusercontent.com/105496635/188396326-27a382f1-9acc-457c-a9e8-a22804991aa3.png)


Cho phép RsYnc kết nối từ địa chỉ IP hay mạng con cụ thể:

Các Rsync chương trình, chạy trên cổng 873, có thể được sử dụng để chuyển các tập tin từ máy này sang máy khác.

Sử dụng lệnh sau để cho phép IP: 172.16.1.31:

       sudo ufw allow from 172.16.1.31 to any port 873

![image](https://user-images.githubusercontent.com/105496635/188396402-c1d5f727-dd76-43b1-8f39-c5839c4fab99.png)


Sử dụng lệnh sau để cho phép mạng con kết nối:

       sudo ufw allow from 172.16.1.0/24 to any port 873


Cho phép Nginx HTTP/HTTPS:

Chạy lệnh sau để xác định cấu hình nào khả dụng:

        sudo ufw app list | grep Nginx


Lệnh sau để cho phép HTTP/HTTPS chạy trên cổng  80 và 443:

         sudo ufw allow "Nginx Full"


Cho phép phép tất cả các kết nối HTTP đến cổng 80:

            sudo ufw allow http


Cho phép phép tất cả các kết nối HTTPS đến cổng 443:

           sudo ufw allow https



## Phần Kết:
UFW là một công cụ mạnh mẽ có thể cải thiện đáng kể tính bảo mật của các máy chủ của bạn khi được định cấu hình đúng cách. Hướng dẫn tham khảo này bao gồm một số quy tắc UFW phổ biến thường được sử dụng để định cấu hình tường lửa trên Ubuntu.
















