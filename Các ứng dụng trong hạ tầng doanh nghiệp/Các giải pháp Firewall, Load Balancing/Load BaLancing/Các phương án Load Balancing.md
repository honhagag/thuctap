## Cách Load Balancing xử lý trạng thái là gì

![image](https://user-images.githubusercontent.com/105496635/188420968-adfdeaef-2155-43f7-829f-63dfdf1dc75f.png)

Trong nhiều trường hợp ứng dụng yêu cầu người truy cập tiếp tụ keeys nối đến một backend server. Một thuật toán mã ngườn sẽ tạo ra một mối quan hệ dựa trên thông tin là IP khách hàng. Đối với ứng dụng web thông qua sticky session hướng đến một máy chủ vật lý


## Load Balancer dự phòng là gì


![image](https://user-images.githubusercontent.com/105496635/188421673-a1d40726-b750-45c8-9bc9-4396c54aa3dc.png)

Trong nhiều truoefng hợp, chỉ có một Load Balancer là điểm truy caoah duy nhất. CHính vì vậy, chúng ra cần có một Load Balancer thứ hau. Nó sẽ được kết nối với Load Balancer ban đầu. Mục địch để mỗi Load Balancer đều có khả năng phát hiện lỗi và phục hồi

Sẽ ra sao khi xáy ra trường hợp Load Balancer chính bị lỗi? Balancer thứ hai sẽ nhận trách nhiệm thay thế, do DNS di chuyển người dùng đến. Tuy nhiên, việc thay đổi DNS có thể mất nhiều thời gian đến Internet. Và để chuyển đổi dụ phòng được tự động , các quản trị viên sẽ cho phép linh hoạt địa chỉ IP Remappping. Chẳng hạn nhưu trường hợp này là Floating ÍP
IP Remapping giúp loại bỏ các vấn đề bộ nhớ đệm vốn có trong những thay đổi DNS. IP Rempping sẽ cũng cấp một địa chỉ IP tĩnh. Địa chỉ này có thể được dễ dàn ánh xạ khi cần thiết. Tên miền có thể duy trì liên kết với các địa chỉ IP. Trong khi các địa chỉ IP cúa chính nó được di chuyern giữa các máy chủ













