# 1. Tổng  quan
- Zabbix là một công cụ giám sát hệ thống mạng , các thiết bị mạng, giám át khả năng sẵn sàng và hiệu năng của mjang và thiết bị mjang. Nếu có xảy ea lỗi thì sẽ có cảnh báo gửi tới người quản trị mạng sms, email..
- Là công cụ mã nguồn mở miễn phí.
- Được phát hành giấy phép GPlv2, không giới hjan về sức chứa và số lượng thiết bị được giám sát
- Hỗ trợ bất kỳ kích thước của mô hình nào. Có thể là mô hình nhỏ hoặc mô hình lớn, thường xuyên cập nhật và phát hành phiên bản mới
- Zabbix được viết năm 1198, là dự án của Alexei Vladishev (Alexei Vladishev dùng để monnitoe hệ thống database)

2. Zabbix Features

- Zabbix cũng caaos những tính năng quan trọng và cần thiết cho việc monitor hệ thống và các thiết bị mạng
- Zabbic dụa trên các agent và agentless để giám sát hệ thống mạng và các thiết bị mạng. Các thiết bị mạng phải hỗ trijw giao thức SNMP. Zabbix không có khả năng phát hiện hay dự đoán lỗi có thể xảy ra.
- Trong trường hợp có thể xảy ra zabbix cảnh báo cho người quản trị, tuy  nhiên zabbix không có khả năng phát hiện lỗi xảy ra

2.2 Agent- based với Agentless
- Agent - based

Đây là một phần mềm được gọi là ahent được cài đặt trên máy chỉ local và cá thiết bị cần momitor. Mục tiêu của nó là thu thập thông tin gửi về zabbix- server và có thể cảnh báo tới người quản trị

Agent được cài đặt đơn giản nhẹ nhàng, tiêu thụ ít tài nguyên của server

