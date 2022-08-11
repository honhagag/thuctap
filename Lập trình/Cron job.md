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

# Cách viết cú pháp đúng 
File cron gồm có 5 trường, mỗi trường đại diện bởi một dấu hoa thị. Chúng dùng để xác định ngày tháng năm và thời gian tác vụ nhất định được thiết lập 
để hoạt động đi hoạt động lại

![image](https://user-images.githubusercontent.com/105496635/184057276-209e242b-736e-4bea-8b61-2ae6e8c6e256.png)

- Minute: Phút của giờ mà lệnh sẽ chạy, trong khoảng từ 0 đến 59 
- Hour : Dựa trên giờ mà lệnh chạy, trong khoảng từ 0 đến 23
- Day of the month: Dựa trên ngày tháng mà  bạn muốn chạy lệnh khoảng từ  1 đến 31
- Month: Dựa trên tháng mà bạn muốn chạy, trong khoảng từ 1 đến 12
- Day of the week: Dựa trên tuần mà bạn muốn chạy, trong khoảng từ 1 đến 12

Thêm vào đó, bạn cần dùng kí tự đúng với mỗi file crontab.

- Dấu hoa thị (*) – để xác định tất cả tham số được lên lịch
- Dấu phẩy (,) – để duy trì 2 hoặc nhiều lần thực thi một lệnh
- Dấu gạch nối (-) – để xác định khoảng thời gian thiết lập lần thực thi một lệnh
- Dấu gạch chéo (/) – để tạo khoảng thời gian nghỉ cụ thể
- Cuối cùng (L) – cho mục đích cụ thể là chỉ định ngày cuối cùng của tuần trong tháng. Ví dụ, 3L nghĩa là thứ tư cuối cùng.
- Ngày trong tuần (W) – để xác định ngày trong tuần gần nhất. Ví dụ, 1W nghĩa là nếu ngày 1 là thứ 7, lệnh sẽ chạy vào thứ hai (ngày 3)
- Hash (#) – để xác định ngày của tuần, theo sau bởi số chạy từ 1 đến 5. Ví dụ, 1#2 nghĩa là ngày thứ Hai thứ hai.
- Dấu chấm hỏi (?) – để để lại khoảng trống
