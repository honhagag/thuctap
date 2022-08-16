# Những cách import file sql vào sql server nhanh nhất, hiệu quả nhất

## Cách 1 : Sử dụng Detack - Attack Cơ sở dữ liệu

Bước 1 : Click chuột phải vài Database tiếp theo chọn Task - Detack

![image](https://user-images.githubusercontent.com/105496635/184828924-a6c2e972-23ea-4d3d-8554-58015da38ea9.png)


Bước 2 : Thực hiện sao chép 2 file Database

Thông thường 2 file nằm trong thư mục Data nên chúng ta truy cập theo đường dẫn sau : 

Chọn ổ C -> Program Files -> Microsoft SQL Server -> MSSQL15.SQLEXPRESS -> MSSQL -> DATA 

![image](https://user-images.githubusercontent.com/105496635/184829915-0fbf095d-f833-4d50-a7ae-5b1aad82e223.png)

Bạn chỉ cần gửi 2 file này cho người mà bạn muốn chia sẻ, với 2 file đó họ đủ sức khôi phục lại dữ liệu trên máy tính không giống.

Bước 3 : Khôi phục dữ liệu trên máy tính khác 

Sau khi người nhận đã nhận được 2 file đã chia sẻ , bạn dán 2 file vào đường link :

ổ C -> Program Files -> Microsoft SQL Server -> MSSQL15.CHINHTRAN -> MSSQL -> DATA 

thực hiện paste xong tiếp theo chúng ta tiến hành attack lại database bằng cách :

Click chuột phải vào Database chọn Attack tiếp đến chọn Add -> Chọn Database -> OK -> OK

![image](https://user-images.githubusercontent.com/97047640/172795007-995e653d-6d36-4d50-b0a7-b464975149ba.png)

![image](https://user-images.githubusercontent.com/105496635/184831548-70e63685-d957-4446-ae95-a92e3ad6fac9.png)

Sau khi thực hiện xong các bạn sẽ thấy Database vừa mưới thêm hiển thị ở phần Data . Nếu nó chưa hiện thì hay Refresh lại để thấy phần Database vừa mới có trong SQL.

![image](https://user-images.githubusercontent.com/105496635/184832513-86eabaaf-28d3-49e2-b910-a123704611e5.png)


# Cách 2 : Xuất File SQL 

Bước 1 : Click chuột phải vào Database chọn Task - Chọn Generate Scripts :

![image](https://user-images.githubusercontent.com/105496635/184833176-ecedc1d1-2b01-44a1-bb06-88b6fd252085.png)


Bước 2 Nhấn Next để tiếp tục quá trình 

![image](https://user-images.githubusercontent.com/97047640/172798010-6d3344d2-754a-4ff3-8f9b-060065339a60.png)

Bước 3 : Chọn 1 số Table hoặc chọn lựa tất cả

![image](https://user-images.githubusercontent.com/97047640/172798073-6bfaaafb-1829-4fbc-8b86-c75017e3ab50.png)

Bước 4 : Để có thể xuất file .sql kèm thêm dữ liệu thì cần phải thực hiện các thao tác như sau :

Advanced - Types of data no script chọn Schema and data - OK - Next 

![image](https://user-images.githubusercontent.com/97047640/172799032-c766d8c7-898e-44ee-9a7a-d706c733d394.png)

Bước 5 : Bấm next để tiếp tục 

![image](https://user-images.githubusercontent.com/105496635/184833512-ce0fca28-bb75-4371-af75-84a7f0608c5f.png)

![image](https://user-images.githubusercontent.com/105496635/184833598-288e5e72-c822-408e-b81c-30841ac7b77e.png)



Bước 6 : Kiểm tra tình trạng xuất file và bấm Finish để hoàn thành công cuộc xuất file hoangga.sql

![image](https://user-images.githubusercontent.com/97047640/172800407-9d89ef94-1717-4f70-adc0-6158077f090e.png)

Sau khi thành công 6 bước chúng ta sẽ thấy file chinhtran.sql nằm trong đường dẫn : C:\Users\vip\Documents\hoangga.sql

![image](https://user-images.githubusercontent.com/105496635/184835032-d94d2b38-bd68-4a21-87b9-932ec3db7b33.png)

## Cách dùng file hoangga.sql

Bước 1 : mở SQL Server lên chọn vào File - Open - File 

![image](https://user-images.githubusercontent.com/97047640/172800772-5f69b2ee-fdce-4866-a9b5-935feb3b69c6.png)

Bước 2 : Chọn file chinhtran.sql để mở lên trong SQL Server 

*Lưu ý : Cần tạo 1 Database giống với tên database cũ để chứa dữ liệu chuẩn bị nhập vào .

Bước 3 : Lự chọn tất cả các câu lệnh và nhấn Execute. Kết quả sẽ hiện ra thông báo : Command (s) completed successfully. Open Database Chinhtran ra sẽ thấy được toàn bộ các bảng và dữ liệu mà chúng ta cần.

![image](https://user-images.githubusercontent.com/105496635/184835299-7d5e95ab-637b-4320-99d6-fdebdabc6ff6.png)



