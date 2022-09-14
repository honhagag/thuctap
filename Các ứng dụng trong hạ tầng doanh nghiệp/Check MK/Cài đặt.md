# Cài đặt
## 1. Hướng dẫn cài đặt
- Bước 1: Update phần mềm trước khi cài đặt
 
            sudo yum update

- Bước 2: Cài đặt repo EPEL

Check MK cần khác nhiều các gói dependence đi kèm, vì thế chúng ta cần cài đặt thêm gói repo này để có thể đáp ứng một sối gói mà local không cung cấp.

            yum install -y epel-release wget        

![image](https://user-images.githubusercontent.com/105496635/190087705-b6639d92-0be3-4b27-b0f6-d32fb837d79c.png)


Và kết quả sau khi cài đặt

![image](https://user-images.githubusercontent.com/105496635/190087841-4c081a0f-ddf8-4dbb-9c42-197d6b169f88.png)

- Bước 3: Tải file cài đặt OMD - Check MK


          wget https://download.checkmk.com/checkmk/2.0.0p26/check-mk-raw-2.0.0p26-el7-38.x86_64.rpm


![image](https://user-images.githubusercontent.com/105496635/190088057-2a74812f-1d46-46da-9bcf-04234e2f1ea7.png)


- Bước 4: Cài đặt OMD- Check MK

 Sử dụng lệnh 
 
                  wget http://mathias-kettner.de/download/check_mk-agent-1.2.4p5-1.noarch.rpm

![image](https://user-images.githubusercontent.com/105496635/190094286-1f135a20-a621-409f-b853-107c643e458d.png)


Sau khi tải xuống chúng ta giải ném tập tin :

            yum install check_mk-agent-1.2.4p5-1.noarch.rpm
 
                   
- Bước 5: Tạo và khởi động site trên OMD

Tạo site

          omd creat hoangga
          
   `hoangga` là cái tên mình tạo

![image](https://user-images.githubusercontent.com/105496635/190102383-4e0012e3-0dc0-4647-8ec8-ca5139f1d0c6.png)


Khởi động site       `omd start hoangga`


![image](https://user-images.githubusercontent.com/105496635/190104772-523cabf5-30d7-4f30-8b1c-974f094edd8b.png)


- Mở port 80 cho HTTPD trên Firewalld

- Nếu server của bạn có sử dụng Firewalld, hãy mở port cho httpd bằng lệnh:

       firewall-cmd --permanent --add-port=80/tcp
       firewall-cmd --reload


Tắt SELinux

     setenforce 0


Chỉnh sửa file cấu hình của SELinux:

    vi /etc/sysconfig/selinux 
    
Để tắt tường lửa

Sửa dòng` SELINUX=enforcing` thành `SELINUX=disabled.`



## 2. Kiểm tra và check user

- Sử dụng lệnh `omd status hoangga` để check thông tin tài khoản

![image](https://user-images.githubusercontent.com/105496635/190122476-e1e982a4-242f-4b4b-92c0-31f873317a79.png)



Nhập địa chỉ ip và tên đã tạo để truy cập và sau đó sử dụng tài khoản mật khẩu đã check để đăng nhập

http://192.168.110.163/hoangga

Tài khoản : cmkadmin
Mật khẩu : yuB5EPUS


![image](https://user-images.githubusercontent.com/105496635/190122761-b6b22001-8994-49b8-9ec6-7d33ae458a70.png)
















































