# File Log trong Zimbra
1. Để truy cập vào file Log sử dụng lệnh `cd /opt/zimbra/log` và sau đó dùng `ls` để hiện toàn bộ long

![image](https://user-images.githubusercontent.com/105496635/187014065-25c86795-02db-4f86-992f-e92b012c7c8d.png)

2. Mail.log
- Trong đó mailnox.log là nơi lưu dữ gian mức làm độ của công việc tac vụ,  địa chỉ ip và cũng như liên quan đến sự việc
- Log level thể hiện mức độ ảnh hướng của sự kiến đến của mail server. Mặc định có 4 mức độ INFO, WARN, ERROR, và FATAL
   - INFO - Các Event tại mức độ này có mức đích thông báo của tiến trình của Zimbra như việc tạo, xóa Messger , ...
   - WARN - Các Event tường này có mức độ tiềm tàng nhưng không ảnh hướng đến hoặt động Server, ví dụ như về sự kiện đăng nhập sai của người dùng
   - ERROR - Thể hiện lỗi xyar ra nhưng lại không ảnh hưởng đến hoạt động cửa server, ví dụ như cảnh báo về inddexx dữ liệu của người dùng
   - PATAL - Hiển thị lỗi server hoạt động không ổn đinh và mất kết nối tới đến cơ sở dữ liệu
- Các file log được thực hiện cập nhật hằng ngày. Phiên bản cuối cùng luôn có tên là mail.log các file trước được đặt tên theo ngày ví dụ như

mailbox.log.2022-08-26.tar.gz.

3. 




















