# Các lỗ hỏng trong Zimbra
## 1. Lỗ hỏng bảo mật trong Mail Server Zimbra
1.1 Lỗ hỏng đầu tiền có đoạn mã là CVE-2021-35208:
- Cross-Site Scripting (Lỗ hỏng XSS nằm trong ZmMailMsgView.java). Khi người dùng mở mail trên trình duyệt web, họ có thể kích thích đoạn mã JavaScript, cho phép hacker truy cập và sử dụng như người dùng
- Lỗ hỏng XSS thường xuất hiện phổ biến ở các thành phần bảo mật, do máy khash có nhiều font-end cho web , di động và nhiều các loại hệ điều hành khác nhau. Hacker sẽ thường xuyên khai thác lỗ hỏng trên XSS để có thể truy cập quyền như người dùng
1.2 Lỗ hỏng thứ có mã là CVE-2021-35209:
- Hacker có khả năng xâm lược vào các Server-Side Request Forgery (SSRF) của hệ thống. Lỗ hỏng SSFR có thể giúp hacker có quyền truy cập các quyền như: truy cập vào mạng nội bộ như cơ sở dữ liệu, trang quản trị và các dịch vụ yêu cầu khác
- Các lỗ hỏng SSFR ngày càng được các hacker truy cập hệ thống doanh nghiệp
- Nếu 2 lỗ hòng này cùng một lúc các hacker sẽ trick xuất được Google API hoặc chứng chỉ AWS IAM
- Các nhà nghiên cứu đã chưng minh được  2 lỗ hỏng XSS và SSFR cùng một lúc sẽ nguy hiểm hơn, vì thế Zimbra phải nâng cao bảo mật nhiều hơn

## 2. Giải pháp bảo mật cho Zimbra

Một doanh nghiệp lớn hay nhỏ đều có những thông tin quan trọng và ít nhiều của tổ chức. Nên có các phương pháp sau
1. Xác minh và mã hóa Email quan trọng
- Việc mã hóa nội dung email là bước quan trọng để không bị đánh cấp dữ liệu
2. Lưu ý lựa chọn dịch vụ web mail
- Hãy trang bị tường lửa để email cho doanh nghiệp để đảm bảo đã được bảo mật SSL
3. Giáo dục nhân viên để sử dụng mail an toàn
Con người là yêu tố dẫn đến mọi tấn công. Hacker đã biết khơi gợi các nhân để đưa ra các chiêu thức lừa đảo, mời gợi mọi người 
4. Sử dụng công cụ lọc mail
5. Chọn tường lửa lựa chọn mail thông minh
