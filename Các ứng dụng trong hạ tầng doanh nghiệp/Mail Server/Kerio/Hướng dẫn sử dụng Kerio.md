# Cách tạo mới một Domain trên Kerio
## Chuẩn bị:
- Domain: xn--hoangvip-1ya8k.vn

- Nhu cầu cho 10 tài khoản
## Các bước thực hiện
Bước 1:  Vào configuration -> domain -> add -> local domain

Domain : Tên domain cần đưa vào

Description : Miêu tả thông tin liên quan

User count : Giới hạn số user cho domain

![image](https://user-images.githubusercontent.com/105496635/185532498-bd2c61eb-5c1b-4f8c-8069-3230c89cc819.png)


![image](https://user-images.githubusercontent.com/105496635/185532966-60f7b48a-b13b-4e3d-83cc-f7c170183230.png)

Bước 2 : Tab Security

Chọn theo như trong hình : 2 thông số trên nhằm đảm bảo vấn đề liên quan đến password.

![image](https://user-images.githubusercontent.com/105496635/185533009-e31e1470-f608-4f46-9750-e555736d8341.png)


Bước 3: Tab Mesages

Giới hạn dung lượng mail gửi ra : 50MB

Ngoài ra bạn có thể cấu hình thêm phần Items mục địch nhằm tối ưu hệ thống dung lượng của user.

![image](https://user-images.githubusercontent.com/105496635/185533049-bf69e7f1-12e0-458f-b6f0-362305026d38.png)


Bước 4: Tab Directory Service

Ở phần này nếu bạn có sử dụng Microsoft Active Directory thì bạn cấu hình tại đây. Ở phần này mình không có sử dụng AD nên mình không cấu hình.

![image](https://user-images.githubusercontent.com/105496635/185533233-6e4a3007-9de6-48cc-8046-47eeb1f9a0b2.png)


Bước 4: Tab Directory Service

Ở phần này nếu bạn có sử dụng Microsoft Active Directory thì bạn cấu hình tại đây. Ở phần này mình không có sử dụng AD nên mình không cấu hình.


![image](https://user-images.githubusercontent.com/105496635/185533268-d2261713-c55e-4dee-b24b-e78e97da3a51.png)


Bước 5: Tab Custom Logo

Ở đây nếu bạn có công ty logo riêng thì bạn có thể upload lên đây : Kích thước đề nghi 142×45

Cài đặt thành công cho 1 domain !

![image](https://user-images.githubusercontent.com/105496635/185533328-0579028c-9ccd-4dbe-a262-743efff662bb.png)


Bước 6 : Set domain xn--hoangvip-1ya8k.vn thành domain chính để quản lý.

Chuột phải vào domain xn--hoangvip-1ya8k.vn

![image](https://user-images.githubusercontent.com/105496635/185533403-d012bb24-5e29-4a40-8af6-51912a4344c4.png)


2. Hướng dẫn tạo user cho domain xn--hoangvip-1ya8k.vn vừa tạo

Bước 1: Login vào account -> User -> chọn domain

![image](https://user-images.githubusercontent.com/105496635/185534253-174eb58a-61a9-4c9d-8836-e7f1efded3ab.png)


Bước 2: Add user vào domain trên

Chọn add -> điền thông tin user

Bước 3: Tại tab General Điền đầy đủ thông tin


![image](https://user-images.githubusercontent.com/105496635/185534460-f27e1abf-5f68-4e0e-b15c-027312300e34.png)

Bước 4: Tab contact Ở phần này bạn có thể điền tùy ý thông tin hoặc không điền cũng không có vấn đề gì


![image](https://user-images.githubusercontent.com/105496635/185534844-adc409d6-9283-4ccd-9721-460539ddd65b.png)





Bước 5: Nếu bạn có group riêng thì bạn vào phần group để cấu hình

Ví dụ : Group IT, group Nhân sự, group kinh doanh … nếu không có thì không cần cấu hình

Bước 6: Tab Rights

Ở tab này là phần gán quyền cho user trên, nếu là admin thì cần quyền gì, user thì quyền gì

ví dụ admin có toàn quyền trên domain  xn--hoangvip-1ya8k.vn , cái này như phần quyền cho admin cấp thấp hơn quản lý.

Nếu không bạn có thể cho admin có toàn quyền trên server.


![image](https://user-images.githubusercontent.com/105496635/185535350-34504889-7a65-4415-a429-c6d08f74d538.png)

Bước 6: Tab Quota

Để giới hạn dung lượng cho mỏi user thì bạn vào đây để cấu hình

Ở đây mình giới hạn user 500 MB




![image](https://user-images.githubusercontent.com/105496635/185535442-2d4f4b48-1736-47a9-bc85-862af9b0d99a.png)



Bước 7: Tab mesages

Ở phần này tương tự như phần cấu hình chính sách tại phần cấu hình domain, tuy nhiên nếu bạn là admin thì và bạn muốn cấu hình riêng cho từng user thì bạn cấu hình tại đây. Nếu không thì tất cả các user sẽ được cấu hình chính sách theo domain chính.

Ví dụ : domain chính là xn--hoangvip-1ya8k.vn giới hạn gửi mail là 50Mb thì tất cả user đều bị giới hạn, nhưng bạn muốn sếp có quyền hạn gởi mail 100MB thì bạn sẽ cấu hình tại đây để sếp được ngoại lệ.

![image](https://user-images.githubusercontent.com/105496635/185535519-9804bdfb-aba4-4fca-9d7f-2711438a82c6.png)

Bước 8: Kiểm tra lại domain vừa tạo có hoạt động hay không https://IP_Server_mail:4040/admin

![image](https://user-images.githubusercontent.com/105496635/185535769-b9bc653f-4186-4075-b112-80cf97ab1092.png)


![image](https://user-images.githubusercontent.com/105496635/185535986-20e21341-c4f9-469d-8f7b-45f100cb83e5.png)

Như vậy là bạn đã login thành công. (Đây là trang admin quản trị của user admin)

Tóm lại : Bạn đã add một domain ngonmame.com vào hệ thống, và tạo một user admin quản trị domain này. Nếu bạn muốn add thêm user cho domain ngon mà mẹ này thì bạn cứ thực hiện add user là được.

Lưu ý : Bước kiểm tra là ta kiểm tra bằng IP, bây giờ bạn muốn trỏ login vào bằng domain thì bạn chỉ cần tạo một record mail.xn--hoangvip-1ya8k.vn trỏ về địa chỉ IP trên là được.

Mình cần lưu ý 2 thông tin sau :

Lưu ý : tùy vào từng công cụ quản trị domain thì có hình ảnh khác nhau và quản trị khác nhau nhưng các record thì giống nhau.

![image](https://user-images.githubusercontent.com/105496635/185537890-434eecbf-a501-4cfa-a446-2671f96123cf.png)



Kiểm tra lại hệ vấn đề trên bằng cách Ping và Kiểm tra mx record

![image](https://user-images.githubusercontent.com/105496635/185537961-ee04cace-670e-4df4-b69e-2e47bb6cadd1.png)

Kiểm tra record MX

![image](https://user-images.githubusercontent.com/105496635/185538365-e5f38e88-8bd4-4eae-ae2e-6f0071f66f67.png)


Như vậy bạn đã login thành công ! Có thể gửi mail được rồi! (Đây là trang webmail cho client) Kiểm tra truy cập bằng domain



![image](https://user-images.githubusercontent.com/105496635/185538400-c00875d4-650f-4210-bb2e-ee1b7c78684f.png)






