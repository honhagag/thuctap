# Cách commit code lên Github
## 1. Tạo kho lưu trữ cục bộ (Local Repository)
- Ấn vào dấu + trên menu và chọn New repository.
 
 ![image](https://user-images.githubusercontent.com/105496635/184048267-d4aa622c-e3a0-4380-a9cc-ae189c5598d1.png)
 
 Bạn sẽ cần đặt tên cho kho chứa của bạn, sau đó lựa chọn loại kho chứa phù hợp – Public (ai cũng có thể clone) và Private (chỉ có những người được cấp quyền mới có thể clone).
 
 - Bạn sẽ cần đặt tên cho kho chứa của bạn, sau đó lựa chọn loại kho chứa phù hợp – Public (ai cũng có thể clone) và Private (chỉ có những người được cấp quyền mới có thể clone).
  ![image](https://user-images.githubusercontent.com/105496635/184048538-11ace73f-527f-49f9-b139-9eecac6f99d7.png)
  
 - Sau khi bạn đã chọn xong những tuỳ chọn của repo mới, hãy ấn Create Repository để tạo. 

Khi tạo xong nó sẽ dẫn bạn tới trang hướng dẫn làm việc với kho chứa vừa tạo. Và kho chứa của bạn bây giờ sẽ có địa chỉ là https://github.com/$user-name/$repository, ví dụ ở hình dưới là:
https://github.com/honhagag/comitcodegithub.git

![image](https://user-images.githubusercontent.com/105496635/184049121-d9ddf14c-30ec-4ce5-9f67-db2d91296855.png)

## 2. Clone repo về máy
Tiếp theo, việc của bạn bây giờ là hãy clone repo mới này về máy của mình bằng lệnh git clone địa_chỉ.

Ví dụ ở trên, chúng ta sẽ clone repo về máy bằng lệnh:

$ git clone https://github.com/honhagag/comitcodegithub.git

## 3. Push code lên git
Thêm/sửa/xóa các file/thư mục trên repo vừa clone về, sau đó lần lượt chạy từng lệnh sau:

$ git add

$ git commit -m "điền nội dung commit vào đây"

$ git push origin master

Chú ý: Trỏ đúng thư mục mà chúng ta clone git về, ví dụ cd 'tên thư mục' để chuyển đến.


