# File Log trong Zimbra
## 1. Để truy cập vào file Log sử dụng lệnh `cd /opt/zimbra/log` và sau đó dùng `ls` để hiện toàn bộ long

![image](https://user-images.githubusercontent.com/105496635/187014065-25c86795-02db-4f86-992f-e92b012c7c8d.png)

## 2. Mail.log
- Trong đó mailnox.log là nơi lưu dữ gian mức làm độ của công việc tac vụ,  địa chỉ ip và cũng như liên quan đến sự việc
- Log level thể hiện mức độ ảnh hướng của sự kiến đến của mail server. Mặc định có 4 mức độ INFO, WARN, ERROR, và FATAL
   - INFO - Các Event tại mức độ này có mức đích thông báo của tiến trình của Zimbra như việc tạo, xóa Messger , ...
   - WARN - Các Event tường này có mức độ tiềm tàng nhưng không ảnh hướng đến hoặt động Server, ví dụ như về sự kiện đăng nhập sai của người dùng
   - ERROR - Thể hiện lỗi xyar ra nhưng lại không ảnh hưởng đến hoạt động cửa server, ví dụ như cảnh báo về inddexx dữ liệu của người dùng
   - PATAL - Hiển thị lỗi server hoạt động không ổn đinh và mất kết nối tới đến cơ sở dữ liệu
- Các file log được thực hiện cập nhật hằng ngày. Phiên bản cuối cùng luôn có tên là mail.log các file trước được đặt tên theo ngày ví dụ như

mailbox.log.2022-08-26.tar.gz.

## 3. Các file log khác

Thư mục /opt/zimbra/log còn chứa các file log khác, lưu lại các thông tin đặc thù như audit.log thể hiện đăng nhập thành công hoặc không.

Bạn có thể dùng lệnh` grep -ir "invalid password" /opt/zimbra/log/audit.log` để xem những lần đăng nhập không thành công của user.B


![image](https://user-images.githubusercontent.com/105496635/187014907-ff9fcf94-03e9-48da-af4e-70d7015d8015.png)


Bạn có thể tìm theo từ khóa FATAL khi server bị các sự cố nghiêm trọng. Hoặc tìm theo từ khóa ImapServer, Pop3Server khi muốn tìm thông tin liên quan đến giao thức pop3 hay imap.

## 4. Một số cách tìm kiếm lỗi

Tìm lỗi trong FATAL và ERROR

  `grep -iE 'fatal|error' mailbox.log`
  
  
![image](https://user-images.githubusercontent.com/105496635/187014982-5322ccc8-2912-42e9-bc49-bf1afbc5fab7.png)

Trong ảnh thể hiện lỗi đăng nhập không thành công do mật khẩu không hợp lệ

Tìm kiếm các log level info|warn và xung quanh đó.

            grep -iEv -C3 'info|warn' mailbox.log
            
            
Tìm kiếm Hiển thị thêm một số dòng sau đó

           grep -iEv -A3 'info|warn' mailbox.log

Lọc theo từ khóa từ trái sang phải, đầu tiên là user1 sau đó là user2

           grep -iE user1 /var/log/zimbra.log | grep user2
           
Giám sát user1 từ nhiều log file khác nhau theo thời gian thực           
           
             tail -f mailbox.log -f trace_log.2015_03_11 -f access_log.2015-03-11 -f sync.log -f ews.log | grep -i user1
## 5. Zimbra cho phép quyền truy vết thông tin người gửi email 
      `zmmsgtrace, chạy với quyền root.`

![image](https://user-images.githubusercontent.com/105496635/187018779-b483e7d6-f16c-47d2-8416-5539ee523673.png)


Truy vết người gửi mail bằng lệnh

   ` /opt/zimbra/libexec/zmmsgtrace -s admin@mail.xn--hoangvip-1ya8k.vn`

![image](https://user-images.githubusercontent.com/105496635/187018856-7a10b750-f2fd-4fb4-816d-bb7687d52838.png)


Truy vết theo địa chỉ người nhận:

`/opt/zimbra/libexec/zmmsgtrace -r @mail.xn--hoangvip-1ya8k.vn`

![image](https://user-images.githubusercontent.com/105496635/187019065-df50dbba-2ce1-4787-b0bc-35ca7849625a.png)


Trace từ các file log khác nhau

`/opt/zimbra/libexec/zmmsgtrace -r '@gmail.com' /var/log/zimbra*`


## 6. Logger
- Để thiết lập ghi log tập trung trong một hệ thống Zimbra có nhiều server bạn cần cấu hình một host để thu nhận log. Thường bạn sẽ dùng mailbox server, cài đặt logger để thu thập log.

- Logger server sẽ thu thập thông tin thống kê, trạng thái của các service trên các server khác, zimbra.log được lưu tập trung nhưng các log khác như mailbox.log và audit.log được lưu theo kiểu round robin trên các mailstore server. Muốn tập trung các log này về một log server riêng, zimico khuyến cáo bạo dùng 1 giải pháp lưu và phân tích log tập trung của bên thứ 3 như Graylog.

- Các bước thực hiện.
    - Cài đặt logger của zimbra lên mailbox server này.
    - Edit file /etc/sysconfig/rsyslog và cấu hình SYSLOGD_OPTIONS="-r -c 2"
    - Edit /etc/rsyslog.conf và kích hoạt 2 dòng sau:
$ModLoad imupd $UDPServerRun 514 systemctl restart rsyslog su - zimbra /opt/zimbra/bin/zmsshkeygen /opt/zimbra/bin/zmupdateauthkeys /opt/zimbra/libexec/zmloggerinit Bạn kiểm tra thông số: zmprov gacf | grep zimbraLogHostname Trên các server khác, đảm bảo rằng thông số hiện tại là tên mailbox server đã được cài dịch vụ logger. Ngoài ra trên các server còn lại, chạy các lệnh sau: su - zimbra /opt/zimbra/bin/zmsshkeygen /opt/zimbra/bin/zmupdateauthkeys exit /opt/zimbra/libexec/zmsyslogsetup systemctl restart rsyslog su - zimbra zmcontrol restart
