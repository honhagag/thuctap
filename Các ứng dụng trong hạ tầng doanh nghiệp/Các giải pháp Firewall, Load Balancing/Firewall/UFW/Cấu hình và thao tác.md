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




































































