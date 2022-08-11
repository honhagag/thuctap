# Cron job
## 1. Cron job là gì
 Cron job là chương trình để xử lí các tác vụ  lặp đi lặp lịa ở lần sau. Cron job đưa ra một lệnh  để lên lịch "làm việc" cho một hành động cụ thể, tại một thời điểm
mà cần lặp đi lặp lại
 Cách hoạt động:
 - Nếu bạn muốn lên lịch lớn cho một lần hoạt động , vào một thời điểm sau này bạn nên cần dùng lệnh khác. Nhưng với những công việc đinh kì thì nên dùng Cron job
 - Cron job là một Daemon, nghĩa là nó hoạt động dưới nền thực thi không cần tương tác. Trong Window nó gọi là Service 
 - Doemon luôn sẵn sàng và đợi khi có câu lệnh yêu cầu chạy một tác động nhất định trong cùng máy tính hoặc cùng mạng lưới
 - File Cron là file text đơn giản chứa các lệnh được chạy trong thời gian cụ thể. File crontab mặc định trong hệ thống là etc/crontab  và nằm trong thư mục 
 crontab /etc/cron/.* /. Chỉ quản trị viên mới được sửa file trong hệ thống 

## Chức năng Cron job

##### Tự động hoá các tác vụ cơ bản của máy chủ – tính năng nổi bật của Cron Jobs
- Tự động Backup dữ liệu hệ thống định kì
- Tự động gửi email: email định kì cho khách hàng, gửi báo giá hay thông báo các bản tin mới theo thời điểm do khách hàng của bạn tùy chọn, …
- Tự động thực hiện một lệnh nào đó trong Linux do người dùng tạo ra: cập nhật số liệu, quét chỉ mục, cache dữ liệu hệ thống, …

#### ƯU ĐIỂM KHI SỬ DỤNG CRON JOBS
Nhờ Cron Jobs, bạn sẽ tiết kiệm được lượng lớn thời gian, không phải quản lý máy chủ lưu trữ và các tác vụ liên quan. Nếu là nhân viên văn phòng, bây giờ bạn hoàn toàn có thể về nhà, thư giãn sau một ngày miệt mài 8 tiếng trong văn phòng thay vì dành buổi tối của họ sao lưu các tập tin và quản lý địa chỉ liên lạc.

Song song đó, bạn cũng không cần phải cố gắng ghi nhớ và tạo đi tạo lại những công việc định kì.

#### Nhược điểm
Cron Jobs chỉ có thể thực hiện câu lệnh theo chu kỳ 1 phút trở lên, trong trường hợp muốn thực hiện các công việc lặp lại theo chu kỳ 1s, 5s, 10s, … thì CronTab sẽ không làm được.

Để CronJob có thể thực hiện theo chu kỳ 1s, 2s, 3s, …. , bạn hãy yêu cầu nhà cung cấp dịch vụ hỗ trợ nhé.



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

# Ví dụ về cú pháp của Cronjob

Khi muốn bạn muốn dừng nhận những email có thể thêm >/dev/null 2>&1 vào cú pháp như ví dụ bên dưới:

`0 5 * * * /root/backup.sh >/dev/null 2>&1`

Nếu bạn muốn gửi email output đến một tài khoản cụ thể, thêm MAILTO và sau đó là địa chỉ email. Đây là ví dụ:

`ILTO="myname@hostinger.com"
0 3 * * * /root/backup.sh >/dev/null 2>&1`

|Cú pháp|Ý nghĩa|
|-|-|
|0 0 * * * /bin/sh backup.sh|Để chạy cơ sở dữ liệu backup vào giữa đêm, và chạy sau 1 ngày.|
|0 6,18 * * * /bin/sh backup.sh|	Để chạy backup cơ sở dữ liệu 2 lần 1 ngày lúc 6AM và 6PM.|
|0 */6 * * * /scripts/monitor.sh|	Để thực thi giám sát mỗi 6 giờ.|
|*/10 * * * * /home/user/script.sh|	Để chạy cron job cho file script đặt trong thư mục chính mỗi 10 phút.|
|0 * 20 7 * /bin/sh backup.sh|	Để chạy cơ sở dữ liệu backup mỗi giờ mỗi ngày 20/07.|
|0 0 * * 2 * /bin/sh|	Để chạy cơ sở dữ liệu backup giữa đêm mỗi thứ ba.|
|* * * 1,2,5 *  /script/script.sh|	Để chạy lệnh vào tháng một, tháng hai và tháng năm.|
|10-59/5 5 * * * /home/user/script.sh|	Để chạy lệnh mỗi 5 phút lúc 5AM, bắt đầu lúc 5:10 AM.|
|0 8 1 */3 * /home/user/script.sh	|Để chạy lệnh hàng quý vào ngày 1 lúc 8AM.|
|* * * * * /scripts/script.sh; /scripts/scrit2.sh|	Để đặt lịch nhiều jobs trên cron job độc lập.|
|@reboot /scripts/script.sh	|Để chạy tác vụ nhất định mỗi khi bạn khởi động hệ thống.|
|0 0 1 * *  /home/user/script.sh|	Để chạy lệnh vào ngày đầu tiên của mỗi tháng.|

