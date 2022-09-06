# Cài đặt cPanel trên CenOS7

## Bước 1:  Bạn cần tắt SELINUX trước khi thực hiện cài đặt

              vi  /etc/selinux/config

SELINUX= disabled



## Bước 2: Vô hiệu hóa Firewall


        systemctl stop firewalld
        systemctl disable firewalld


## Bước 3: Cập nhật hệ thống


          sudo yum update



## Bước 4: Vô hiệu hóa Network Manager


             systemctl stop NetworkManager.service
             systemctl disable NetworkManager.service
             systemctl enable network.service
             systemctl start network.service



![image](https://user-images.githubusercontent.com/105496635/188585278-4edf2624-1c49-4a05-8e12-f92ba028ab95.png)


## Bước 5: Tải file và chạy file cài đặt.

      cd /home
      curl -o latest -L https://securedownloads.cpanel.net/latest
      sh latest

![image](https://user-images.githubusercontent.com/105496635/188585599-097b0734-18a6-488a-b3b1-d12fa9d63215.png)





























