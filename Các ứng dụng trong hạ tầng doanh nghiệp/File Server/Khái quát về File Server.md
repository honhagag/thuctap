# File Server
## 1. File Server là gì
- File server là một máy tính nối mạng cung cấp không gian để lưu trữ và chia sẻ dữ liệu như văn bản , hình ảnh, âm thanh, video. Các dữu liệu này có thể truy cập với các worktation. Worktation này có thể kết nối tới máy chủ  khi các máy này chia sẻ quyền truy cập thông qua mạng máy tính

![image](https://user-images.githubusercontent.com/105496635/187577700-8f314ef2-8d0e-45b6-9974-a1789fa3213f.png)

Trong lược đồ máy khách - máy chủ (client - server), các máy khách chính là các máy trạm sử dụng stogare. Thông thường, một file server sẽ không hiện các nhiệm vụ máy tính và cũng không chạy các chương trình client. Khi cấu hình máy chủ Filr server chủ yếu chỉ thiết lập cho dữ liệu trong khi nhiệm vụ được tính toán được thực hiện bới các workstation 

## 2. Phân loại các kiểu File Server
Một file server có thể là máy chủ chuyên dụng hoặc không chuyên dụng. Một máy chuên dụng sẽ được thiết kế đặc biệt để sử dijng như một mail  server đến với các máy chủ server vơi các máy trạm được kêt nối để đọc, ghi các tập tin và cơ sở dữ liệu

File server cũng được phân thoai loại phương thức truy cập
 
- FPT: File Transfer Protocol 
- HTTP: Hypertext Tranfer Protocpl
- SMB: Server Mesage Block/ CIFC - Common In File Syste - Window hoặc UNIX mà thường cho UNIX
- NFS: Network File System – Chủ yếu là cho UNIX, hệ thống tương tự UNIX
- Database servers, cung cấp quyền truy cập vào shared database vì chúng có thể êu cầu Recorrd looking

## 3. Cấu trúc của File Server
- Storage 
Vì chức năng quan trọng nhất trong file server là storage, nên hiện nay đã có các công nghệ được phát triển cho phép vận hành nhiều ổ đĩa theo nhóm, hình thành một disk array. 1 disk array điển hình sẽ chứa cache (bộ nhớ tạm thời có tốc độ nhanh hơn magnetic disk), cũng như các chức năng tiên tiến hơn như RAID hay ảo hóa lưu trữ. Bên cạnh đó, disk array cũng giúp nâng cao độ sẵn sàng nhờ các yếu tố dự phòng khác ngoài RAID như nguồn điện. Các disk array có thể được hợp nhất hoặc ảo hóa trong môi trường SAN.

- Netword-attached stoge
Netword-attached stoge là máy tính lưu trữ dữ liệu cấp độ tập tin được kết nối với mạng máy tính cho phép truy cập dữ liệu trên một nhóm máy khach không đồng nhất. NAS device - thiết bị lưu trữ gắn vào mạng (phân biệt với mạng NAS) là một thiết bị/ máy tính chuyên dùng chỉ dùng đê server các tập tin thay vì dùng cho các ,mục đích chung

![image](https://user-images.githubusercontent.com/105496635/187582788-d6987092-2b6d-4e44-bd2f-9c0c3e2f9d5f.png)

Cho đến năng 2001, các thiết bị NAS đã dần trở nên phổ biến nhờ mang đến phương thức tiện lợ đê chia sẻ tệp giữa nhiều máy tính. Lợi ích của NAS so với các file server không chuyên dụng, bao gồm các tính năng như truy cập dữ liệu nhanh hơn, quản trị dễ dàng hơn và cấu hình đơn giản hơn.

Hệ thống NAS là các thiết bị nối mạng với 1 hay nhiều ổ cứng, thường được sắp xếp thành các storage container dự phòng hoặc các RAID array. Network Attached Storage loại bỏ việc phân phát tệp từ các máy chủ khác trên mạng. NAS thường cấp quyền truy cập files sử dụng các giao thức chia sẻ file qua mạng như NFS, SMB/CIFS (Server Message Block/Common Internet File System) hoặc AFP.


## 4. Bảo mật

Việc xây dựng hẹ thống FIle server thường hỗ trợ một vài hình thức bảo mật hệ thống nhằm hạn chế quyền truy cập đối với người dùng hoặc nhóm người dùng cụ thể 

Trong các tổ chức lớn, nhiệm vụ thường được phân cấp cho cáác directory service như openLDAP, eDirectory của Novell hoặc Active Directory của Microsoft.

Các server này hoạt động trong môi trường máy tính phân tầng; xử lý user, máy tính, ứng dụng và file như các thành phần riêng biệt nhưng có liên quan đến nhau trên mạng; cấp quyền truy cập thông qua xác thực người dùng hoặc nhóm người dùng.

Như vậy, chúng ta đã nắm được các thông tin tổng quan và cơ bản về hệ thống File server. Ngoài File server, còn có rất nhiều các hình thức lưu trữ khác, bạn có thể tìm hiểu trong các bài viết cùng chuyên mục.

























