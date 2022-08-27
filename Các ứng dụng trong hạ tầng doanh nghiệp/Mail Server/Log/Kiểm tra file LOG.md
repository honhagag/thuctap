# Kiểm tra File Log
- Việc kiểm tra log gửi nhận của email server zimbra là cần thiết, giúp xác định được một email đã gửi/nhận thành công hay chưa và nếu chưa thành công thì bị dừng
-  ở bước nào và báo lỗi ra sao
     
       Đường dẫn file log /var/log/zimbra.log
       
 Chu trình gửi thư => Connect tới email server => MTA kiểm tra địa chỉ người nhận => Kiểm tra qua các rule filter, đánh giá spam, virus => Xếp vào queue => Gửi thư 
 => Xóa khỏi queue => Thông báo Message accepted for delivery

- Để kiểm tra file log đã và đang thực hiện những gì, sử dụng lệnh `tail -f /var/log/zimbra.log`
 
 ![image](https://user-images.githubusercontent.com/105496635/187008185-5deb3387-ae04-4ec5-9175-0af0d6555e9d.png)



Chu trình nhận: Chấp nhận kết nối từ email server gửi => Kiểm tra qua các rule filter, đánh giá spam, virus => Xếp vào queue => Nhận thư và xóa khỏi queue => Thông báo nhận thư 250 2.1.5 Delivery OK
 











