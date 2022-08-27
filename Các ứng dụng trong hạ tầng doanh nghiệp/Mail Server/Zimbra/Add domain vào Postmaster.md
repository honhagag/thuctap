# Add domain vào Postmaster
Trong quá trình gửi mail đến các địa chỉ @gmail.com hoặc các địa chỉ mail sử dụng trên hệ thống của Google nhưng nhận được thông báo lỗi:

Như hình dưới đây. Lí dó là do không được xác thực nên google đánh giá là spam nên không được gửi

![image](https://user-images.githubusercontent.com/105496635/187011923-19b420aa-a200-41ea-99e4-ea491c2afa0e.png)

Như vậy phải Add tên miền vào Postmaster

Bước 1: Nhập Email để xác nhận
![image](https://user-images.githubusercontent.com/105496635/187013022-ce154054-6e8b-4ef8-83fa-cb6cfacb608a.png)

Bước 2:  Cấu hình bản ghi DNS TXT mà Google cung cấp và chọn Verify


![image](https://user-images.githubusercontent.com/105496635/187013085-e09c1885-aeab-4d85-9378-55a2a3e42e94.png)

Bước 3: Chọn done để hoàn tất

- Sau khi thực hiện thêm tên miền vào công cụ Postmaster của Google thành công thì thông tin sẽ được hiển thị như sau:

![image](https://user-images.githubusercontent.com/105496635/187013621-621e691c-6634-4d9f-af12-8e8da96b713c.png)








