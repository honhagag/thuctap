# AFR
## 1. Giới thiệu về APF
- APF là tên viết tắt của Advance Policy Firewall(tường lửa chính sách nâng cao)
- Đây là một loại tường lửa do 1 nhóm phát triển và xây dựng trên các ruless của iptables
- Không giống như tường lửa CSF, APF có tính linh hoạt cao hơn và gần như không cần phải thực hiện các bước cài đặt để có thể sử dụng ngay lập tức

## 2. Cài đặt
### Bước 1 : Truy cập vào thư mục gốc -> Tiến hành dowload và giải nén file APF

- Truy cập thư mục gốc
 
        cd /root/


- Tải thư mục

         wget http://www.rfxn.com/downloads/apf-current.tar.gz
         
 
 ![image](https://user-images.githubusercontent.com/105496635/187859740-42e95735-e84c-4eba-8c93-938e1296bf79.png)


- Giải nén tập tin

            tar -zxvf apf-current.tar.gz

![image](https://user-images.githubusercontent.com/105496635/187859867-5e64fdae-281d-495c-ad87-ff4adbb2b20f.png)


### Bước 2: Tiến hành cài đặt APF Firewall

- Di chuyển vào thư mục vừa giải nén
          
          cd apf-1.7.6/

- Tiến hành cài đặt và khởi động

       sh ./install.sh
      


![image](https://user-images.githubusercontent.com/105496635/187866615-b185e538-2de0-4166-a121-22f4a48a54b0.png)


        apf -s 

![image](https://user-images.githubusercontent.com/105496635/187866707-86950e3e-aacf-40a9-a8f7-37293e6e43b5.png)


### Bước 3: cấu hình và restart.

            nano /etc/apf/conf.apf


![image](https://user-images.githubusercontent.com/105496635/187867426-4e538f0d-feff-4d30-b676-ae29b6283c77.png)




- Khởi động lại dịch vụ

        apf -r


![image](https://user-images.githubusercontent.com/105496635/187867689-a608a54e-2e75-4e01-b8f3-858b72ebb260.png)


- Xem trang thái của dịch vụ apf

       apf status

![image](https://user-images.githubusercontent.com/105496635/187867939-db61542f-dc46-41e1-9009-9b5c18c9078b.png)











