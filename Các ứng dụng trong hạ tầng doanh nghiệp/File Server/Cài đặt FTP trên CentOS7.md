# Cài đặt FPT server trên CentOS

## 1. Cấu hình FTP trên CentOS 7 bằng VSFTPD
- Cài đặt dịch vụ FTP với VSFTPD
- Trước khi cài đặt cần update máy chủ sử dụng lệnh: 

                yum update -y
                
 hoặc 
 
                 sudo yum update
                 
 ![image](https://user-images.githubusercontent.com/105496635/187586481-d561a9ef-a821-4d33-873a-5cff22f89660.png)
               
                
## 2. Sau đó cài đặt vsftpd

              sudo yum install vsftpd             
                
 ![image](https://user-images.githubusercontent.com/105496635/187587052-4b78d7d7-80ac-422f-9d0e-c17650a5fe4c.png)

![image](https://user-images.githubusercontent.com/105496635/187587182-4c329c75-5b11-4d80-9d19-d2d2f01cf55f.png)
     
 
 ## 3. Khởi động dịch vụ và cho nó chạy cùng hệ thống
 
           sudo systemctl start vsftpd
           sudo systemctl enable vsftpd
 
 
 ![image](https://user-images.githubusercontent.com/105496635/187588183-4041dba8-c6ab-40c6-a328-9aa5f0414e30.png)
 
 ## Tiếp theo, tạo một tường lửa cho phép truy cập FPT trên port 21
  
         sudo firewall-cmd --zone=public --permanent --add-port=21/tcp
         sudo firewall-cmd --zone=public --permanent --add-service=ftp
         sudo firewall-cmd --reload
 
 ![image](https://user-images.githubusercontent.com/105496635/187588561-f2a35bae-588a-4bd9-a4d8-fa3cbb0bfa57.png)

 
 Lưu ý: Nếu bạn đang sử dụng một ứng dụng tường lửa khác, hãy tham khảo tài liệu để cấu hình chính xác cho cổng 21. Ngoài ra, một số client FPT sử dụng cổng 20. Do đó bạn cũng có thể muốn thêm cả quy tắc của cổng đó. Cụ thể là chỉ cần sao chép dòng lệnh, rồi thay đổi 21 thành 20.
 
 ## Kiểm tra trang thái đã hoạt động
  
         systemctl status vsftpd
 
 
 ![image](https://user-images.githubusercontent.com/105496635/187590620-40ec6572-4b47-49b6-b382-bc4d28b4146e.png)

 
 
 
 
 
 
 
 
                
                
