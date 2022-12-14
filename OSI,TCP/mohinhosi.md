# Tìm hiểu  về mô hình OSI

I,Mô hình OSI
-Mô hình OSI (Open Systems Interconnection Reference Model, viết ngắn là OSI Model hoặc OSI Reference 
Model) – tạm dịch là mô hình tham chiếu kết nối các hệ thống mở hay còn được gọi là mô hình bảy tầng của 
OSI. Mô hình OSI mô tả bảy tầng mà hệ thống máy tính sử dụng để giao tiếp qua mạng. Đây là mô hình tiêu 
chuẩn đầu tiên cho truyền thông mạng, được tất cả các công ty máy tính và viễn thông lớn áp dụng vào đầu 
những năm 1980.

-Mô hình OSI tuân theo các nguyên tắc phân tầng như sau:

Mô hình gồm N = 7 tầng. OSI là hệ thống mở, phải có khả năng kết nối với các hệ thống khác nhau, tương thích với các chuẩn OSI.
    Gồm: + Application Protocol
         + Presentation Protocol
         + Sesion Protocol
         + Transport Protocol
         + Netword Protocol
         + Datalink Protocol
         + Physical Protocol





 +Quá trình xử lý các ứng dụng được thực hiện trong các hệ thống mở, trong khi vẫn duy trì được các hoạt động kết nối giữa các hệ thống.

 +Thiết lập kênh logic nhằm mục đích thực hiện việc trao đổi thông tin giữa các thực thể.


-Các giao thức trong mô hình OSI
Trong mô hình OSI có hai loại giao thức được sử dụng: giao thức hướng liên kết (Connection – Oriented) và giao thức không liên kết (Connectionless).

  +Giao thức hướng liên kết
Trước khi truyền dữ liệu, các thực thể đồng tầng trong hai hệ thống cần phải thiết lập một liên kết logic. Chúng thương lượng với nhau về tập các tham số sẽ sử dụng trong giai đoạn truyền dữ liệu, cắt/hợp dữ liệu, liên kết sẽ được hủy bỏ. Thiết lập liên kết logic sẽ nâng cao độ tin cậy và an toàn trong quá trình trao đổi dữ liệu.

  +Giao thức không liên kết
Dữ liệu được truyền độc lập trên các tuyến khác nhau. Với các giao thức không liên kết chỉ có giai đoạn duy nhất truyền dữ liệu.
-Vai trò và chức năng chủ yếu các tầng.
Vai trò và chức năng tầng ứng dụng (Application Layer)
Nhiệm vụ của tầng này là xác định giao diện giữa người sử dụng và môi trường OSI. Bao gồm nhiều giao thức ứng dụng cung cấp các phương diện cho người sử dụng truy cập vào môi trường mạng và cung cấp các dịch vụ phân tán. Khi các thực thể ứng dụng AE (Application Entity) được thiết lập, nó sẽ gọi đến các phần tử dịch vụ ứng dụng ASE (Application Service Element). Mỗi thực thể ứng dụng có thể gồm một hoặc nhiều các phần tử dịch vụ ứng dụng. Các phần tử dịch vụ ứng dụng được phối hợp trong môi trường của thực thể ứng dụng thông qua các liên kết gọi là đối tượng liên kết đơn SAO (Single Association Object). SAO điều khiển việc truyền thông và cho phép tuần tự hóa các sự kiện truyền thông.
