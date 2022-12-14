# Zimbra 
## Tổng quan
### 1. Zimbra Mail Server là gì
- Zimbra Mail Server là phần mềm mã nguồn mở hỗ trợ người dùng ở hai chế độ máy chủ Mail và máy chủ Website và được phát triển với ngoài mục đích người tiêu dùng Mail thì là giải pháp của nhiều vấn đề bảo mật, kết nối các thành viên chat, phân chia quản lí công việc và chia sẻ công việc một cách nhanh chống hiệu quả cho doanh nghiệp lớn nhỏ
### 2. Chức năng của Zimbra mail
Các chức năng trên zimbra mail:

- Thư điện tử: Hệ thống thư điện tử hoàn hảo, Với hai phần là Mail Server (SMTP, POP3, IMAP, Backup, Antivirus… Bên cạnh đó có đủ các tính năng như: tự động trả lời, chuyển tiếp…) và Mail Client (Zimbra Desktop và Zimbra Web Client).
- Sổ địa chỉ (Contacts): Quản lý sổ cá nhân của từng thành viên(Địa chỉ, số điện thoại, thông tin cá nhân,…) và sổ chung của đội nhóm.
- Danh mục công việc (Tasks): Danh sách các công việc, giúp theo dõi tiến độ, và việc quản lý được tối ưu hơn, cũng như có phân chia độ ưu tiên công việc và khối lượng công việc đã hoàn thành của mỗi cá nhân hoặc đội nhóm.
- Tài liệu (Documents): Dễ dàng soạn thảo văn bản tài liệu dưới dạng Wiki của mỗi cá nhân hoặc đội nhóm. Cho phép người dùng in trực tiếp văn bản soạn thảo xong hoặc trao đổi(gửi – nhận) qua Email.
- Cặp tài liệu hồ sơ (Briefcase): Với công cụ này có thể lưu trữ tài liệu, tập tin cho việc dùng cá nhân hoặc chia sẻ với nhóm hoặc cá nhân khác dùng chung.
- Chat: Chat nội bộ với nhau trong mạng LAN hoặc trên Internet.
- Lịch công tác (Calendar): Thông tin về lịch cá nhân và lịch nhóm, hỗ trợ cho phép tạo cuộc hẹn, tự động gửi mail theo lịch trình(Như thời gian hợp được lên lịch trước)…
- Preferences: Chỉnh sửa nâng cao với Zimbra, Gồm thay đổi Theme, phông chữ, ngôn ngữ, phím tắt, chữ ký, bộ lọc mail….

### 3. Cấu hình Zimbra
Disk: Trên 20GB Ram: 6GB IP(VPS hoặc máy chủ), domain, mail domain

## Cài đặt Zimbra

Bước 1: Cập nhật bản ghi mail

Để phục vụ cho việc cài đặt. Bạn hãy trỏ bản ghi mail như sau trước nhé. Bên dưới là 2 bản ghi và mẫu của mình.

![image](https://user-images.githubusercontent.com/105496635/186051480-de77d99a-9a46-4ea1-8d89-587a31bb5250.png)

Bước 2: Cập nhật SElinux
-Sử dụng lệnh `vi /etc/selinux/config` để vào mục thay đổi, chuyển từ `ensabled`

![image](https://user-images.githubusercontent.com/105496635/186096391-73a63011-5e34-4471-9f68-bb4e1245f24b.png)

 thành `disabled`

![image](https://user-images.githubusercontent.com/105496635/186097046-7c29276f-b853-4cd4-af84-65fe3ddde998.png)

Và sau đó sử dụng `sestatus` để kiểm tra

![image](https://user-images.githubusercontent.com/105496635/186097409-6419b3fb-e332-41eb-983e-43e42071da9a.png)

### Thực hiện stop postfix và remove postfix.
- Postfix là một phầm mềm nguồn mở được dùng để gửi mail (Mail Transfer Agent-MTA). Được phát hành bởi IBM với mục tiêu thay thế trình gửi mail phổ biến là sendmail. Nó được trang bị trên hệ điều hành do đó bạn hãy xoá bỏ để sử dụng dịch vụ riêng của Zimbra.

               ` `  systemctl stop postfix
                  systemctl disable postfix``

cập nhật hệ thống và khởi động lại.
                `yum update -y ; reboot`
                
 Bướm 3. Kiểm tra và set host name.                
     hostnamectl set-hostname mail.xn--hoangvip-1ya8k.vn
     exec bash
![image](https://user-images.githubusercontent.com/105496635/186100082-9a2768ab-9b49-41c3-b97d-adce02b21c8a.png)

- Sau khi set hostname xong bạn thêm dòng sau vào file hosts bạn nhớ thay đổi IP bằng IP của bạn

vi /etc/hots
`192.168.110.131 mail.xn--hoangvip-1ya8k.vn`

![image](https://user-images.githubusercontent.com/105496635/186100551-4d1712a5-e766-49e0-92e9-882cc482d156.png)


Bước 4: Cài đặt Zimbra Server
- Bạn thực hiện chạy lệnh sau để install Zimbra & ZCS dependencies

`yum install unzip net-tools sysstat openssh-clients perl-core libaio nmap-ncat libstdc++.so.6 wget -y`

- Bước tiếp theo bạn cần Download Zimbra và cài đặt. Và bạn cần tạo một thư mục zimbra để cài vào đó. Bạn cũng có thể xem các phiên bản Zimbra ở trang chủ để download nhé.

                  mkdir zimbra && cd zimbra

                  wget https://files.zimbra.com/downloads/8.8.15_GA/zcs-8.8.15_GA_3869.RHEL7_64.20190918004220.tgz --no-check-certificate


- Sau khi download về hoàn tất bạn tiến hành giải nén file ra
                   
                   `tar zxpvf zcs*.tgz`


- Truy cập vào thư mục vừa giải nén và chạy lệnh ./install

                  cd zcs* && ./install.sh

![image](https://user-images.githubusercontent.com/105496635/186095631-e8df0aa8-dd45-401b-8d54-3dfbd512cbad.png)


![image](https://user-images.githubusercontent.com/105496635/186106969-9ba83c4b-d820-4ee6-b041-d45321faa01d.png)

![image](https://user-images.githubusercontent.com/105496635/186107422-412024c8-d55e-4762-9f9f-29874bf20954.png)

![image](https://user-images.githubusercontent.com/105496635/186108314-1f7a104a-33c5-44e4-a818-bcc1a05cfcf8.png)

![image](https://user-images.githubusercontent.com/105496635/186109085-0e3fd7a4-ca48-4d62-98db-85f0fdcc09c1.png)


- Như vậy là đã hoàn tất rồi nhé, nếu máy chủ bạn có cài Firewall bạn cần mở các port sau ra để email hoạt động

Bước 6: Sau khi cài đặt xong khởi động lại dịch vụ zimbar bằng lệnh :

               su zimbra
               zmcontrol restart
Bước 7: Mở port
- Dưới đây là các Port bạn cần mở
 `25,80,110,143,443,465,587,993,995,5222,5223,9071,7071`

                 firewall-cmd --permanent --add-port={25,80,110,143,443,465,587,993,995,5222,5223,9071,7071}/tcp
                    firewall-cmd --reload
Giao diện của Zimbra sau khi cài đặt
![image](https://user-images.githubusercontent.com/105496635/186324192-6af9a744-753c-4e53-85e3-8088fd18a2e8.png)

# Thiết lập password cho Zimbra
Sau khi truy cập vào Zimbra, chúng ta tiến hành thay đổi mật khẩu

- Bước 1: SSH vào email server và chuyển sang thao tác với user zimbra sử dụng lệnh `su -zimbra`

- Bước 2: Tiếp đó kiểm tra có những quyền admin nào sử dụng `zmprov gaaa`

![image](https://user-images.githubusercontent.com/105496635/186325758-9f76494b-deb8-48dd-945e-9b200a417709.png)

- Bước 3: Thay đổi mật khẩu bằng lệnh `zmprov sp <admin email address> <new password>`

Ví dụ `zmprov sp admin@mail.hoaàngviíp.vn`

![image](https://user-images.githubusercontent.com/105496635/186326542-c2be1ec3-5681-46d5-bdd5-7abdd6f7f2df.png)

Và sau đó sử dụng mật khẩu truy cập vào 

![image](https://user-images.githubusercontent.com/105496635/186326629-81789344-e8c5-4628-b9a5-c2226e9eede2.png)












