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
