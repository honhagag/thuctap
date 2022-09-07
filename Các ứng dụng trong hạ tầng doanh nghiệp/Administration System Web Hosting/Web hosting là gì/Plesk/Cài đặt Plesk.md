# Cài đặt Plesk
### Bước 1: - Kiểm tra trạng thái của selinux và iptables. Nếu 2 dịch vụ này bật, vui lòng turn off trước khi quá trình cài đặt Plesk-Panel

-Câu lệnh kiểm tra trạng thái dịch vụ 

           sestatus

 ![image](https://user-images.githubusercontent.com/105496635/188808896-5ca6fbc7-c389-4e45-9f94-4c80e9a18c88.png)

             selinux: enabled -> dịch vụ đang được bật
             selinux: disabled -> dịch vụ đang được tắt

- Sử dụng lệnh để tắt

             vi /etc/selinux/config 
           

### Bước 2: Xóa bỏ các gói dịch vụ đã có sẵn (nếu có) : httpd, sendmail, mysql, postfix thông qua câu lệnh :

                  yum -y remove httpd sendmail mysql* postfix


### Bước 3: Cài đặt gói dịch vụ wget

                    yum -y install wget



### Bước 4: Tải file cài đặt Plesk bằng cách chạy câu lệnh sau:

                       wget http://autoinstall.plesk.com/plesk-installe

![image](https://user-images.githubusercontent.com/105496635/188810310-cd582567-ba4d-458c-9056-383f4fc8fdc7.png)



### Bước 5: Cấp quyền 
           
                    chmod +x plesk-installer

Sau khi đã hoàn tất download, tiến hành cài đặt plesk bằng câu lệnh sau:


                   ./plesk-installer


![image](https://user-images.githubusercontent.com/105496635/188811041-c2381574-36bc-449a-aefb-02243b6dbcec.png)
               



### Bước 6: Nhập các lệnh theo yêu cầu

![image](https://user-images.githubusercontent.com/105496635/188811344-c54c764a-8b2a-4421-a913-21215c1a9f35.png)

### Bước 7: Chọn gói Plesk cần cài đặt với các lựa chọn như Full, Recommended Custom như bên dưới. Ở đây ta sẽ lấy ví dụ chọn gói cài đặt Recommended và chọn F để tiếp tục. 

![image](https://user-images.githubusercontent.com/105496635/188811954-4349e3da-6ff2-4805-8877-a61eef45e048.png)


### Bước 8: Thông báo cần nâng cấp 3 gói để có thể tiến hành cài đặt, nhấm F để tiếp tục


![image](https://user-images.githubusercontent.com/105496635/188812216-8ccea673-ab5e-49da-9d0f-244b4601dbf6.png)

### Bước 9: Hoàn tất quá trình cài đặt, truy cập vào trang https://:8443 để tiếp tục cài đặt như các phiên bản khác với thông tin như sau:



































































































































































