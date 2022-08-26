# Mô hình triển khai hệ thống thu thập Log cơ bản

## 1. Giới thiệu về log
- Log ghi lại liên tục các thông báo về hoạt động của cả hệ thống hoặc của các dịch vụ được triển khai trên hệ thống và file tương úng. Log file thường là các file văn bản thông thường dưới dạng "clear text", có thể dễ dàng đọc được các trình soạn thảo bằng file bằng các trình soạn thảo văn bản (vi,vim,nano,...) hoặc các trình đọc văn bawnrr thông thường (cat,tailf,head,...) là có thể xem được file log. Các file long có thể giải quyết các vấn đề ứng dụng, tiến trình log.
- Tóm lại: 
  - Log = Thời điểm dữ liệu
  - Log ghi lại thời điểm hoạt động cửa hệ thống

![image](https://user-images.githubusercontent.com/105496635/186794918-45cd265d-484c-45e8-bb78-b7244eab3049.png)

## 2. Vòng đời của file log
-  Đầu tiên nó sẽ được lưu ở máy chủ local sau đó nó sẽ vận chuyển về file log của máy chủ
-  Người quản lí mạng sẽ quản lí sẽ kiểm tra từ file log, từ đó niết được máy chủ client hoạt động những gì
-  Qua bước này người quản lí sẽ phát hiện những hành vi xâm nhập trái phép
-  Sau khi qua phân tích sẽ lưu lại file log khi cần thiết
-  Bước cuối cùng là xóa, người quản lí sẽ xóa nhưng file log không cần thiết

## 3. Công cụ của file log 
- Phân tích nguyên nhân khi có sự cố xảy ra
- Giúp cho việc khác phục hệ thống nhanh hơn khi hệ thống cần
- Giúp phát hiện, xử lí một vấn đề có thể xảy ra đối với hệ thôngs
- Khi xử lí log, người quản lí có thể xử lí 2 vấn đề đó là: xử lí log local và xử lí log tập trung

## 4. Log trên local
- Chỉ lưu lại log trên Server
- Dùng command find, tail... để log xem

![image](https://user-images.githubusercontent.com/105496635/186795711-197ec18e-5ea1-4c9c-b1da-9423e1b97e23.png)

## 5. Log tập trung
- Là quá trình tập trung, thu thập, phân tích các nguồn thu thập khác nhau về một nơi an toàn danh cho việc phân tích, theo dõi hệ thống

## 6. Lợi ích của việc Log tập trung 
- Giúp quản trị viên có cái nhìn tổng về hệ thống, có định hướng giải quyết
- Mọi hoạt của hệ thống được ghi lại và lưu trữ toàn bộ ở một nơi an toàn (Log Server). Đảm bảo việc phân tích các cuộc tấn công vào hệ thống
- Log tập trung  kết hợp với việc phân tích dữ liệu va phân tích log giúp quá trình phân tích log trở nên đơn giản hơn
- Log Local đẩy về Log tập trung
- Mỗi ứng dụng có giao thức đẩy Long khác nhau

![image](https://user-images.githubusercontent.com/105496635/186798113-4d68c67d-5708-4d79-b777-763f9d2d5b1a.png)

## 7. Lợi ích của Log tập trung 
- Để có thể đánh giá khái quát về tình trạng an toàn, an ninh thông tin của một số tổ chức quốc gia thì việc thu thâp, phân tích và lưu trữ các sự kiện an toàn các thiết bị an toàn thông tin từ các thiết bị, dịch vụ và ứng dụng như rounter, swich, firewall, IDS/ÍPS, Mail Secury , Web Security, Anti Virus, ứng dụng Mail Server, Web, cơ sở dữ liệu, hệ điều hành là hết sức cần thiết
- Chính vì thế, hệ thống quản lý Log tập trung hay cao hơn là SIEM được ra đời với mục tiêu thu thập và liên kết tất cả các sự kiện trên cả hệ thống mạng giúp các quản trị viên có cái nhìn tổng quan và thống nhất về các vấn đề trên cả hệ thống.
- Quản trị tập trung Log giúp quản lí và phân tích các sự kiện an toàn thông tin , thực hiện thu thập, chuẩn hóa, phân tích và tường quan toàn bộ sự kiện hệ thống thông tin được sinh ra các thành phần công nghệ sinh của cơ quan, tổ chức
- Quản trị Log tập trung có thể thực hiện các nhiệm vụ sau:
   - Phát hiện các tấn công từ bên ngoài cũng như tấn công về nội bộ 
   - Phát hiện kịp thời những điểm yếu, lỗ hỏng từ thiết bị, ứng dụng và dịch vụ hệ thống
   - Phát hiện các máy tính nghi là nhiễm virus, các máy tính bị nhiễm mã độc và các máy tính bị tình nghi là thành viên máy tính mạng botnet
   - Giám sát viên tuân thủ an ninh quốc gia
   - Cung cấp bằng chứng sau cuộc điều tra sau sự cố






















