# Giới thiệu
- Zabbix là một phần mềm mã nguồn mở có chức năng giám sát được sử dụng để thu thập các số liệu từ các thiết bị và hệ thống khác nhau như thiết bị mạng, hệ thống VM, hệ thống Linux/ Window và dịch vụ đám mây. Zabbix có thể gửi thông báo thông báo về các vấn đề trong bât kỳ hệ thống được giám sát nàp

# Điều kiện

- Máy chỉ WEb Apache
- PHP và các extension càn thiết
- Máy chủ Cơ siwr dữ liệu MySQL/ MariDB

# Cài đặt Zabbix trên CentOS

Bước 1:  Trước khi cài đặt chúng ta cần update CentOS
  
           sudo yum update
           
           

- Tiền hành tắt tường lửa

            vi /etc/selinux/config

- Sau đó tiền hành cài đặt httpd và kiểm tra trạng thái

             sudo yum install httpd.service
             systemctl start httpd
             systemctl status httpd.service
 


Bước 2: Cài đặt epel và remi repos

           yum -y install epel-release -y
![image](https://user-images.githubusercontent.com/105496635/189075090-604310fc-7164-45d8-bd10-48365058f830.png)


         yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm

![image](https://user-images.githubusercontent.com/105496635/189075600-cfdb4403-45f4-4b49-b9f2-b6e3add1175b.png)



- Vô hiệu PHP 5 repositories và enable PHP 7.2 repo

        yum-config-manager --disable remi-php54
  
  
 ![image](https://user-images.githubusercontent.com/105496635/189076426-7e567389-c198-44b4-822a-7349c7bbf4a0.png)

        
        
        
        yum-config-manager --enable remi-php72



Bước 3: Cài đặt PHP

             yum install php php-pear php-cgi php-common php-mbstring php-snmp php-gd php-pecl-mysql php-xml php-mysql php-gettext php-bcmath



![image](https://user-images.githubusercontent.com/105496635/189077497-a6aff237-6d30-4e4c-b622-5405d9568980.png)
  
  
  - Chỉnh sửa time Zone PHP tại file php.ini

              vi /etc/php.ini
              date.timezone = Asia/Ho_Chi_Minh

![image](https://user-images.githubusercontent.com/105496635/189078258-a0f24dbf-7b69-4fe5-98e6-aac7bbce8779.png)


Bước 4: Cài đặt MariaDB
Bạn chạy lệnh sau để cài đặt

          yum --enablerepo=remi install mariadb-server
          systemctl start mariadb.service
          systemctl enable mariadb
          systemctl status mariadb.service

![image](https://user-images.githubusercontent.com/105496635/189079264-e5a9b355-70ea-4e5d-b38a-cf6046b96862.png)



Sau đó bạn chạy lệnh sau để cấu hình bảo mật MariaDB

           mysql_secure_installation


Bạn chọn Y và thêm vào pass root mới cho MariaDB và tiếp tục, khi nhận thông báo bạn cứ chọn Y hết nhé.

Sau đó bạn đăng nhập vào DB server và nhập password vào

           mysql -u root -p

Bước 5: Tạo Database cho Zabbix
Bạn thực hiện chạy các lệnh sau sau khi đăng nhập vào DB server

lệnh tạo DB có tên là kblinux

          create database kblinux CHARACTER SET UTF8 COLLATE UTF8_BIN;
Tạo User DB

          create user 'zabbixuser'@'localhost' identified BY 'h1YcadmWzdHr'; 
Gán quyền DB với DB User

           grant all privileges on kblinux.* to zabbixuser@localhost; 
           flush privileges;
            quit;
            
   ![image](https://user-images.githubusercontent.com/105496635/189082672-98faa5b6-7c3b-4da6-a2e5-02dbe7c88fec.png)
         
            
 Bước 6: Cài đặt Zabbix và các
         
           rpm -ivh https://repo.zabbix.com/zabbix/4.0/rhel/7/x86_64/zabbix-release-4.0-1.el7.noarch.rpm
           yum install zabbix-server-mysql zabbix-web-mysql zabbix-agent zabbix-get
           
           
           
           
           
           
![image](https://user-images.githubusercontent.com/105496635/189083982-5e1c0f50-0e81-4428-9f22-2fb03817f2a2.png)



Bước 7: Configure Zabbix


Thay đổi Time Zone trong cấu hình Zabbix Apache

           nano /etc/httpd/conf.d/zabbix.conf


chỉnh sửa:

          php_value date.timezone Asia/Ho_Chi_Minh
Sau đó bạn Restart lại httpd

          systemctl restart httpd.service
Tiếp theo bạn truy cập vào thư mục sau /usr/share/doc/zabbix-server-mysql-4.0.43 và import MySQL.

          cd /usr/share/doc/zabbix-server-mysql-4.0.43    
Lưu ý: Tùy phiên bản mà chổ mình tô đỏ sẽ khác, để chắc chắn bạn kiểm tra và truy cập cho đúng nhé

           zcat create.sql.gz | mysql -u zabbixuser -p kblinux
Mở file zabbix_server.conf tại đây

            vi /etc/zabbix/zabbix_server.conf
Tại đây bạn tìm đến dòng số 91, 100, 116, 125 và thay đổi thông số cấu hình mặc định thành thông tin database mà bạn đã tạo trước đó ở Bước 5


















            
            
            
            

































