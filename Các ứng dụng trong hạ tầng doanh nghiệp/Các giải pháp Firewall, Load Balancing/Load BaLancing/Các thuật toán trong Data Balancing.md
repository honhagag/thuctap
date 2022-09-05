# Thuật toán trong Data Balacing
![image](https://user-images.githubusercontent.com/105496635/188412578-5a21634a-fd80-432b-9212-6e99a0ac56dd.png)

Tùy thuộc công nghệ Load Balancing mà các thuật toán khác nhau sẽ được siwr dụng để đimh tình trạng của máy chủ có hoạt động hay không. Các loại thuật toán thường thấy là
- Round Robin
- Weighted Round Robin
- Dynamic Round Robin
- Fastest
- Least Connections

||Round Robin|Weighted Round Robin|Dynamic Round Robin|Fastest|Fastest|
|-|-|-|-|-|-|
|Khái niệm|Round Robin là thuật toán lựa chọn các máy chủ theo trình tự. Theo đó, Load Balancer sẽ bắt đầu đi từ máy chủ số 1 trong danh sách của nó ứng với yêu cầu đầu tiên. Tiếp đó, nó sẽ di chuyển dần xuống trong danh sách theo thứ tự và bắt đầu lại ở đầu trang khi đến máy chủ cuối cùng.|Tương tự như kỹ thuật Round Robin nhưng WRR còn có khả năng xử lý theo cấu hình của từng server đích. Mỗi máy chủ được đánh giá bằng một số nguyên (giá trị trọng số Weight – mặc định giá trị là 1). Một server có khả năng xử lý gấp đôi server khác sẽ được đánh số lớn hơn và nhận được số request gấp đôi từ bộ cân bằng tải.|Thuật toán DRR hoạt động gần giống với thuật toán WRR. Điểm khác biệt là trọng số ở đây dựa trên sự kiểm tra server một cách liên tục. Do đó trọng số liên tục thay đổi.Việc chọn server sẽ dựa trên rất nhiều khía cạnh trong việc phân tích hiệu năng của server trên thời gia thực. Ví dụ: số kết nối hiện đang có trên các server hoặc server trả lời nhanh nhất, …|Đây là thuật toán dựa trên tính toán thời gian đáp ứng của mỗi server (response time). Thuật toán này sẽ chọn server nào có thời gian đáp ứng nhanh nhất. Thời gian đáp ứng được xác định bởi khoảng thời gian giữa thời điểm gửi một gói tin đến server và thời điểm nhận được gói tin trả lời.Việc gửi và nhận này sẽ được bộ cân bằng tải đảm nhiệm. Dựa trên thời gian đáp ứng, bộ cân bằng tải sẽ biết chuyển yêu cầu tiếp theo đến server nào.Thuật toán Fastest thường được dùng khi các server ở các vị trí địa lý khác nhau. Như vậy người dùng ở gần server nào thì thời gian đáp ứng của server đó sẽ nhanh nhất. Cuối cùng server đó sẽ được chọn để phục vụ.|Các request sẽ được chuyển vào server có ít kết nối nhất trong hệ thống. Thuật toán này được coi như thuật toán động, vì nó phải đếm số kết nối đang hoạt động của server. Least Connections có khả năng hoạt động tốt. Ngay cả khi tải của các kết nối biến thiên trong một khoảng lớn. Do đó nếu sử dụng RC sẽ khắc phục được nhược điểm của Round Robin.
|Nhược điểm|Khi có 2 yêu cầu liên tục từ phía người dùng sẽ có thể được gửi vào 2 server khác nhau. Điều này làm tốn thời gian tạo thêm kết nối với server thứ 2 trong khi đó server thứ nhất cũng có thể trả lời được thông tin mà người dùng đang cần. Để giải quyết điều này, round robin thường được cài đặt cùng với các phương pháp duy trì session như sử dụng cookie.|Weighted Round Robin gây mất cân bằng tải động nếu như tải của các request liên tục thay đổi trong một khoảng thời gian rộng|Thuật toán này thường không được cài đặt trong các bộ cân bằng tài đơn giản. Nó thường được sử dụng trong các sản phẩm cân bằng tải của F5 Network.|||








