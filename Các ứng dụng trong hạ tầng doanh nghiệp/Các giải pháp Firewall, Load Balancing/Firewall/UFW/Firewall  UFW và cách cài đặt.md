## 1. Khái niệm
- Để cấu hình tường lưa trên Linux tiện lợi và hiệu quả hơn, bạn ta nên chuyển qua sử dụng UFW (Uncomplicated Firewall) do Canonical (công ty làm ra điều hành Ubuntu) phát triển. UFW không phải là một ứng dụng tường lừa thay thế iptables, nó chỉ giao diện dòng lệnh của iptablesvới các câu lệnh ngắn gọn, dễ nhớ hơn.

## 2. Cài đặt

- Bạn chỉ nên cài đặt UFW trên hệ thống Linux mới, chưa cài đặt bất cứ control panel, script quản lý nào như cPanel, aaPanel, CyberPanel, Centminmod,… Vì các loại control panel này luôn cài đặt sẵn các tiện ích tường lửa đi kèm. Cài đặt thêm UFW sẽ gây xung đột hệ thống.

Bước 1: Cập nhật hệ thống trước khi cài đặt

       sudo yum update
     
Bước 2: Cài đặt repo, từ đó chúng ta có thể cài đặt UFW.epel-release

            `sudo yum install epel-release`

![image](https://user-images.githubusercontent.com/105496635/188363448-6d9f83b8-4bdc-4232-9257-900292c96607.png)


Bước 3. Cài đặt UFW.

       `yum install --enablerepo="epel" ufw`

![image](https://user-images.githubusercontent.com/105496635/188363675-92aff5ac-c667-49d2-be27-693a723536c6.png)


Bước 4. Xác minh cài đặt và kiểm tra phiên bản với:

        `ufw --version`


![image](https://user-images.githubusercontent.com/105496635/188363801-793b33b9-0950-458d-857d-3126e91181ce.png)



Bước 5. Sau khi cài đặt xong, hãy kích hoạt nó.

`sudo ufw enable`

![image](https://user-images.githubusercontent.com/105496635/188364379-e3f1e680-4aa3-4708-8b60-2c475afcc25d.png)


Bước 6. Để kiểm tra trạng thái, hãy chạy:

`sudo ufw status`

