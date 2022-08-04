# Tìm hiểu về Process trong Linux
## 1. Khái niệm

Một process (tiến trình) , hiểu theo cách đơn giản , là một ví dụ của một chương trình đang chạy. Bất cứ khi nào bạn thông báo một lệnh trong Linux , nó tạo hoặc bắt đầu một process mới.

Mỗi process có 1 PID ( Process ID ) đại diện . PID gồm tối đa 5 chữ số và là duy nhất tại 1 thời điểm . PID của process A có thể được tận dụng cho process B nếu process A đã kết thúc .

- Có 2 loại process :

 - Foreground Process

 - Background Process

## 1.1. Foreground Process

Theo mặc định , mọi process mà bạn bắt đầu chạy là foreground process . Nó nhận input từ bàn phím và gửi output tới màn hình .

Trong khi một chương trình đang chạy trong foreground và cần một khoảng thời gian dài, chúng ta không thể chạy bất kỳ lệnh khác (bắt đầu process khác) bởi vì dòng nhắc lệnh không có sẵn tới khi chương trình đang chạy kết thúc process và thoát ra.

## 1.2) Background Process

Background process chạy mà không được kết nối với bàn phím của bạn . Nếu backround process yêu cầu bất cứ đầu vào từ bàn phím , chương trinh sẽ đợi .

Lợi thế của chạy một chương trình trong background là có thể chạy các lệnh khác : không phải đợi tới khi nó kết thúc để bắt đầu một process mới !

Để bắt đầu một background process , thêm dấu "&" tại cuối lệnh .

#### ping -c 10 8.8.8.8 &















