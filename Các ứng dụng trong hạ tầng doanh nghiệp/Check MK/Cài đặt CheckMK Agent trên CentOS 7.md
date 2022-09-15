1. Chuẩn bị

host:  192.168.110.183 linux


2. Lấy link để cài đặt agent trên checkmk server.


![image](https://user-images.githubusercontent.com/105496635/190333834-6ddaf28c-1258-4d79-a06c-beba897b8c3d.png)

Chọn vào và nhấp phải để lấy link liên kết

![image](https://user-images.githubusercontent.com/105496635/190333916-0189a3a7-5a1e-418c-aaed-d02d38f6af3f.png)

Ở đây, có 3 packet dành cho 3 DISTRO:

    *.deb: Dành cho các host sử dụng DEBIAN
    *.rpm: Dành cho các host sử dụng RHEL
    *.msi: Dành cho các host sử dụng MS Windows

Và tiến hành cài đặt bằng lệnh

          wget http://192.168.110.163/hoangga/check_mk/agents/check-mk-agent-2.0.0p26-1.noarch.rpm



![image](https://user-images.githubusercontent.com/105496635/190334326-40758a42-8286-46f0-b7e7-b7061b2518fe.png)


Cài đặt xinet.d

      yum install xinetd -y
      
 ![image](https://user-images.githubusercontent.com/105496635/190336410-bcae1809-080a-421e-b8a7-a6ff3dd05348.png)
     
      
Kiểm tra xinet.d đã đc cài đặt hay chưa.

      rpm -qa | grep xinetd

![image](https://user-images.githubusercontent.com/105496635/190336476-e9b14420-e73f-4e9e-be5f-c3978e5f1cb2.png)


Khởi động hệ thống và cho chạy cùng nginx

      systemctl start xinetd
      systemctl enable xinetd

Cài đặt agent băng lệnh

      rpm -ivh check-mk-agent-*


![image](https://user-images.githubusercontent.com/105496635/190337491-22a55a77-effd-4a80-814b-5cef9a648033.png)



- Tạo host trên CheckMK

Bước 1: 
Chọn setting -> chọn host

![image](https://user-images.githubusercontent.com/105496635/190341659-2de2d709-1fb1-4ef0-bae5-7837ee298380.png)

Bước 2: 

Chọn Add Host

![image](https://user-images.githubusercontent.com/105496635/190341807-061d09c4-01a2-446c-b2f7-eae3488baa2a.png)


![image](https://user-images.githubusercontent.com/105496635/190342924-ba6e5369-4860-49f1-a6ad-4dc92c09928d.png)


Sau khi cấu hình xong và lưu

![image](https://user-images.githubusercontent.com/105496635/190343347-b3bdf61d-a574-44ee-b7c5-85d2ef4713cd.png)


Chờ trong giây lát để update

![image](https://user-images.githubusercontent.com/105496635/190344721-00959e27-e328-4f6c-aa01-a1a74971b0af.png)





























