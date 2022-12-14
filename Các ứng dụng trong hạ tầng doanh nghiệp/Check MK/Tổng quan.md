# 1. OMD, Check mật khẩu là gì

![image](https://user-images.githubusercontent.com/105496635/189607147-b4a6ec21-cd96-43ec-acb7-359c3ff98455.png)

- OMD - Open Monitoring Distribution là một dự án được phát triển từ năm 2010 bới Mathias Kettner. OMD sử dụng nhân là Nagios Core, kết hợp với các phần mềm mã nguồn mở khác để đóng gói thành một sản phẩm phục vụ cho nhu cầu giám sát, cảnh báo và hiển thị.

- Dự án Check_MK được phát triển từ năm 2008 như là một plugin của Nagios Core.

- Năm 2010 dự án OMD (Open Monitoring Distribution) được khởi động bởi Mathias Kettner, là sự kết hợp của Nagios, Check_MK, NagVis, PNP4Nagios, DocuWiki, …tạo nên sự linh hoạt trong giám sát. Các distro của OMD đang là OMD-LABS và CHECK_MK RAW.

- Check_MK là một phần của OMD, hiện tại đang có 2 phiên bản Check_MK là Check_MK Raw Edition (CRE) và Check_MK Enterprise Edition (CEE)


# 2. Ưu điểm trong thiết kế kiến trúc của OMD.
- OMD được xây dựng từ những đóng góp của cộng đồng về những khó khăn hay khuyết điểm mà Nagios gặp phải, từ đó quyết định ra quyết định cần tích hợp thêm những sản phẩm cần cải thiện
- Việc cài đặt trở lại vô cùng đơn giản. OMD được đóng gói hoàn chỉnh trong 1 pakage, việc cài đặt hay cầu hình chỉ mất khoảng 10p với một câu lệnh



![image](https://user-images.githubusercontent.com/105496635/189609020-732b3c6b-d73a-4b8e-ae30-b2d237c8b17b.png)


Check_MK ra đời để giải quyết bài toán về hiệu năng mà Nagios gặp phải trong quá khứ.Cơ chế mới của Check_MK cho phép việc mở rộng hệ thống trở nên dễ dàng hơn, có thể giám sát nhiều hệ thống chỉ từ một máy chủ Nagios server.

Có 2 mô đun mà Check_MK sử dụng để cải thiện đáng kể hiệu năng là Livestatus và Livecheck.

Livestatus có những thay đổi để cải thiện hiệu năng đó là:

Livestatus cũng sử dụng Nagios Event Broker API như NDO, nhưng nó sẽ không chủ động ghi dữ liệu ra. Thay vào đó, nó sẽ mở ra một socket để dữ liệu có thể được lấy ra theo yêu cầu.

Livestatus tiêu tốn ít CPU.

Livestatus không làm cho Disk I/O thay đổi khi truy vấn trạng thái dữ liệu.

Không cần cấu hình. Không cần cơ sở dữ liệu. Không cần quản lý.

Livecheck hoạt động như thế nào để cải thiện được hiệu năng :
Livecheck sử dụng các helper process, các core giao tiếp với helper thông qua Unix socket (điều này không xảy ra trên file system).

Chỉ có một một helper program được fork thay vì toàn bộ Nagios Core.

Các tiến trình fork được phân tán trên tất cả các CPU thay vì chỉ một như trước.

Process VM size tổng chỉ khoảng 100KB. 












































































