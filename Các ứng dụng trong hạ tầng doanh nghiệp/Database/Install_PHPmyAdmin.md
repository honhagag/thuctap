# Install phpMyAdmin on CentOS 7

[<img src="..\images\Screenshot_1.png">
](https://github.com/chinhtran06062001/hocviecIT/blob/main/Database/phpMyAdmin/images/Screenshot_1.png?raw=true)
*Khái niệm : phpMyAdmin là gì ?

- phpMyAdmin là một công cụ phần mềm miễn phí được viết bằng PHP nhằm xử lý việc quản trị CSDL trên Web. phpMyAdmin hỗ trợ quản lý CSDL của cả MySQL và MariaDB.

- Nó có thể được cấu hình để quản lý cơ sở dữ liệu cục bộ (trên cùng hệ thống) hoặc cơ sở dữ liệu từ xa (qua mạng).

- Các hoạt động thường được sử dụng (quản lý cơ sở dữ liệu, bảng, cột, quan hệ, chỉ mục, người dùng, quyền, v.v.) có thể được thực hiện thông qua giao diện người dùng, trong khi bạn vẫn có khả năng thực hiện trực tiếp bất kỳ câu lệnh SQL nào.


## Điều kiện tiên quyết
- Trên Server đã cài đặt sẵn LAMP Stack (Linux, Apache, MySQL và PHP). Nếu chưa có, bạn có thể xem hướng dẫn cài đặt LAMP Stack trên CentOS 7 tại [đây](https://news.cloud365.vn/huong-dan-cai-dat-lamp-tren-centos-7/)
- Có quyền sử dụng root user hoặc sử dụng các câu lệnh với quyền sudo
- Server cài CentOS 7

## Cài đặt phpMyAdmin
### Bước 1: Cài đặt Kho lưu trữ EPEL
(Nếu đã cài đặt EPEL, bạn có thể bỏ qua bước này.) CentOS 7 không có quyền truy cập vào phpMyAdmin trong kho phần mềm mặc định của nó. Bạn sẽ cần có quyền truy cập vào kho lưu trữ EPEL - Gói bổ sung cho Enterprise Linux.
```
yum install -y epel-release  
```

Làm mới và cập nhật kho EPEL
```
yum –y update
```

### Bước 2: Cài đặt phpMyAdmin trên CentOS 7
```
yum -y install phpmyadmin
```

### Bước 3: Cấu hình và bảo mật phpMyAdmin
#### Hạn chế địa chỉ IP
- Được sử dụng để cấp quyền truy cập từ xa cho một máy trạm. Theo mặc định, phpMyAdmin được cấu hình để server được cài đặt có quyền truy cập.

- File cấu hình : `/etc/httpd/conf.d/phpMyAdmin.conf` , các dòng tham chiếu đến `Require ip` , `Allow from IP` mặc định là `127.0.0.1`

    <img src="..\images\Screenshot_2.png">

- Để cho phép các hệ thống khác truy cập ứng dụng **phpMyAdmin** này, thêm (hoặc thay đổi) địa chỉ IP này thành địa chỉ IP của máy tính bạn muốn cấp quyền truy cập:

    <img src="..\images\Screenshot_3.png">

#### Thay đổi Alias
Thay đổi đường dẫn truy cập trang đăng nhập
- Comment 2 dòng 
    ```
    #Alias /phpMyAdmin /usr/share/phpMyAdmin
    #Alias /phpmyadmin /usr/share/phpMyAdmin
    ```
- Thêm vào đường dẫn của bạn
    ```
    Alias /chinhtran /usr/share/phpMyAdmin 
    ```

- Lưu lại cấu hình vừa chỉnh sửa.

- Khởi động lại dịch vụ Apache để nhận cấu hình mới
    ```
    systemctl restart httpd
    ```

