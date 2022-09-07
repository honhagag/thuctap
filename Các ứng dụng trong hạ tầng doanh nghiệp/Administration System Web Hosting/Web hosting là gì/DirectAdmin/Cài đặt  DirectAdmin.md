# Chuẩn bị cài đặt DirectAdmin
## Cài đặt Directadmin trên CentOS 7

-  Trước khi cài đặt phần mềm trên mã nguồn mở chúng ta cần cập những tài nguyên

         sudo yum update
         
### Bước 1:  Cài đặt các gói cần thiết
 
          yum install wget gcc gcc-c++ flex bison make bind bind-libs bind-utils openssl openssl-devel perl quota libaio
 
![image](https://user-images.githubusercontent.com/105496635/188778203-ef128151-c279-47c4-9930-912faa77521d.png)



           yum -y install psmisc net-tools systemd-devel libdb-devel perl-DBI xfsprogs rsyslog logrotate crontabs file
         
![image](https://user-images.githubusercontent.com/105496635/188778360-f27966ea-0788-4306-9d91-6720369fcba5.png)

### Bước 2: Tải tập tin setup.sh

           wget http://www.directadmin.com/setup.sh


![image](https://user-images.githubusercontent.com/105496635/188778491-b1000adb-173c-40ef-bcd3-457d01d93e2e.png)


### Bước 3: Thay đổi quyền trên file setup.sh

            chmod 755 setup.sh

![image](https://user-images.githubusercontent.com/105496635/188778614-70bc1c7c-e450-4f39-aa70-45efb1800426.png)

### Bước 4:  Chạy tập lệnh cài đặt DirectAdmin


         ./setup.sh  auto
           

![image](https://user-images.githubusercontent.com/105496635/188779572-94bbe89f-4a6e-4af7-985d-b5f7a5ff8c2b.png)










































































