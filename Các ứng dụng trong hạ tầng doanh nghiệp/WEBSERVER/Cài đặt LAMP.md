# LAMP

- LAMP là viết tắt của Linux, Apache, MySQL và PHP (cũng có thể là Python, Perl nhưng bài này chỉ nói về Php), mỗi trong số đó là các gói phần mềm riêng lẻ được kết hợp để tạo thành một giải pháp máy chủ web linh hoạt. Các thành phần này, được sắp xếp theo các lớp hỗ trợ lẫn nhau, tạo thành các stack phần mềm

## I. Stack của LAMP

### 1. LAMP Stack là một bộ sofmware mã ngườn mở được sử dụng để phát triển ứng dụng web

![image](https://user-images.githubusercontent.com/105496635/184464022-08d4f413-0cfb-4e43-9a22-76fc83a85c92.png)

- Linux: là lớp đầu tiên trong stack. Hệ điều hành này là cơ sở nền tảng cho các lớp phần mềm khác.
- Apache đóng vai trò một HTTP server dùng để xử lý các yêu cầu gửi tới máy chủ.
- Mysql là cơ sở dữ liệu để lưu trữ mọi thông tin trên website.
- PHP sau đó sẽ xử lý các nhiệm vụ cần thiết hoặc kết nối với CSDL MySQL để lấy thông tin cần thiết sau đó trả về cho Apache. Apache cuối cùng sẽ trả kết quả nhận được về cho máy khách đã gửi yêu cầu tới.

### 2. Ưu điểm của LAMP stack
- LAMP stack gồm  4 thành phần, tất cả đều ví dụ Free and Open- Soucre Software (FOSS). VÌ chúng miễn phí dowload nên thu hút nhiều người sử dụng để tránh phải trả số tiền lớn khi phát triển web của họ
- Vì là FOSS, nên mã nguồn mở của somfware  đuọcư chia sẻ và có sẵn để mọi người thực hiện
- LAM stack được xem là một nền an toàn, vì nếu có lỗi phát sinh thì họ sẽ góp ý để khắc phục sớm nhất
- Điều khiến nó hấp dẫn là bạn có thể điều chỉnh stack và hoán đổi các thành phần Software mà nguồn mở khác để phù hợp với nhu cầu mình
 
### 3. LAMP Stack thay thế
Các lựa chọn thay thế nguồn mở:
- LEMP (Linux, NGINX, MySQL / MariaDB, PHP / Perl / Python)
- LAPP (Linux, Apache, PostgreSQL, PHP)
- LEAP (Linux, Eucalyptus, AppScale, Python)
- LLMP (Linux, Lighttpd, MySQL / MariaDB, PHP / Perl / Python)

Các lựa chọn thay thế không phải nguồn mở gồm:
- WAMP (Windows, Apache, MySQL / MariaDB, PHP / Perl / Python)
- WIMP (Windows, Dịch vụ thông tin Internet, MySQL / MariaDB, PHP / Perl / Python)
- MAMP (Mac OS x, Apache, MySQL / MariaDB, PHP / Perl / Python)

### II. Cơ chế hoạt động các thành phần trong LAMP

#### 1 Sự hoạt động của Linux trong LAMP

Linux cũng đóng vai trò là một hệ điều hành.  Trong LAMP, Linux có vai trò là hệ điều hành mã nguồn mở, được cung cấp hoàn toàn miễn phí. Khi bạn tìm thấy một vài chương trình trong LAMP mà không thấy Linux như Suse, Redhat, Ubuntu,... thì đừng lo, Linux của bạn không hề thiếu vì những chương trình này chính là phiên bản
khác của Linux.

#### 2 Apache được hoạt đọng như thế nào
Apache nắm giữ vai trò là một phần mềm server web phổ biến nhất hiện nay Apache có thế mạnh về độ nhanh chóng khi truy cập và cực kỳ an toàn. Người dùng có thể tùy chỉnh nó để phục vụ cho mục đích hỗ trợ ngôn ngữ web như CGI, PHP, SSL, ASP

 #### 3 MySql 
 Đây là một mã nguồn mở vô cùng phổ biến, có lợi thế lớn từ độ hiệu suất cũng như mức độ uy tín cao, đem đến cho người dùng có thể dễ dàng sử dụng. MySQL đặc biệt tốt khi ứng dụng trên web, đây là một lý do quan trọng khiến cho nó trở nên đặc biệt hiệu quả trong LAMP.

#### 4  PHP hoạt động trong LAMP như thế nào?
PHP là ngôn ngữ kịch bản trong máy chủ và cũng được cập nhật một cách thường xuyên những kỹ thuật mới thông qua cơ chế vay mượn những tính năng tốt nhất từ các ngôn ngữ lập trình.




# Mục lục:

1. cài apache.
2. cài MySQL(MariaDB)
3. cài php
4. kiểm tra việc apache kiểm soát php.
5. cài đặt phpAdmin.

-----------------------------------------------------------------------------------------------

# 1. cài apache:

# Bước 1: Vì Apache có sẵn trong kho lưu trữ của Centos , nên bạn chỉ cần cài đặt bằng lệnh sau

          yum install -y httpd
                     
# Bước 2: Sau khi cài đặt hoàn tất, các bạn có thể sử dụng các lệnh sau để quản lý Apache

          systemctl start httpd      (Khởi động dịch vụ Apache)

          systemctl stop httpd       (Dừng dịch vụ Apache)

          systemctl reload httpd     (Tải lại dịch vụ Apache)

          systemctl restart httpd    (Khởi động lại  dịch vụ Apache:)

          systemctl enable httpd     (Thiết lập Apache khởi động cùng hệ thống)

          systemctl disable httpd    (Vô hiệu hoá Apache khởi động cùng hệ thống )

          systemctl status httpd     (Xem trạng thái dịch vụ Apache)
          
![image](https://user-images.githubusercontent.com/95491130/183229023-bdfd091e-8a58-444c-ae9c-96d4e7563cef.png)

          
# Bước 3: Mặc định trên Centos 7 sẽ sử dụng tường lửa là Firewall, nên các bạn cần thực hiện mở Port dịch vụ Apache với Firewall theo các cách sau

              firewall-cmd --permanent --zone=public --add-service=http

              firewall-cmd --permanent --zone=public --add-service=https

              firewall-cmd --reload
          
![image](https://user-images.githubusercontent.com/95491130/183229076-7597ac48-5077-4fa7-b509-8e83ee2d4443.png)
           
# 2. cài đặt mariaDB

# Bước 1: Để cài đặt MariaDB, bạn cần thực hiện lệnh sau

          yum install -y mariadb mariadb-server
       
# Bước 2: Sau khi cài đặt hoàn tất, bạn có thể sử dụng các lệnh sau để quản lý MariaDB

          systemctl start mariadb      (Khởi động dịch vụ mariadb)

          systemctl stop mariadb      (Dừng dịch vụ mariadb)

          systemctl restart mariadb    (Khởi động lại  dịch vụ mariadb)

          systemctl enable mariadb     (Thiết lập mariadb khởi động cùng hệ thống)

          systemctl disable mariadb    (Vô hiệu hoá mariadb khởi động cùng hệ thống )

          systemctl status mariadb     (Xem trạng thái dịch vụ mariadb)

![image](https://user-images.githubusercontent.com/95491130/183229134-53a018a3-9c9f-4fa8-8e91-421b874ddd43.png)

# Bước 3: Thiết lập bảo mật MariaDB Server

          mysql_secure_installation
          
- Khi được nhắc nhập mật khẩu, ta có thể nhấn Enter để trống hoặc cập nhật mật khẩu mới
Sau đó làm các bước để thiết lập mật khẩu. Cuối cùng, tập lệnh sẽ yêu cầu định cấu hình một số biện pháp bảo mật, bao gồm:

       Xóa người dùng ẩn danh?

       Không cho phép đăng nhập từ xa?

       Xóa cơ sở dữ liệu thử nghiệm và truy cập vào nó?

       Tải lại bảng đặc quyền ngay bây giờ

![image](https://user-images.githubusercontent.com/95491130/183228976-18ce1768-a94e-4aa7-9a32-844f87dca8ac.png)


![image](https://user-images.githubusercontent.com/95491130/183228979-751d8186-f7ea-4a6c-9d74-b2cd22cca027.png)


# 3. cài PHP.

- Phiên bản PHP có sẵn CentOS 7 là các bản cũ và đã lỗi thời và vì lý do đó, các bạn nên cài đặt kho lưu trữ gói của bên thứ ba để có thể sử dụng các phiên bản PHP mới nhất . Và Remi là kho lưu trữ gói phổ biến cung cấp các bản phát hành PHP mới nhất cho các máy chủ CentOS.

# Bước 1: Để cài đặt kho Remi các bạn chạy lệnh sau

          yum install -y yum-utils https://rpms.remirepo.net/enterprise/remi-release-7.rpm

![image](https://user-images.githubusercontent.com/95491130/183229216-193f0e95-a598-473f-9d47-19ea01c31e51.png)

# Bước 2: Sau khi cài đặt gói Remi xong, các bạn cần chọn phiên bản PHP mà mình cần cài đặt và kích hoạt gói chứa phiên bản PHP đó. Ở hướng dẫn này mình sẽ cài đặt PHP 8.0 nên sẽ kích hoạt gói bằng lệnh sau

          yum-config-manager --enable remi-php80
          
# Bước 3: Khi module remi-80 của PHP đã được bật, bạn có thể tiến hành cài đặt PHP và các PHP Extension cần thiết bằng lệnh bên dưới:

          yum install -y php php-ldap php-zip php-embedded php-cli php-mysql php-common php-gd php-xml php-mbstring php-mcrypt php-pdo php-soap php-json php-simplexml php-process php-curl php-bcmath php-snmp php-pspell php-gmp php-intl php-imap perl-LWP-Protocol-https php-pear-Net-SMTP php-enchant php-pear php-devel php-zlib php-xmlrpc php-tidy php-opcache php-cli php-pecl-zip unzip gcc

![image](https://user-images.githubusercontent.com/95491130/183229549-4cfa1713-d5fc-4696-aab1-8e85e305e140.png)

# Bước 4: hiên bản PHP vừa cài đặt bằng cách

            php -v
            
![image](https://user-images.githubusercontent.com/95491130/183229568-366afd40-84ce-4371-908d-e06594cff48a.png)

# 4. kiểm tra việc apache kiểm soát php.

- Thư mục gốc web mặc định là /var/www/html. Ta tạo một tệp PHP (info.php) trong thư mục này để kiểm tra Apache xử lý PHP.

# File info.php sẽ hiển thị thông tin chi tiết phiên bản PHP mà chúng ta cài đặt

          nano /var/www/html/info.php

- Dán nội dung sau vào file:

                <?php
                phpinfo();
                ?>

![image](https://user-images.githubusercontent.com/95491130/183229889-bb75497a-70e0-42f3-9f7b-a489c796b928.png)

- Sau đó tiến hành “Lưu lại”

# Bây giờ các bạn mở trình duyệt lên và gõ địa chỉ:http://192.168.44.128/info.php, nếu kết quả hiển thị như hình dưới là việc cài đặt của chúng ta đã thành công

![image](https://user-images.githubusercontent.com/95491130/183229873-1b79a618-565d-4e9a-9f58-df37033b87dc.png)

# 5. Cài đặt PhpAdmin(tùy chọn).

- pMyadmin là một trình quản lý Mysql server trên giao diện web, giúp chúng ta dễ dàng thao tác với Database hơn

- phpMyAdmin có trong repository EPEL (Gói bổ sung cho Enterprise Linux). Để truy cập EPEL, bạn cần install gói đặc biệt – epel-release.

# bước 1: Sử dụng lệnh sau để install epel-release CentOS:

        yum install epel-release
               
# Bước 2: Cài đặt phpMyadmin

        yum install phpmyadmin

# Bước 3: Cấu hình phpmyadmin, bạn vào file phpmyadmin.conf để thiết lập

        nano /etc/httpd/conf.d/phpMyAdmin.conf

- đây bạn sẽ thấy 4 chuỗi ip yêu cầu khác nhau, khớp với chuỗi IP dài. Giá trị mặc định là 127.0.0.1. Thay thế giá trị đó bằng IP máy bạn sẽ sử dụng để truy cập phpMyAdmin

![image](https://user-images.githubusercontent.com/95491130/183231825-a424cb4e-6430-4a94-82f0-b0ed2ea1c00d.png)

![image](https://user-images.githubusercontent.com/95491130/183231842-24ab554a-51d3-4e26-bac1-c88f2c8b4723.png)


 # Bước 4: Khởi động lại Apache web server

          systemctl restart httpd

#  trình duyệt, vào đường dẫn sau để truy cập vào phpMyadmin: https://192.168.44.128/phpmyadmin

![image](https://user-images.githubusercontent.com/95491130/183231868-76096799-cbbb-4124-8f91-85e3fd31d525.png)


# đăng nhập vào bằng tài khoản root để kiểm tra:

![image](https://user-images.githubusercontent.com/95491130/183231967-0dbf4158-5fc1-4705-a327-5cc5d7e5b16a.png)

![image](https://user-images.githubusercontent.com/95491130/183231975-763ed3be-3b5c-4dfe-9625-e4ecd0efd9a0.png)







