# Truy cập FTP server
- Tạo user

        useradd hoangnon
        useradd hoangnon1

- Đặt pass
        
        passwd hoangnon
        passwd hoangnon1
        
        
 ![image](https://user-images.githubusercontent.com/105496635/187641922-30d81af7-e4ab-4466-98d0-7691416e4c67.png)


Sau khi tạo user thì thư mục mặc định của tài khoản này sẽ ở `/home/hoangnon /home/hoangnon1`
Cấp quyền truy cập đến FTP server    
        
  Cấp quyền truy cập đến FTP server
Tạo file chroot_list trong /etc/vsftpd
Thêm user hoangnon, hoangnon1 vào file /etc/vsftpd/chroot_list để có thể truy cập vào server      
        
Sử dụng lệnh 
       
       nano /etc/vsftpd/chroot_list         
        
  ![image](https://user-images.githubusercontent.com/105496635/187647356-711c1fe6-0fc3-4fbf-93c5-cfeb09a1fdf6.png)

Chỉ định thư mục home khi người dùng đăng nhập vào hệ thống
Tạo thư mục `user_conf`

          mkdir /etc/vsftpd/user_conf

Chỉ định thư mục home cho user `hoangnon` và `hoangnon1` và thêm các dòng lệnh tương ứng với mỗi file

       vi /etc/vsftpd/user_conf/htv1
       local_root=/var/www/htv1



![image](https://user-images.githubusercontent.com/105496635/187652463-745bf3bd-babe-4e05-87e1-79a30c77401c.png)


       vi /etc/vsftpd/user_conf/htv1
       local_root=/var/www/htv

![image](https://user-images.githubusercontent.com/105496635/187652574-0b8c9fed-23c9-45de-9e69-4e103337cf5c.png)


Sau đó restart lại dịch vụ vsftpd

         systemctl restart vsftpd


