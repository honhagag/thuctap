# CSF
## 1. Giới thiệu
- Để bảo vệ Webserver của mình chống lại các cuộc tấn công DDos, Flood, Syn Flood, Port Sacn... ta cần phải cài tường lửa-  Firewall cho nó. Có rất nhiều chương trình
Firewall cài đặt trên VPS nhưng CSF(CpnfigServer Securitu & Firewall) là mọt trong những firewall nhỏ gọn và hoạt động hiệu quả nhất
- CSF Firewall được cung cấp miễn phí và hoạt và hoạt động dựa trên iptables và tiến trình ldf để quét các file log để phát hiện các dấu hiệu tấn công nên hầu như không sử dụng nhiều tài nguyên của máy chủ. Vì vậy cài đặt CSF Firewall vừa giúp bạn bảo vệ máy chủ chống lại các cuộc tấn công nhưng vẫn đảm bảo hiệu xuất tối đa cho websitr

## 2. Tác dụng CSF firewall đối cới máy chủ Webserver
- Hạn chế được các cuộc tấn công Ddos
- Block IP đang Sac Port máy chủ
- Chống BrutrForce Attack vào FTP server, web server, mail server, Directadmin ,cPanel
- Block IP Syn Flood
- Block IP Ping Flood
- Cho phép chúng ta không cho try cập từ 1 quốc gia nào đó rất đơn giản bằng cách chỉ định Country Code chuẩn IOS
- Hỗ trợ IPV4  và IPV6
- Khi phát hiện tấn công từ một IP cụ thể, sẽ khóa tạm thời hoặc vĩnh viễn ở tầng mạng (an toàn hơn ở tầng ứng dụng ) nên webserver ko phải xử lý các yêu cầu từ các IP bị cấm, không ảnh hưởng tới hiệu suất phục vụ.
- ho phép bạn chuyến hướng yêu cầu từ các IP bị khóa sang 1 file .html định sẵn để thông báo cho người dùng biết IP của họ bị chặn truy cập (block) tạm thời hoặc vĩnh viễn.

















