# Những cách triển khai tường lửa
## 1. Stateful firewall(Tường lửa có trạng thái)
 Những tuowfnng lửa đầu tiền được phát triern, chúng không có trjang thái, có nghãi là phàn cứng mà lưu lược truy cập đi qua trong khi được triển tra sẽ theo dõi từng
 gói lưu data hoặc cho phép chúng
 Loại tường lửa này ra đời vào năm 1990, chúng kiểm tra luowjgn truy cajcap, liên quan đén trạng thái  hoặt đọng và đặc điểm kết nối mạng đê cung cấp tường lửa toàn
 diện hơn
 
##  2. Next-generation firewalls - NGFW

- Đây là hệ thống tường lử tiếp theo, chúng được bổ sung thêm nhiều tính năng an toàn mới. Bao gồm eep Packet Inspection - DPI; phát hiện xâm nhập và ngăn vào kiểm tra lưu lượng được mã hóa. Giúp chúng barp vệ toàn diện hơn
- Phần cứng tường lửa: Phần cứng tường lửa là máy chủ đơn giản có thể hoạt động như một router lọc lưu lượng truy cập và phần mềm tường lửa. Chúng thường được sử dụng trong mạng lưới doanh nghiệp, giữa router và điểm kết nối của nahf cing cấp dịch  vụ internet. Một doanh nghiệp có hể truển khao nhiều tường lửa vật lí trong một trung tâm dư liệu
- Phần mềm tường lửa
- hệt hống phần mèm tường lửa quản  lí việc  triern khai các điểm cuối phần cwnsh tường lử. hệ thông trung tam tnafy là nới các chính sch và các tính năng được cấu hình, nó có chức nằng thực hiện phân tích và phản đối các mối đe doan

## 3. Proxy based firewall

Các tường lử nàu hoạt động như một cổng nối giữa người dùng cuối yề cầu dữ liệu proxy lọc qua tất cả lưu luowjgn truy cập này trước khi chsung được chuyển cho người dùng cuối. Như vậy nó giúp che giaasu danh tính của người yêu cần thông tin ban đầu. Điều này có ý nghĩa trong việc bảo vệ máy khach khỏ tiếp xúc mố đe dọa

## 4. Packet-filtering firewalls(tường lửa lọc gói) 

Đây là lọi twuofng lửa được sử dụng phổ biens nhất, chúng này kiểm tra địa chỉ IP nguồn và điịch cảu gói. Hoạt đọng theo pơhuowng thức kiểm tra các gói tin và nếu chúng không khớp với qiy tắc đã thiết lập thì sẽ không để chung qua đi. Packet- filtering firewalls được chia thành hai loại: stateful và stateless. Stateless firewalls kiểm tracasc gói độc lập với nhau và thiếu ngữ canh , stateful và stateless kiểm tea các fois đọc lập với nhau và thiếu ngữ cảnh , statefull firewalls ghi nhiws thông tin về các gói đã truyền trước đó
Khả năng bảo vể của pasket-filtering firewall rất cơ bản và còn nhiều hạn chế. Chúng sẽ dễ dàng bị vo hiệ hóa trong trường hojpe một yêu cầu độc hại được cho phép từ một địa chỉ nguồn đáng tin cậy 


## 5. Web application firewall - WAF (Tường lửa ứng dụng web)

![image](https://user-images.githubusercontent.com/105496635/187828771-844932d8-c929-489c-bf1e-0e381598a35d.png)

Các tường lửa này được sử dụng cho các ứng dụng cụ thể. Khac với tường lử dựa trên poroxy dùng đê bảo vệ máy khaasch ngời dùng cuối, thù tường lửa ứng dụng web bảo vệ máy chỉ ứng dụng

## 6. Kiểm tra trạng thái 

Đây là chức năng tường lửa cơ bản, nó chặn lưu lượng truy cập không mong muốn trong chính sach được cài sẵn

## 7. Diệt virus

Đây là chức năng mới của tường lửa , giúp nó có thể phát hiện ra các mối nguy hại này

## 8. Hệ thống phòng chống xâm nhập

Lớp này bảo mật này có thể được triển khai như một sản phẩm đôc lập hoặc được tích hợp vaof tường lửa thế hệ tiếp theo. Trong khi công nghê tường lửa cơ bản xác định và chặn các loại lưu lượng mạng nhất định, hệ thống IPS được sử dụng nhiều biện pháp bảo mật chi tiết hơn như truy tìm chữ ký, phát hiện bất thường để ngăn chăn các mối đe dọa khồn mong muốn xâm nhập vào mạng công ti

## 9. Phân tích sau ác gói (DPI)
DPI có thể là một phần hoặc được sử dụng kết hợp với về thống IPS, nhưng nó trở thành một tính năng quan trọng của tường lửa thế hệ tiếp theo vì khả năng phân tích lưu lượng truy cập chi tiết, đặc biệt là các tiêu đề của các gói và dữ liệu lưu lượng. DPI cũng có thể được sử dụng để theo dõi lưu lượng gửi đi để đảm bảo thông tin nhạy cảm không rời khỏi mạng công ty, một công nghệ được gọi là ngăn chặn mất dữ liệu (Data Loss Prevention - DLP).

## 9. Kiểm tra SSL 
 Kiểm tra tầng bải mật SSL được sử dụn gđể kiểm tra lưu lượng được mã hóa xem các mối đe dọa khôn. Khi ngày càng nhiều lưu lượng được mã hóa, kiếm tra SSL trờ thành một phần quan trọng của công nghệ DPI đang được triển khai trng tường lửa thees hệ mói. Kiểm tra SSL hoặc động như moojkt buffer giải mã hóa lưu lượng trước kho nó được chuyển đén địa điểm cuối cùng kiểm tra

## 10. Sandboxing là một trong những tính năng mới được triển khai trong tường lửa thế hệ tiếp theo, đề cập đến khả năng của tường lửa để nhận lưu lượng hoặc mã không xác địng và chạy trong nó mối trường thử nghiệm để xác định xem nó có vấn đề gì hay không























