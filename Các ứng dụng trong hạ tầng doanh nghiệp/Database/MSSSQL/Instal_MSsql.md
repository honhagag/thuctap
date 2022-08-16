# Cài đặt và sử dụng Mssql trên windows server

Link download: https://www.microsoft.com/en-us/sql-server/sql-server-downloads

![image](https://user-images.githubusercontent.com/62273292/161185558-1ef111cc-e8b3-4402-b8e5-069989c6a6fb.png)

Chọn custom

![image](https://user-images.githubusercontent.com/62273292/161185663-be0f044f-23b3-4bbf-a81a-e0b1d4ddb635.png)

Cài đặt

![image](https://user-images.githubusercontent.com/62273292/161186812-2b7663be-5717-4972-bd4c-061ed386cbe2.png)

Cài ssms

![image](https://user-images.githubusercontent.com/62273292/161187204-0c6aed17-661f-4e66-a018-e20119c599cd.png)

![image](https://user-images.githubusercontent.com/62273292/161188700-8ebae1ff-b79f-4396-8f83-f5ca260a5fe3.png)

![image](https://user-images.githubusercontent.com/62273292/161212254-df2083dd-ffdf-4518-827c-f26c6e7e3daa.png)


Có 2 chế độ xác thực chính là Windows Authentication và SQL Server Authentication

![image](https://user-images.githubusercontent.com/62273292/161212428-3c09c86a-ad58-4fce-ae4a-585a86a591e3.png)


  Chế độ Windows Authentication: Là chế độ xác thực người dùng windows, chỉ cần có user vào windows là được, không cần nhập Password.
  
  Chế độ SQL Server Authentication: Là chế độ xác thực người dùng mức SQL Server, do SQL server quản lý user và password, người dùng phải có user và password mới có thể  truy cập vào SQL Server
      - SQL Server có 1 user mặc định full quyền là security admin- viết tắt là sa.
      - Password của user sa do người dùng nhập vào khi cài đặt SQL Server
   


Khi đăng nhập vào thì sẽ có giao diện chính 

![image](https://user-images.githubusercontent.com/62273292/161212767-bec8cdda-244e-4aba-b6b0-49756e35e4a4.png)

Chọn new Query và bắt đầu thực hiện các câu lệnh cơ bản

Tạo 1 cơ sỡ dữ liệu mới

![image](https://user-images.githubusercontent.com/105496635/184814290-ac9a2093-e773-4859-af2a-1eb1314a9f4a.png)

Tạo bảng cho database

![image](https://user-images.githubusercontent.com/105496635/184815096-11da6786-c902-4576-aa91-a1fc31b81585.png)

Chèn dữ liệu vào trong bảng

![image](https://user-images.githubusercontent.com/105496635/184816522-7bcf703d-0181-45d3-b490-06f6d27a3774.png)

Nối 2 bảng lại với nhau với trường id

![image](https://user-images.githubusercontent.com/105496635/184817526-65c8c495-c470-4e67-846d-dcf7dce38f10.png)


Dùng lệnh select để xem dữ kiệu trong bảng

![image](https://user-images.githubusercontent.com/105496635/184821882-72dc8ec2-6f4e-46f7-a99b-94c5e2608815.png)

Dùng lệnh update để cập nhật dữ liệu trong bảng

![image](https://user-images.githubusercontent.com/105496635/184822497-24fa1e20-9375-4ab6-9603-9959595cff1a.png)

Lệnh delete: chúng ta có thể xóa dữ liệu,  xóa  database

![image](https://user-images.githubusercontent.com/105496635/184823356-6599ab17-d35a-4f48-938b-c43e850aeb78.png)


![image](https://user-images.githubusercontent.com/105496635/184824041-458d8e30-fe12-418b-996e-afb491c8b1cb.png)

























      
      
