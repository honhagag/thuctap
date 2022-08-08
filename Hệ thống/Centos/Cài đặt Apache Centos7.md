# Install CentOs 7:
 Link dowload Centos 7: http://centos-hcm.viettelidc.com.vn/7.9.2009/isos/x86_64/
 
## Các bước để tạo apache trên CentOS 7:

Giao diện CentOS 7:
![image](https://user-images.githubusercontent.com/105496635/183330923-0ce14b5f-7c16-423c-b1ce-b913dbe50fef.png)

*Trong giao diện này, nhấp phải để mở hộp thoại teminal*

![image](https://user-images.githubusercontent.com/105496635/183331443-98ec189f-3c4e-444e-874f-028249340f64.png)


 - Bước 1: Thay đổi quyền người dùng sang `root@localhost` sử dụng lệnh :

![image](https://user-images.githubusercontent.com/105496635/183331755-6ecd1f8d-8743-463a-a5ae-fce3e769d6d9.png)

 - Bước 2: Vì CentOS là mã nguồn mở, nên Apache có sẵn trong kho lưu trữ, trước tiên cần cập nhật  `httpd package index` để cập nhật những thay đổi mới nhất

  - Sử dụng lệnh `sudo yum update httpd`

![image](https://user-images.githubusercontent.com/105496635/183333705-83f2b45a-52ab-4fdb-8694-7d4168e0fd74.png)

  - Sau đó thực hiện gói cài đặt phần mềm `sudo yum install httpd`


![image](https://user-images.githubusercontent.com/105496635/183334800-60f4e9e6-fc42-44fe-a39a-d53550abff60.png)


Khi đã xác nhận, yum package manager sẽ cài đặt Apache và các phần dependencies bắt buộc khác.

- Tiếp theo cài đặt tường lửa "Firewall" trên server và mở cổng port 80 để phục vụ cho nhu cầu qua http
`sudo firewall-cmd --permanent --add-service=http`

![image](https://user-images.githubusercontent.com/105496635/183336564-a23e8846-7c58-4be5-931b-36a55bdfd11e.png)

- Để cấu hình Apache web theo giao thức https, cổng 443:

`sudo firewall-cmd --permanent --add-service=https`

![image](https://user-images.githubusercontent.com/105496635/183337013-378c1c8c-ba2c-49fa-89ac-74d10124b6bd.png)

Sau khi cài đặt cần bạn cần tải lại firewall để các quy tắc có hiệu lực và có thể sử dụng:
`sudo firewall-cmd --permanent --add-service=https`

![image](https://user-images.githubusercontent.com/105496635/183337549-e69179a8-0189-465f-ac0c-79613c761aa2.png)


## Kiểm tra Web Server
 - Apache trên CentOS sẽ không tự khởi động, mà khởi động thử công, sử dụng lệnh `sudo systemctl start httpd`

![image](https://user-images.githubusercontent.com/105496635/183339799-e7f73bda-968a-4fc3-a7cd-a8b635fd76a9.png)

- Để chắc chắn hơn thì chúng ta sử dụng `sudo systemctl status httpd`


![image](https://user-images.githubusercontent.com/105496635/183339959-a3f088e9-65d4-42f8-934d-f059420d83d2.png)

Sau khi thực hiện lệnh cho kết quả

![image](https://user-images.githubusercontent.com/105496635/183340108-66d8a588-1daf-4e6b-ae7c-03596c256f2c.png)

Như vậy đã hoàn thành cài Apache trên CentOS 7

- Để xem web đã cài thì sử dụng địa chỉ IP của CentOS 7, để xem địa chỉ IP của CentOS 7 sử dụng lệnh `hostnam -I`

![image](https://user-images.githubusercontent.com/105496635/183340859-a33ba8cb-9294-4b53-b1d0-797c18472f07.png)

Sử dụng Ip để truy cập vào máy chủ

![image](https://user-images.githubusercontent.com/105496635/183340999-1b5a187d-e0b7-4509-a693-a6d55e33b6de.png)



