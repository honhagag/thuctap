# Cron job
1. Cron job là chương trình để xử lí các tác vụ  lặp đi lặp lịa ở lần sau. Cron job đưa ra một lệnh  để lên lịch "làm việc" cho một hành động cụ thể, tại một thời điểm
mà cần lặp đi lặp lại
2. Cách hoạt động:
 - Nếu bạn muốn lên lịch lớn cho một lần hoạt động , vào một thời điểm sau này bạn nên cần dùng lệnh khác. Nhưng với những công việc đinh kì thì nên dùng Cron job
 - Cron job là một Daemon, nghĩa là nó hoạt động dưới nền thực thi không cần tương tác. Trong Window nó gọi là Service 
 - Doemon luôn sẵn sàng và đợi khi có câu lệnh yêu cầu chạy một tác động nhất định trong cùng máy tính hoặc cùng mạng lưới
 - File Cron là file text đơn giản chứa các lệnh được chạy trong thời gian cụ thể. File crontab mặc định trong hệ thống là etc/crontab  và nằm trong thư mục 
 crontab /etc/cron/.* /. Chỉ quản trị viên mới được sửa file trong hệ thống 
 - Với Cron job, bạn có thể bảo trì hệ thống , giám sát lưu lượng ổ đia và backup. Bản chất của nó vì vậy hoạt động 24/7-  như server
 - Cron jobs thường được dùng chủ yếu bởi quản trị viên hệ thống nhưng nó cũng có ích với cả quản trị viên web. Ví dụ, dùng cron để hủy kích hoạt tài khoản đã hết hạn,
 - kiểm tra links hỏng, hoặc gửi bản tin cho người dùng mục tiêu.

# Những điều cơ bản về Cron job
Sử dụng Cron job trên ubuntu
