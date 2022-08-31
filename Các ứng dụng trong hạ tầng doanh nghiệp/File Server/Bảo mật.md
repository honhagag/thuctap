# Bảo mật
 
 Để cấu hình bảo mật cho FTP Server thêm an toàn, bạn thêm vào 2 dòng bên dưới. Đây là cách chroot FPT rất cần thiết với máy chủ có nhiều user. Mục đích là đảm bảo mỗi user được tạo ra sẽ bị giới hạn truy cập trong Home Directory của nó, không thể view hoặc access vào bất kỳ thư mục nào.

        chroot_local_user=YES # kích hoạt tính năng chroot cho local user.
        allow_writeable_chroot=YES # Phải có dòng này chroot mới hoạt động chuẩn được nhé.

Tiếp theo là userlist_enable. Nếu được gán giá trị YES thì tất cả các user được liệt kê trong file /etc/vsftpd/user_list sẽ không thể access vào FTP Server được. Tất cả các user trong user_list đều là những tài khoản quan trọng dùng để vận hành máy chủ, tốt nhất là không dùng cho FTP thì hơn. Nếu giá trị là NO thì ngược lại, toàn bộ những user trong user_list sẽ truy cập được FTP Server.

Mình chọn YES

      userlist_enable=YES




Khi chroot user đồng nghĩa với việc user không thể truy cập được đâu ngoài thư mục của mình. Nhưng trong quá trình sử dụng, nhiều khi bạn muốn tạo ra một ngoại lệ (exception) để một user nào đó có thể đi vào tất cả các thư mục xem một tí thì phải làm thế nào?

Để làm được điều đó, bạn thêm vào 2 dòng bên dưới.

         chroot_list_enable=YES # Dòng này vô hiệu hóa Chroot.

       chroot_list_file=/etc/vsftpd/chroot_list # Dòng này tạo ra một file chứa danh sách    các local user không bị giới hạn bởi chroot.




# Tạo tài khoản FTP

Khi cấu hình và bảo mật FTP đã sẵn sàng, để linh hoạt khi sử dụng FTP trên Linux, bạn bắt đầu tạo user FTP.

Theo mặc định Local User được tạo ra trên Linux có Home Directory là /home/user. Tất cả dữ liệu user upload/download đều nằm trong thư mục /home/user cả.

Nhưng nếu bạn không muốn dùng mặc định, muốn gom tất cả vào đường dẫn /var/ftp/user thì phải làm thế nào?


Bước 1 – Tạo Home Directory

Ví dụ mình sẽ tạo user1 có home directory là /var/ftp/user1, chạy lệnh:

       mkdir /var/ftp/user1
Bước 2 – Tạo user

useradd -d /var/ftp/user1 -s /sbin/nologin user1
Ý nghĩa thông số:

        -d: Thay đổi Home Directory sang /var/ftp/user1, nếu không user tạo ra sẽ dùng có Home Directory mặc định là /home/user1.

       -s: Tạo Shell cho user1 không cho login vào server. Bạn nên dùng shell nologin thay cho /bin/bash, /bin/sh.

Chú ý: nếu một user2 được tạo ra trước đó sử dụng Home Directory mặc định, bạn có thể thay đổi bằng lệnh sau:

         usermod -d /var/ftp/user2
Bước 3 – Thay đổi quyền sở hữu Home Directory

Thư mục tạo ra mặc định root:root quản lý, bạn phải chown lại cho thư mục.

        chown user1:user1 -R /var/ftp/user1








































