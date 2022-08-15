# Các thao tác với phpMyAdmin

## I. Các thao tác cơ bản 
### 1. Tạo DB
Ở cột bên trái, click chọn **New** sau đó nhập vào tên CSDL của bạn, chọn kiểu mã hóa kí tự rồi chọn **Create**:

![image](https://user-images.githubusercontent.com/105496635/184591086-a2624b8b-b6d0-4f6f-9084-bdacac57686f.png)

Sau khi tạo thành công, ta sẽ thấy Database vừa tạo ở phần bên trái giao diện:

![image](https://user-images.githubusercontent.com/105496635/184591108-d45c78d0-dc4f-4da3-9ecc-158a3ecdefc0.png)

### 2. Tạo bảng
- Chọn DB muốn tạo bảng

- Chọn phần Create table, nhập tên bảng, số cột của bảng rồi click **Go** để tiến hành tạo bảng

![image](https://user-images.githubusercontent.com/105496635/184591139-2d081d58-af61-43fe-9a35-ba8ddfb78d54.png)

- Sau đó, ta sẽ cấu hình các thuộc tính của bảng

![image](https://user-images.githubusercontent.com/105496635/184591183-7bd26f9b-8825-4ae1-8c1b-d89fa4a4b862.png)

- **Các thuộc tính của cột**
    - **Name** – Tên của cột;
    - **Type** – Loại dữ liệu sẽ được lưu trong cột;
    - **Length/Values** – Độ dài của trường;
    - **Default** – tùy chọn giúp bạn đặt giá trị mặc định cho cột. Điều này sẽ hữu ích trong trường hợp bạn cần đặt dấu thời gian;
    - **Collation** – Đối chiếu dữ liệu cho từng trường;
    - **Attributes** – Gán bất kỳ thuộc tính đặc biệt nào cho trường;
    - **Null** – Xác định giá trị của trường có thể để trống hay không;
    - **Index** – Đặt chỉ mục cho các hàng;
    - **A_I** – viết tắt của Auto Increment. Nếu tùy chọn này được bật thì các giá trị trong trường của cột sẽ tự động tăng lên;
    - **Comments** – Ghi chú về cột

  ![image](https://user-images.githubusercontent.com/105496635/184591357-44d5dd0e-36ed-4897-a8ba-2e27147d8da7.png)
    
- Sử dụng **Preview SQL** để xem xem các thao tác trên dưới dạng câu lệnh truy vấn

   ![image](https://user-images.githubusercontent.com/105496635/184591368-148962d1-e2df-4061-aaca-96607feca959.png)

- Chọn **Save** để lưu cấu hình với bảng. Sau khi Save, sẽ có giao diện như sau:

    ![image](https://user-images.githubusercontent.com/105496635/184591384-22fe8504-b3a0-4850-b439-2cf140c8516c.png)

### 3. Vị trí đang làm việc
Ta có thể thấy nơi ta đang làm việc với database như hình bên dưới

![image](https://user-images.githubusercontent.com/105496635/184591423-d1cbf5df-1f3c-47f1-8246-745438d047ab.png)

## II. Thao tác với Databases
### 1. Truy cập Database
Ta chọn Database ở list bên trái, hoặc vào tab Database rồi chọn Database cần truy cập

![image](https://user-images.githubusercontent.com/105496635/184591443-5eb7a7d7-e97f-480b-9672-2799e7f397a3.png)

![image](https://user-images.githubusercontent.com/105496635/184591459-eeed3743-a82e-41dc-af0f-0b25c4e5b0fa.png)

### 2. Xóa Database
Chọn Database, chọn tab **Operations** -> **Drop the database (DROP)**
![image](https://user-images.githubusercontent.com/105496635/184591510-9f485b81-2179-4d56-a4ed-e27c7e28f61f.png)

![image](https://user-images.githubusercontent.com/105496635/184591529-c721fc40-1878-4cf2-a08c-4ce42add0260.png)


## III. Thao tác với bảng
### 1. Xem bảng
Ta có thể click chuột vào tên bảng hoặc click vào **Browse**

![image](https://user-images.githubusercontent.com/105496635/184591562-a567bac9-efd8-4432-ba9a-7fec2c062fdd.png)

Sau đó, ta sẽ vào giao diện của bảng vừa chọn:

![image](https://user-images.githubusercontent.com/105496635/184591623-8ac291eb-aa35-4ce5-9115-d8c07a4676b8.png)

### 2. Chỉnh sửa bản ghi trong bảng
Để chỉnh sửa bản ghi nào đó trong bảng, ta click chuột **Edit** tại bản ghi

![image](https://user-images.githubusercontent.com/105496635/184591668-ac816866-f7f1-4bf7-8fb1-0b786fbdaa3c.png)

Ta sẽ thấy cấu trúc bản ghi kèm giá trị hiện tại, ta có thể chỉnh sửa và click **Go** để hoàn tất thay đổi.

![image](https://user-images.githubusercontent.com/105496635/184591795-7de50554-2133-4771-861c-932655829df7.png)
### 3. Thêm bản ghi
Ta có thể click **Insert** tại bảng cần thêm bản ghi

![image](https://user-images.githubusercontent.com/105496635/184591819-ec7b8f60-70c1-4ffa-8ca6-47ff3e41ff57.png)

Sau đó, ta sẽ thêm các bản ghi vào bảng rồi click chuột **Go** để thêm bản ghi

![image](https://user-images.githubusercontent.com/105496635/184591832-d34a8b88-0821-4d47-88d9-daa91a73396c.png)
Ta sẽ thấy bản ghi được thêm trong bảng

![image](https://user-images.githubusercontent.com/105496635/184591855-ad818577-1575-41c9-8c16-ba6fd3062e1e.png)

### 4. Xóa bản ghi
Click chuột vào **Delete** trên bản ghi muốn xóa

![image](https://user-images.githubusercontent.com/105496635/184591886-c04783e6-6a10-4d10-be36-f7dcc9b30acc.png)

Click **OK** để xác nhận Xóa

![image](https://user-images.githubusercontent.com/105496635/184591903-216c314a-fe8d-4faa-aaf0-717db9724fc7.png)

### 5. Làm trống bảng cơ sở dữ liệu
Để xóa hết dữ liệu bảng ta click **Empty**

![image](https://user-images.githubusercontent.com/105496635/184591926-dea3f950-70a5-45a7-9cbc-eeec871b0427.png)

Click **OK** để xác nhận xóa

![image](https://user-images.githubusercontent.com/105496635/184591950-2ce695e4-217f-48e0-af0e-8a1646371281.png)

### 6. Xóa bảng
Click **Drop** trên bảng để xóa

![image](https://user-images.githubusercontent.com/105496635/184591962-1dd55af3-6c12-469d-94f8-5f613e74d5f9.png)

Click **OK** để xác nhận

![image](https://user-images.githubusercontent.com/105496635/184591988-180c098f-f90d-4d58-b8f4-f46a3f524494.png)

## IV. Query
Ta có thể truy vấn dữ liệu thông qua các câu truy vấn.

Để làm điều này, ta chọn Tab **Query** rồi viết truy vấn. Click **Go** để chạy truy vấn.
