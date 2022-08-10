# Gắn miền cho IP
1. Sử dụng lệnh `ip add` để check IP của Centos 7

![image](https://user-images.githubusercontent.com/105496635/183854369-a78cc6f6-008e-4b6b-8688-dd43c8b9a125.png)

IP ở đây là 192.168.1.1
2. Gắn miền cho IP, sử dụng lệnh `vi /etc/hosts` để cài DNS cho địa chỉ IP

![image](https://user-images.githubusercontent.com/105496635/183855355-dbd1dd4b-c70e-4610-99b7-1cad84944114.png)

Sau đó hiện thị:

![image](https://user-images.githubusercontent.com/105496635/183856023-5c4eee34-debf-40bf-9ff0-ef1475812ca7.png)

3. Sử dụng phím tắt `Insert` trên bàn phím để sửa tập tin và thêm DNS và miền: 

![image](https://user-images.githubusercontent.com/105496635/183856408-f4a19abe-d6ba-4714-a6b9-09a18b030d91.png)

4. Tiếp theo ấn phím tắt `Esc` trên bàn phím để thoát chế độ chỉnh sửa và sử dụng lệnh `:wq` để lưu lại và gõ `Enter` để lưu

![image](https://user-images.githubusercontent.com/105496635/183856796-ef084452-2170-406d-928a-e0012acbbc96.png)

# Tạo file trên DNS 
### 1. Sử dụng `cd /etc/httpd/` đây là thư mục cấu hình cho httpd

![image](https://user-images.githubusercontent.com/105496635/183858415-ce0d886b-a16f-42bc-919a-29308321174c.png)

### 2. Gõ `ls` để kiếm tra các file cấu hình:

![image](https://user-images.githubusercontent.com/105496635/183858989-bb7068b0-240f-44b0-800c-532481e62926.png)

### 3. Gõ `cd conf` để vào file cấu hình web và gõ `cd /var/www/html` để truy cập vào file tạo web

![image](https://user-images.githubusercontent.com/105496635/183862374-9a3902ac-e3a1-4831-97da-6e89b8c8667a.png)

### 4. Gõ `vi index.html` để tạo một trang web riêng

![image](https://user-images.githubusercontent.com/105496635/183862763-21a3a0dc-c96b-4f76-9bdb-b5509becba73.png)

### 5. Sau khi gõ lệnh sẽ tạo ra một thư mục để nhập nội dung hiện thị trên trang web

![image](https://user-images.githubusercontent.com/105496635/183863139-b98c1e99-b928-4e1d-86ec-50d25cbcf524.png)
 
 Và sau đó lưu lại

### 6. Sử dụng tên miền đã tạo nhập lên trình duyệt web để kiểm tra

![image](https://user-images.githubusercontent.com/105496635/183863641-54949f72-ceb5-44bd-a5c8-776218141b1b.png)







