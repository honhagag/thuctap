#  Cấu hình dịch vụ VSTFTPD
File cấu hình: /etc/vsftpd/vsftpd.conf

## 1. Trước khi bắt đầu, hãy tạo ra một bản sao của file cấu hình mặc định

  `sudo cp /etc/vsftpd/vsftpd.conf /etc/vsftpd/vsftpd.conf.default`

Việc này đảm bảo bạn có cách để quay trở lại cấu hình mặc định nếu gặp sự cố trong quá trình cài đặt.

## 2.  Sau đó, chỉnh sửa file cấu hình với lệnh:

`sudo nano /etc/vsftpd/vsftpd.conf`

### - Các tham số cơ bản

Khi bật tham số listen, vsFTPd chạy ở mode stand alone và lắng nghe trên socket IPv4

`listen = YES`

![image](https://user-images.githubusercontent.com/105496635/187616824-ee9c2075-a933-472b-918d-b6cb2139a3e6.png)


Cho phép các kết nối không chứng thực (anonymous). Tham số sẽ tự động kích hoạt nếu ta comment tham số.

`anonymous_enable=YES`


![image](https://user-images.githubusercontent.com/105496635/187614023-87d76e01-cd9a-4706-bceb-77b153181616.png)

Cho phép user local truy cập:

`local_enable=YES`
![image](https://user-images.githubusercontent.com/105496635/187614235-0ea74037-6488-453b-b379-70280a1e8cc1.png)


Cho phép user quyền truy cập chỉnh sửa file trên server:

`write_enable=YES`

![image](https://user-images.githubusercontent.com/105496635/187614312-7e22c7f9-8096-49fa-a3d9-b3365d1c8851.png)


Cho phép người dùng ẩn danh upload file (tính năng này chỉ có hiệu lực nếu tham số write_enable được bật). Thêm vào đó, bạn cần tạo đường dẫn cho phép người dùng ẩn danh chỉnh sửa.

`anon_upload_enable=YES`
 
 ![image](https://user-images.githubusercontent.com/105496635/187614496-6bf582e9-11e8-4fdb-be25-4a2c1f4c8ef4.png)

 

Cho phép người dùng ẩn danh tạo đường dẫn thư mục mới:

`anon_mkdir_write_enable=YES`

![image](https://user-images.githubusercontent.com/105496635/187614614-45f5824c-62fc-49b5-bfb9-9716fad47031.png)


Chroot hiểu đơn giản là kỹ thuật “giam” một chương trình, dependencies và library cần thiết kế để chạy chương trình vào một folder tách biệt với hệ thống để nâng cao tính bảo mật. Và nếu chương trình đó bị xâm nhập trái phép thì nó chỉ ảnh hưởng trong nội tại như thư mục đó mà thôi.

Trong bài viết này, chúng ta sẽ học cách bật mí tính năng chroot cho các user khi đăng nhập vào FTP Server. Ta có các tùy chọn sau:


Chroot tất cả user:


    chroot_local_user=YES
    chroot_list_enable=NO

![image](https://user-images.githubusercontent.com/105496635/187616985-1f314001-a97f-4e87-8dea-3ef8a29d4af1.png)


Chỉ chroot đối với một số user nằm trong danh sách được tạo nên đường dẫn /etc/vsftpd.chroot_list:


     chroot_local_user=NO
     chroot_list_enable=YES

Chroot tất cả user ngoại trừ danh sách các user được liệt kê tại /etc/vsftpd.chroot_list:
 
       chroot_local_user=YES
       chroot_list_enable=YES

Hạn chế các user truy cập vào FTP Server

      userlist_deny=YES
      userlist_file=/etc/vsftpd.denied_users

Hoặc có thể cấm tất cả các user truy cập FTP và lập danh sách những người được truy cập.


       userlist_deny=NO
       userlist_enable=YES
       userlist_file=/etc/vsftpd.allowed_users

![image](https://user-images.githubusercontent.com/105496635/187618737-504e9d9e-a379-4aec-8284-d76891e224ce.png)

Banner khi người dùng login vào FTP server
        
        ftpd_banner="Welcome FTP Server"

![image](https://user-images.githubusercontent.com/105496635/187620717-1884bc70-bbf2-4f8d-9a26-f9b759ba64aa.png)

















