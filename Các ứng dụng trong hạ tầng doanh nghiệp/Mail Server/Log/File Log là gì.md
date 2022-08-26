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

- Tóm lại, việc xây dựng một giải pháp quản lý tập trung Log hợp lý sẽ giúp cải thiện hiệu quả cho hệ thống giám sát an ninh trong việc phân tích và xử lý các biến cố. Các phân tích viên sẽ tốn ít thời gian cho việc đánh giá chính xác được các biến cố nếu khả năng tự động của hệ thống gặp trục trặc.

- Một giải pháp tốt sẽ cho phép tất cả các biến cố an ninh quan trọng được thu thập và lưu trữ vào cơ sở dữ liệu nhằm cung cấp thông tin cho các phân tích viên an ninh, các đội ứng phó sự cố, và các bộ phận khác của tổ chức.
 
 ## 8. Khái quát về hệ thống thu thập Log tập trung ELK
 Elastic Stack (ELK Stack) là một nhóm phần mềm mã nguồn mở, dựa trên Elastic nó cho phép tìm kiếm, thu thập, phân tích, thực hiện các log thu thập từ các nguồn, các   log này là bất kì dạng nào ELK là trung tâm phân tích log. Trung tâm này sở hữu khi trợ giúp các vấn đề phát triền server các ứng dụng không cần trực tiếp thu thâp vào  log server, từng ứng dụng 
 Thường để xây dựng nên trung tâm này dùng đến ELK với các thành phần chính gồm:
 
 ![image](https://user-images.githubusercontent.com/105496635/186821824-348f55a8-9337-4850-b6e0-763fcc5b755d.png)

           Elasticsearch: máy chủ lưu trữ và tìm kiếm dữ liệu
           Logstash: thành phần xử lí dữ liệu, sau đó nó gửi Elsticsearch về để lưu
           Kibana: ứng dụng nền web và xem trực quan các log
           Beats: gửi dữ liệu từ máy lưu từ Logdtash
           
## 9. Cơ chế hoạt động của ELK stack

![image](https://user-images.githubusercontent.com/105496635/186822669-11dbe396-6fb2-4343-ada8-1734f449dc65.png)

- Đầu tiên, log sẽ được đưa đến Logstash. (Thông qua nhiều con đường, ví dụ như server gửi UDP request chứa log tới URL của Logstash, hoặc Beat đọc file log và gửi lên Logstash)

- Logstash sẽ đọc những log này, thêm những thông tin như thời gian, IP, parse dữ liệu từ log (server nào, độ nghiêm trọng, nội dung log) ra, sau đó ghi xuống database là Elasticsearch.

- Khi muốn xem log, người dùng vào URL của Kibana. Kibana sẽ đọc thông tin log trong Elasticsearch, hiển thị lên giao diện cho người dùng query và xử lý.


## 10. Hướng dẫn triển khai hệ thống đơn giản
  Cần tài nguyên gì để triển khai hệ thống để triển khai hệ thống ELK
  - Đây là một trong những câu hỏi mà một quản trị hệ thống cần quan tâm. Một trong những ưu điểm của ELK là các bạn có thể bắt đầu rất nhỏ, chỉ với một server (physical hoặc virtual), và có thể mở rộng tùy theo nhu cầu (scale up và scale out). Tuy nhiên, vì đây là phần mềm miễn phí (về cơ bản) và bản chất của Elasticsearch là search engine, không phải là SIEM, nên để xây dựng được hệ thống theo dõi log cho Production thì người quản trị cần phải đầu tư thời gian (đồng nghĩa với tiền bạc).

- Nhân lực: thường thì chỉ cần 1 người là gánh đủ ELK. Ban đầu thì sẽ mất thời gian tìm hiểu để triển khai và tinh chỉnh, sau khi ổn định thì chỉ cần phân tích thông tin và xử lý.
- Tài nguyên hệ thống: ở mức nhỏ nhất, các bạn có thể triển khai server ở mức nhỏ nhất với CPU từ 2-4, 8 GB, 30 gb free HDD. Yêu cầu tài nguyên với tỉ lệ như sau:
   - Lưu lượng log thu thập 
   - Yêu cầu về tốc độ xuất Eláticsearch 
   - Yêu cầu về tốc độ tìm kiếm (keyword vs. full text search vs. custom full text search)
   -Yêu cầu về Đeundacy(number of replicas)
   - Nhìn chung  là không có công thức nào để tính tài nguyên mỗi nhu cầu sử dụng tài nguyên khác nhau

## 11. Mô hình theo dõi log
- Cơ bản nhất là dùng beats thu thập log và máy tính  và gửi thẳng về Log Stack để xử lí thu thập. Ngoài ra , nếu sử dụng nxlog bản Enterprise có thể gửi thẳng log vào ES (chắc có thể dùng Ingest pipeline để xử lý), tuy nhiên thường thì chúng ta dùng Logstash để normalize và enrich log events. 
  
- Với hệ thống mạng có nhiều lớp mạng riêng biệt, nếu để beats gửi log trực tiếp đến Logstack thì phải tạo ra Log stack đến tất cả các máy log stack TCP port chúng ta có thể điều này có thê xảy ra khi thêm vào các nxlog vào các lớp
- Trên mỗi nxlog tập trung mình có thể sử dụng disk buffer để queue trong trường hợp nxlog không thể kết nối tới Logstack










