# Phân biệt giao thức TCP và UDP
1, Khái niệm UDP và TCP:
- UDP (User Datagram Protocol) là một trong những giao thức cốt lõi của giao thức TCP/IP. Dùng UDP, chương trình trên mạng máy tính có thể gởi những dữ liệu ngắn được gọi là datagram tới máy khác. UDP không cung cấp sự tin cậy và thứ tự truyền nhận mà TCP làm; các gói dữ liệu có thể đến không đúng thứ tự hoặc bị mất mà không có thông báo.Tuy nhiên UDP nhanh và hiệu quả hơn đối với các mục tiêu như kích thước nhỏ và yêu cầu khắt khe về thời gian. Do bản chất không trạng thái của nó nên nó hữu dụng đối với việc trả lời các truy vấn nhỏ với số lượng lớn người yêu cầu.

- TCP (Transmission Control Protocol – “Giao thức điều khiển truyền vận”) là một trong các giao thức cốt lõi của bộ giao thức TCP/IP. Sử dụng TCP, các ứng dụng trên các máy chủ được nối mạng có thể tạo các “kết nối” với nhau, mà qua đó chúng có thể trao đổi dữ liệu hoặc các gói tin. Giao thức này đảm bảo chuyển giao dữ liệu tới nơi nhận một cách đáng tin cậy và đúng thứ tự. TCP còn phân biệt giữa dữ liệu của nhiều ứng dụng (chẳng hạn, dịch vụ Web và dịch vụ thư điện tử) đồng thời chạy trên cùng một máy chủ.
2, Phân biệt

So sánh một cách đơn giản :

Giống nhau : đều là các giao thức mạng TCP/IP, đều có chức năng kết nối các máy lại với nhau, và có thể gửi dữ liệu cho nhau….

Khác nhau (cơ bản): 
các header của TCP và UDP khác nhau ở kích thước (20 và 8 byte) nguyên nhân chủ yếu là do TCP phải hộ trợ nhiều chức năng hữu ích hơn(như khả năng khôi phục lỗi). UDP dùng ít byte hơn cho phần header và yêu cầu xử lý từ host ít hơn
TCP :
– Dùng cho mạng WAN
– Không cho phép mất gói tin
– Đảm bảo việc truyền dữ liệu
– Tốc độ truyền thấp hơn UDP
UDP:
– Dùng cho mạng LAN
– Cho phép mất dữ liệu
– Không đảm bảo.
– Tốc độ truyền cao, VolP truyền tốt qua UDP

TCP hoạt động theo hướng kết nối (connection-oriented), trước khi truyền dữ liệu giữa 2 máy, nó thiết lập một kết nối giữa 2 máy theo phương thức “bắt tay 3 bước (three-way-hand-shake)” bằng cách gửi gói tin ACK từ máy đích sang máy nhận, trong suốt quá trình truyền gói tin, máy gửi yêu cầu máy đích xác nhận đã nhận đủ các gói tin đã gửi, nếu có gói tin bị mất, máy đích sẽ yêu cầu máy gửi gửi lại, thường xuyên kiểm tra gói tin có bị lỗi hay ko, ngoài ra còn cho phép qui định số lượng gói tin được gửi trong một lần gửi (window-sizing), điều này đảm bảo máy nhận nhận được đầy đủ các gói tin mà máy gửi gửi đi –> truyền dữ liệu chậm hơn UDP nhưng đáng tin cậy hơn UDP

UDP hoạt động theo hướng ko kết nối (connectionless), ko y/c thiết lập kết nối giữa 2 máy gửi và nhận, ko có sự đảm bảo gói tin khi truyền đi cũng như ko thông báo về việc mất gói tin, ko kiểm tra lỗi của gói tin
–> truyền dữ liệu nhanh hơn UDP do cơ chế hoạt động có phần đơn giản hơn tuy nhiên lại ko đáng tin cậy bằng TCP

TCP và UDP là 02 Protocol hoạt động ở lớp thứ 04 (Transport Layer) của mô hình OSI và ở lớp thứ 02 (Transport Layer) mô hình TCP/IP (xin lưu ý: mô hình TCP/IP (TCP/IP Model ) khác hoàn toàn với chồng giao thức TCP/IP (TCP/IP Suite)

TCP là giao thức truyền tin cậy và phải bắt tay ba bước (three-way-hand-shake) nên khi Server không nhận được bất kỳ gói tin ACK từ Client gửi trả lời thì Server sẽ gửi lại gói tin đã thất lạc. Server sẽ gửi cho đến khi nhận được ACK của Client mới thôi => Điều này cũng là một nhân tố làm chậm và ngốn băng thông đường truyền.

Ý chủ bài viết muốn nói lên TCP dành cho các ứng dụng secure. đối với các ứng dụng không cần secure thì dùng UDP là được, lợi hơn về performance. finding DC thì không cần secure, LDAP tất nhiên cần secure.

Mặc dù tổng lượng lưu thông của UDP trên mạng thường chỉ vài phần trăm, nhưng có nhiều ứng dụng quan trọng dùng UDP, bao gồm DNS, SNMP, DHCP và RIP, dễ thấy hơn là điện thoại IP, xem truyền hình trực tiếp…Thực tế UDP dùng nhiều cho việc truyền tải Games Online. Như các bạn biết đó…việc nâng cấp sửa lỗi games các nhà quản trị Games và Bảo mật thường xuyên cập nhật bản vá lỗi của games, hoặc các thông tin dẫn truyền trong games đều dùng UDP rất nhiều. Nói TCP bảo mật hơn thì cũng đúng, nhưng UDP cũng rất bảo mật điều này phụ thuộc vào mức độ mã hóa của các Package trong liên kết truyền thông. Nghiên cứu thêm trong An Toàn Bảo Mật Thông Tin…

Để biết máy tính có dùng UDP hay TCP thi bạn có thể thao khảo Sys Tools…những công cụ kiểm tra hệ thống và xem trên Router, check Port Connection….(Tất cả nằm trên anh Google…)

“Tiền nào của nấy”. Sử dụng TCP có rất nhiều ưu điểm, nhưng ngược lại chi phí đắt.  Khi mà ứng dụng không yêu cầu quá cao về chất lượng, có thể chấp nhận việc mất thông tin và trễ về thời gian (như điện thoại internet, media…) thì việc sử dụng UDP thay vì TCP sẽ tiết kiệm được nhiều chi phí.

– Ngoài ra:

+ UDP có độ trễ nhỏ, do không có giai đoạn thiết lập đường truyền

+ UDP nó đơn giản: Phía gửi và phía nhận không phải ghi nhớ trạng thái gửi/nhận.

+ small segment header

+ Không có cơ chế kiểm soát tắc nghẽn, do đó bên gửi có thể gửi dữ liệu với tốc độ tối đa

Các bạn có thể thấy UDP được sd nhiều trong : NTP, DNS, MDNS, BOOTP, DHCP, SysLog, NFS, ISAKMP, Cisco HSRP, Cisco MGCP,…

Hai ứng dụng phổ biến là Yahoo Messenger sử dụng TCP/IP và Skype sử dụng UDP.



Tham khảo: https://kysudien.wordpress.com/2014/03/13/so-sanh-2-giao-thuc-tcp-va-udp/
