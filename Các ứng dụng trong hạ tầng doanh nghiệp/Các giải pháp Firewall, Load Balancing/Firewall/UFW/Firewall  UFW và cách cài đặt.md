## 1. Khái niệm
- Để cấu hình tường lưa trên Linux tiện lợi và hiệu quả hơn, bạn ta nên chuyển qua sử dụng UFW (Uncomplicated Firewall) do Canonical (công ty làm ra điều hành Ubuntu) phát triển. UFW không phải là một ứng dụng tường lừa thay thế iptables, nó chỉ giao diện dòng lệnh của iptablesvới các câu lệnh ngắn gọn, dễ nhớ hơn.

## 2. Cài đặt

- Bạn chỉ nên cài đặt UFW trên hệ thống Linux mới, chưa cài đặt bất cứ control panel, script quản lý nào như cPanel, aaPanel, CyberPanel, Centminmod,… Vì các loại control panel này luôn cài đặt sẵn các tiện ích tường lửa đi kèm. Cài đặt thêm UFW sẽ gây xung đột hệ thống.

- Cập nhật hệ thống trước khi cài đặt

       sudo apt update
       sudo apt upgrade -y





