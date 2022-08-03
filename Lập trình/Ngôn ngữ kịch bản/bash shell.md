# Lập trình Bash Shell (Bash script)
## Giới thiệu Bash Shell:
Đối với bất kỳ những ai đã và đang làm việc với hệ thống Linux thì chắc chắn đều thấy sự hiệu quả của nhứng script Bash Shell. Việc sử dụng script Bash shell giúp các công việc lặp đi lặp lại trên Linux được thực hiện hiệu quả, ít sai sót. Tuy nhiên để viết các script Bash shell ngắn, gọn và có thể tận dụng được trên nhiều môi trường thì chúng ta cần có những kiến thức và lượng thực hành nhất định.

### 1. Bash Shell: Hello World
#### Chế độ Shell tương tác (Interactive Shell)
Chúng ta có thể hiểu đơn giản Shell interactive là dạng sử dụng câu lệnh trực tiếp trên môi trường Unix như ví dụ dưới.

Ví dụ, sử dụng Bash để in ra output là Hello World như sau :

![image](https://user-images.githubusercontent.com/105496635/182521772-558ba0d5-5cd2-49dc-9891-426db95d559e.png)

#### Chế độ Shell không tương tác (Non-Interactive Shell)
Thay vì thực hiện từng câu lệnh Bash một. Chúng ta có thể tổ hợp chúng vào một file script và có thể sử dụng lại nhiều lần.

Ví dụ, tạo một script Hello World

##### Tạo một file với tên là hello-world.sh

![image](https://user-images.githubusercontent.com/105496635/182521897-f369d1a6-7a61-49ea-ab55-d18d50aa2574.png)

##### Phân quyền thực thi được với câu lệnh

![image](https://user-images.githubusercontent.com/105496635/182540601-c2390120-3399-49fc-a575-a29a35ff90a7.png)

##### Thêm nội dung sau vào script
![image](https://user-images.githubusercontent.com/105496635/182540873-bb5168dc-0d2d-42bb-af33-f64c721be9cd.png)
- Dòng 1 : Dòng đầu tiên của script phải bắt đầu với ký tự ` #! `, theo đúng cấu trúc shebang1. Cấu trúc shebang sẽ chỉ cho OS chạy chương trình `/bin/bash` để thực hiện các nội dung của script. VD : /bin/bash hello-world
- Dòng 2 : Sử dụng câu lệnh echo để ghi dòng Hello World ra output.
Thực hiện chạy sript hello-world.sh theo 1 trong 3 cách sau:
![image](https://user-images.githubusercontent.com/105496635/182541381-b21409e6-ef18-4dcf-84c9-68e0402d0031.png)

### 2. Sử dụng các biến trong Linux
Tạo một file mới tên gọi `hello.sh` với nội dung bên dưới và cấp quyền thực thi `chmod +x hello.sh`

Thực hiện chạy sript với cú pháp `./hello.sh`. Output mong đợi sẽ là :

![image](https://user-images.githubusercontent.com/105496635/182542058-c6a94829-c1f4-42b6-b225-d9ce5c0caa08.png)

- Nội dung script như sau :
 Phân tích từng dòng của script sẽ như sau :
 - Dòng 1 : #!/usr/bin/env bash : Cú pháp shebang chỉ ra chương trình cần thực thi với Bash shell
 - Dòng 2 : Gán biến who_variable có nội dung là World.
 - Dòng 3 :
 `printf` : câu lệnh in
`%s` : format chỉ ra rằng biến phía sau phải là dạng string
`\n` : khi có thêm ký tự thì sẽ xuống dòng mới
`$who_variable` : biến được khai báo ở dòng trên

### 3. Truyên tham số vào biến với User Input
- Các biến còn có thể được truyền vào trực tiếp từ người dùng như sau :

![image](https://user-images.githubusercontent.com/105496635/182544122-45f5c4dd-851f-451b-8b60-f7b6c8f6692f.png)

Khi script chạy tới dòng thứ 2, câu lệnh read sẽ đọc dữ liệu truyền vào từ người dùng, sau đó gán dữ liệu đó vào biến name.

Kết quả như sau :

![image](https://user-images.githubusercontent.com/105496635/182544169-71d988df-4e2a-464d-8677-a97d0ecf3788.png)


  
