# Cú pháp Python cơ bản
## Định danh (identifier) trong Python
 Một định danh (identifier) trong Python là một tên được sử dụng để nhận diện một biến, một hàm, một lớp, hoặc một đối tượng. Một định danh bắt đầu với một chữ cái từ A tới Z hoặc từ a tới z hoặc một dấu gạch dưới (_) được theo sau bởi 0 hoặc nhiều ký tự, dấu gạch dưới hoặc các chữ số (từ 0 tới 9).

 Python không hỗ trợ các Punctuation char chẳng hạn như @, $ và % bên trong các định danh. Python là một ngôn ngữ lập trình phân biệt chữ hoa- chữ thường, do đó viettuts và Viettuts là hai định danh khác nhau trong Python. Dưới đây là một số qui tắc nên được sử dụng trong khi đặt tên các định danh:

- Một định danh là một dãy ký tự hoặc chữ số.
- Không có ký tự đặc biệt nào được sử dụng (ngoại trừ dấu gạch dưới) như một định danh. Ký tự đầu tiên có thể là chữ cái, dấu gạch dưới, nhưng không được sử dụng chữ số làm ký tự đầu tiên.
- Từ khóa không nên được sử dụng như là một tên định danh (phần dưới sẽ trình bày về khác từ khóa này).
- Tên lớp bắt đầu với một chữ cái hoa. Tất cả định danh khác bắt đầu với một chữ cái thường.
- Bắt đầu một định danh với một dấu gạch dưới đơn chỉ rằng định danh đó là private.
- Bắt đầu một định danh với hai dấu gạch dưới chỉ rằng định danh đó thực sự là private.
- Nếu định danh cũng kết thúc với hai dấu gạch dưới, thì định danh này là một tên đặc biệt được định nghĩa bởi ngôn ngữ (ví dụ như __init__ chẳng hạn).

## Các từ khóa trong Python
Bảng dưới liệt kê các từ khóa trong Python. Đây là các từ dành riêng và bạn không thể sử dụng chúng như là các hằng, biến hoặc cho bất kỳ tên định danh nào. Tất cả từ khóa trong Python là chỉ ở dạng chữ thường.

|and	|exec|	not|
|-|-|-|
|assert|	finally|	or|
|break	|for|	pass|
|class|	from	|print|
|continue	|global	raise|
|def	|if	|return|
|del	|import	|try|
|elif	|in	|while|
|else	|is|	with|
|except	|lambda	|yield|

## Dòng lệnh và độ thụt dòng lệnh trong Python
Python không cung cấp các dấu ngoặc nhọn({}) để chỉ các khối code cho định nghĩa lớp hoặc hàm hoặc điều khiển luồng. Các khối code được nhận biết bởi độ thụt dòng code (indentation) trong Python và đây là điều bắt buộc.

Số khoảng trống trong độ thụt dòng là biến đổi, nhưng tất cả các lệnh bên trong khối phải được thụt cùng một số lượng khoảng trống như nhau. Ví dụ:
`
1.  if True:
2.    print "True"
3. else:
4.  print "False"
`
`
1. if True:
2.     print "Answer"
3.     print "True"
4. else:
5.     print "Answer"
6.   print "False"
`


Do đó, trong Python thì tất cả các dòng liên tiếp nhau mà được thụt đầu dòng với cùng lượng khoảng trống như nhau sẽ tạo nên một khối.

## Các lệnh trên nhiều dòng trong Python
Các lệnh trong Python có một nét đặc trưng là kết thúc với một newline (dòng mới). Tuy nhiên, Python cho phép sử dụng ký tự \ để chỉ rõ sự liên tục dòng. Ví dụ:


![image](https://user-images.githubusercontent.com/105496635/182759893-414f3529-c7e4-4043-8cac-98dbd577001d.png)

Các lệnh được chứa bên trong các dấu ngoặc [], {}, hoặc () thì không cần sử dụng ký tự \. Ví dụ:

![image](https://user-images.githubusercontent.com/105496635/182759936-8215e0e3-3194-4443-b07e-ff867d4b9600.png)

Python chấp nhận trích dẫn đơn ('), kép (") và trích dẫn tam (''' hoặc """) để biểu thị các hằng chuỗi, miễn là các trích dẫn này có cùng kiểu mở và đóng.

Trích dẫn tam (***) được sử dụng để trải rộng chuỗi được trích dẫn qua nhiều dòng. Dưới đây là tất cả các trích dẫn hợp lệ:

![image](https://user-images.githubusercontent.com/105496635/182760045-4290a91e-3ba9-4b90-ba48-8cd5d04699e2.png)

## Comment trong Python
Python hỗ trợ hai kiểu comment đó là comment 1 dòng và nhiều dòng. Trong Python, một dấu # được sử dụng để comment đơn dòng. Tất cả ký tự ở sau dấu # và kéo dài cho đến hết dòng đó thì được coi là một comment và được bỏ qua bởi trình thông dịch. Ví dụ:

![image](https://user-images.githubusercontent.com/105496635/182760123-612a9abd-990f-4cef-aff9-733e5ace92b4.png)


Chương trình trên sẽ cho kết quả:

![image](https://user-images.githubusercontent.com/105496635/182760171-9f61cbaf-b673-48a8-a567-3777874e50e6.png)

Bạn cũng có thể gõ một comment trên cùng dòng với một lệnh hoặc biểu thức như sau:

![image](https://user-images.githubusercontent.com/105496635/182760590-47a1766e-c0b4-44ce-a3ee-678c6b1fc912.png)

Bạn có thể comment trên nhiều dòng như sau

![image](https://user-images.githubusercontent.com/105496635/182760813-dd6616dd-82e6-4325-80b1-10b1ddce27ff.png)

Python cũng hỗ trợ kiểu comment thứ hai, đó là kiểu comment đa dòng được cho bên trong các trích dẫn tam, ví dụ:

![image](https://user-images.githubusercontent.com/105496635/182760897-8d223803-503c-41ec-a78a-39f1f5fadc6b.png)

## Sử dụng dòng trống trong Python
Một dòng mà chỉ chứa các khoảng trống trắng whitespace, có thể với một comment, thì được xem như là một dòng trống và Python hoàn toàn bỏ qua nó.

Trong một phiên thông dịch trong chế độ tương tác, bạn phải nhập một dòng trống để kết thúc một lệnh đa dòng.

## Các lệnh đa dòng trên một dòng đơn trong Python
Dấu chấm phảy (;) cho phép xuất hiện nhiều lệnh trên một dòng đơn. Tất cả các lệnh được cung cấp này không bắt đầu một khối code mới. Dưới đây là ví dụ:

![image](https://user-images.githubusercontent.com/105496635/182761136-bf59a325-fc94-407c-aa92-068ce191336f.png)

Các nhóm lệnh đa dòng (còn được gọi là suite) trong Python
Một nhóm các lệnh đơn, mà tạo một khối code đơn, được gọi là suite trong Python. Các lệnh phức hợp như if, while, def, và class cần một dòng header và một suite.

Các dòng header bắt đầu lệnh (với từ khóa) và kết thúc với một dầu hai chấm (:) và được theo sau bởi một hoặc nhiều dòng để tạo nên một suite. Ví dụ như:

![image](https://user-images.githubusercontent.com/105496635/182761177-ea31f28d-403d-4557-949d-f0f31aab1677.png)


Tham số dòng lệnh trong Python
Nhiều chương trình có thể được chạy để cung cấp cho bạn một số thông tin cơ bản về cách chúng nên được chạy. Python cho bạn khả năng để làm điều này với -h:
![image](https://user-images.githubusercontent.com/105496635/182761266-32e1d454-f7d3-4c08-8b32-2aaae63650ff.png)


Bạn cũng có thể lập trình cho script của mình theo cái cách mà nó nên chấp nhận các tùy chọn khác nhau tùy theo cách bạn thiết lập. Để tìm hiểu thêm về tham số dòng lệnh, bạn có thể tham khảo bài tham số dòng lệnh trong Python. (Bạn nên tìm hiểu bài này sau khi bạn đã tìm hiểu qua về các khái niệm còn lại của Python.)

Ngoài ra, một điều cần nói đến đó là khi bạn gặp phải trường hợp chương trình hiển thị trên command line như sau:

![image](https://user-images.githubusercontent.com/105496635/182761469-96a37b2f-62e5-48b4-a109-549daf41f928.png)


Lệnh này nói rằng bạn hãy nhấn phím Enter để thoát. Ở đây, "\n\n" là để tạo hai newline (dòng mới) trước khi hiển thị dòng thực sự. Khi người dùng nhấn phím enter, thì chương trình kết thúc. Lệnh này sẽ đợi cho đến khi nào bạn thực hiện một hành động nào đó, và điều này giữ cho cửa sổ console của bạn mở tới khi bạn tiếp tục thực hiện hành động.
