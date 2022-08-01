# Các giao thức chính

#  *Giao thức Http & Https:
I,Giao thức HTTP – Port 80 & giao thức HTTPS – Port 443
   1. Giao thức http- port 80:
-Giao thức HTTP viết tắt của Hybertext Transfer Protocol (HTTP). Đây là giao thức nền tảng của Word Wide Web. Giao thức HTTP được sử dụng để tải 
nội dung của một website từ server chứa website đó đến máy của bạn.
-Giao thức HTTP sử dụng mô hình client-server và sử dụng giao thức TCP.
Giao thức HTTP sử dụng 2 phương thức truy vấn dữ liệu sau để giao tiếp với server:
    + GET request: Get request được dùng để yêu cầu hoặc truy vấn dữ liệu từ một nguồn xác định nào đó. Ví dụ như khi bạn truy cập vào trang
    + Post request: Post request được dùng để gửi thông tin mà bạn đã nhập đến web server để sử lý. Ví dụ khi bạn nhập mật khẩu và password vào trang đăng nhập Facebook và bấm đăng nhập, bạn đang gửi một Post request đến server của Facebook đi kèm theo username và password của của bạn để Facebook xác thực tài khoản.
-Khi bạn gửi truy vấn đến một server chứa website nào đó, bạn sẽ nhận lại một HTTP response, có thể được hiểu như phản hồi của server về yêu cầu mà bạn đã gửi đến.
  *Một HTTP response sẽ bao gồm những phần sau: (HTTP status code,HTTP response header.HTTP body (optional))
 
 Trong đó HTTP status code, sẽ cho biết là liệu HTTP request có được đáp ứng hay không. HTTP status code có dạng một dãy có 3 chữ số như sau:

 -1xx Hiển thị thông tin
 -2xx Báo hiệu yêu cầu đã được đáp ứng thành công
 -3xx Báo hiệu request đã được chuyển hướng sang một địa chỉ server khác
 -4xx Lỗi do client
 -5xx Lỗi do server
 -Giá trị xx sẽ chạy từ 00 đến 99.
 HTTP response header, sẽ cho biết những thông tin quan trọng như ngôn ngữ (ở đây là HTML) và định dạng dữ liệu nào được gửi ở phần HTTP body, status code, ngày giờ dữ liệu được gửi, v.v.

HTTP response body, sẽ là phần nội dung mà bạn yêu cầu. Đương nhiên nếu server gặp lỗi, không phản hồi thì HTTP response sẽ không có phần này.

Giao thức HTTP có một điểm yếu chết người đó là dữ liệu được truyền qua HTTP sẽ không được mã hóa mà ở dạng chữ người thường có thể đọc được. Dẫn đến khả năng bị lộ thông tin mật khẩu rất cao.

2. Giao thức https- port 443
-Giao thức HTTPS viết tắt của Hypertext Transfer Protocol Secure. HTTPS cũng được dùng để trao đổi dữ liệu giữa client và server, tuy nhiên HTTPS sẽ mã hóa toàn bộ thông tin trước khi được truyền đi, làm giảm thiểu việc lộ thông tin nhạy cảm.

-HTTPS sử dụng một giao thức được gọi là Transport Layer Security (TLS) hay trước đây còn được gọi là Secure Sockets Layer (SSL) để mã hóa đường truyền
-Giao thức truyền siêu văn bản an toàn (HTTPS) là phiên bản bảo mật của HTTP , là giao thức chính được sử dụng để gửi dữ liệu giữa trình duyệt web và trang web. HTTPS được mã hóa để tăng tính bảo mật khi truyền dữ liệu. Điều này đặc biệt quan trọng khi người dùng truyền dữ liệu nhạy cảm, chẳng hạn như bằng cách đăng nhập vào tài khoản ngân hàng, dịch vụ email hoặc nhà cung cấp bảo hiểm sức khỏe.

- Bất kỳ trang web nào, đặc biệt là những trang web yêu cầu thông tin đăng nhập, nên sử dụng HTTPS. Trong các trình duyệt web hiện đại như  Chrome, các trang web không sử dụng HTTPS được đánh dấu khác với các trang web đó. Tìm ổ khóa màu xanh lá cây trong thanh URL để biểu thị trang  web được bảo mật. Các trình duyệt web coi trọng HTTPS;
    *HTTPS hoạt động như thế nào?
HTTPS sử dụng một giao thức mã hóa để mã hóa thông tin liên lạc. Giao thức được gọi là Bảo mật lớp truyền tải (TLS) , mặc dù trước đây nó được gọi là Lớp cổng bảo mật (SSL) . Giao thức này bảo mật thông tin liên lạc bằng cách sử dụng cơ sở hạ tầng khóa công khai bất đối xứng . Loại hệ thống bảo mật này sử dụng hai khóa khác nhau để mã hóa thông tin liên lạc giữa hai bên:

Khóa riêng tư - khóa này được kiểm soát bởi chủ sở hữu của một trang web và nó được giữ, như người đọc có thể đã suy đoán, là riêng tư. Khóa này nằm trên máy chủ web và được sử dụng để giải mã thông tin được mã hóa bởi khóa công khai.
Khóa công khai - khóa này khả dụng cho tất cả những ai muốn tương tác với máy chủ theo cách an toàn. Thông tin được mã hóa bằng khóa công khai chỉ có thể được giải mã bằng khóa riêng. 


II, Giao thức FTP – Port 20, 21
 - Giao thức FTP viết tắt của File Transfer Protocol. Giao thức FTP được dùng để trao đổi file giữa 1 client và 1 server. Hay nói cách khác, FTP sẽ cho phép các máy trong cùng một mạng có thể trao đổi file dữ liệu qua lại với nhau thông qua một server trung gian.
     Một cách tóm tắt thì FTP sẽ hoạt động như sau:
        1. Bạn sẽ được cấp cho một tài khoản với username và password để từ máy của bạn (client) kết nối đến máy chủ đang chạy FTP (server).
        2. Bạn sẽ dùng username và password được cấp để đăng nhập vào server FTP.
        3. Server FTP làm nhiệm vụ xác thực username và password của bạn, nếu hợp lệ sẽ cho phép bạn truy cập vào server FTP cũng lưu trữ các file dữ liệu.
        4. Sau khi đã đăng nhập, bạn có quyền tải file dữ liệu của mình lên FTP server để chia sẻ cho mọi người dùng trong mạng, hoặc download dữ liệu từ FTP server xuống máy của bạn.     

Ví dụ bạn muốn chuyển dữ liệu cho bạn Nguyễn Thi A bằng giao thức FTP. Cả hai bạn đều có quyền truy cập vào FTP server. Bạn sẽ làm như sau:

Dùng tài khoản được cấp của bạn tải file lên FTP server
Gọi điện hoặc nhắn tin cho bạn A biết file hiện đang lưu trữ tại FTP server
Bạn A sẽ đăng nhập vào FTP server để tải file về máy mình
Giao thức FTP sử dụng giao thức TCP. Để thực hiện việc trao đổi dữ liệu, 2 đường truyền TCP sẽ đuwọc sử dụng song song. Một đường truyền dùng cho việc quản lý và một dành cho dữ liệu.

Đường truyền quản lý (port 21) sẽ được dùng để gửi username và password từ máy client đến server, nhận lệnh từ máy client (ví dụ như lệnh download file, upload file), v.v.

Đường truyền dữ liệu (port 20) sẽ được dùng để client có thể gửi file từ máy mình đến và lưu trữ file tại máy chủ server.

FTP có một account đặc biệt với usernam và password đều là anonymous. Account này được coi như là một public account mà ai cũng có thể vào được, được dùng để chia sẻ file dữ liệu với những cá nhân không được cấp tài khoản FTP. Tuy nhiên, nếu không được quản lý cẩn thận, account này hoàn toàn có thể được sử dụng để gửi và thực thi mã độc.

Trên Linux, bạn có thể dùng lệnh sau để kết nối đến FTP server.
ftp <IP-address> <port>  
hoặc 
nc <IP-address> <port> 

III,Giao thức SSH – Port 22
-Giao thức SSH viết tắt của Secure Shell. SSH là một giao thức dùng cho phép bạn truy cập máy chủ từ xa với đường truyền được mã hóa nhằm bảo vệ thông tin được truyền đi.

-Không chỉ dùng để kết nối đến máy chủ, SSH còn cho phép bạn thực thi mệnh lệnh và truy cập từ xa vào các hệ thống mạng, thiết bị và ứng dụng nằm trong mạng nội bộ của công ty.

-Thực thi mệnh lệnh từ xa là sao? Nghĩa là từ nhà bạn, thông qua giao thức SSH, bạn hoàn toàn có thể ra lệnh tắt máy, ra lệnh cho máy chạy một tác vụ nào đó v.v. Hay nói cách khác, SSH cho phép bạn gần như nằm toàn bộ hoặc một phần quyền điều khiển máy chủ/thiết bị đó.  
SSH thường được cấp cho những người làm quản trị viên hệ thống, cho phép họ có thể truy cập hệ thống công ty từ nhà.

-SSH sử dụng mô hình client-server với server là máy chủ và client là thiết bị cá nhân của người có nhu cầu cần kết nối đến máy chủ. Để truy cập vào server SSH, bạn cần phải được cấp một username và password.

-Ở giai đoạn 4, sẽ có 1 máy chúng ta sẽ thực hành hack giao thức SSH, đến lúc đó mình sẽ nói sâu hơn các thành phần dùng để xác thực người dùng trên SSH nhé.
ssh <IP-address>/<host>  
hoặc
ssh username@<IP-address>/<host>

IV, Bộ giao thức ARP
1. ARP là gì? Mục đích và cách thức hoạt động của ARP
  - ARP (viết tắt của cụm từ Address Resolution Protocol) là giao thức mạng được dùng để tìm ra địa chỉ phần cứng (địa chỉ MAC) của thiết bị từ một địa chỉ IP nguồn. Nó được sử dụng khi một thiết bị giao tiếp với các thiết bị khác dựa trên nền tảng local network. Ví dụ như trên mạng Ethernet mà hệ thống yêu cầu địa chỉ vật lý trước khi thực hiện gửi packets. 
  - Thiết bị gửi sử dụng ARP để có thể dịch địa chỉ IP sang địa chỉ MAC. Thiết bị sẽ gửi một request ARP đã chứa địa chỉ IP của thiết bị nhận. Tất cả thiết bị trên đoạn local network sẽ nhìn thấy thông điệp này. Tuy nhiên, chỉ thiết bị có địa chỉ IP chứa trong request mới có thể phản hồi lại với thông điệp mà chứa địa chỉ MAC của nó. Thiết bị gửi khi đó sẽ có đầy đủ các thông tin để gửi packet tới thiết bị nhận.

2. Lịch sử và mục đích của ARP
- ARP được hình thành và phát triển vào đầu những năm 1980 như một giao thức dịch địa chỉ chung cho các mạng IP. Bên cạnh Ethernet và WiFi thì ARP đã được triển khai cho ATM, Token Ring và cả những loại mạng vật lý khác.

- ARP cho phép một mạng quản lý các kết nối độc lập với những thiết bị vật lý cụ thể được gắn vào từng mạng. Điều này cho phép giao thức Internet vận hành hiệu quả hơn so với việc nó phải tự quản lý địa chỉ của các thiết bị phần cứng và mạng vật lý.

3. Cơ chế hoạt động của ARP
- Quá trình hoạt động của ARP được bắt đầu khi một thiết bị nguồn trong một mạng IP có nhu cầu thực hiện gửi một gói tin IP. Trước hết thiết bị đó phải xác định được xem địa chỉ IP đích của gói tin có phải đang nằm cùng trong mạng nội bộ của mình hay không. Nếu đúng vậy thì thiết bị sẽ thực hiện gửi trực tiếp gói tin đến thiết bị đích. Nếu địa chỉ IP đích đang  nằm trên mạng khác, thì thiết bị sẽ gửi gói tin đến một trong các router nằm cùng ở trên mạng nội bộ để router này làm nhiệm vụ forward gói tin.
- Cả hai trường hợp, bạn đều thấy được là thiết bị phải gởi gói tin IP đến một thiết bị IP khác trên cùng mạng nội bộ. Chúng ta biết rằng việc gửi gói tin trong cùng mạng thông qua Switch là dựa vào địa chỉ MAC hay là địa chỉ phần cứng của thiết bị. Sau khi gói tin được đóng gói thì hệ thống mới bắt đầu được chuyển qua quá trình phân giải địa chỉ ARP và thực hiện chuyển đi.

- ARP về cơ bản là một quá trình có 2 chiều request/response giữa các thiết bị trong cùng mạng nội bộ. Thiết bị nguồn request bằng cách gửi một bản tin local broadcast  lên trên toàn mạng. Thiết bị đích response bằng một bản tin unicast để trả lại cho thiết bị nguồn.

 4. Các loại bản tin ARP
 - Có hai dạng bản tin trong ARP cơ bản nhất: một là được gửi từ nguồn đến đích, còn một là được gửi từ đích tới nguồn.
   + Request: Khi hệ thống khởi tạo quá trình, gói tin được gửi từ máy nguồn tới thiết bị đích

   + Reply: Khi quá trình đáp trả gói tin ARP request, được gửi từ thiết bị đích đến máy nguồn
 - Có 4 loại địa chỉ nằm trong một bản tin ARP  đó là:

    + Sender Hardware Address: Đây là địa chỉ lớp hai của thiết bị gửi bản tin

    + Sender Protocol Address: Đây là địa chỉ lớp ba (hay còn gọi là địa chỉ logic) của thiết bị gửi bản tin

    + Target Hardware Address: Địa chỉ lớp hai (hay còn được gọi là địa chỉ phần cứng) của thiết bị đích của bản tin

    + Target Protocol Address: Địa chỉ lớp ba (hay gọi là  địa chỉ logic) của thiết bị đích của bản tin


V, Hệ thống DNS
    - Hệ thống DNS viết tắt của Domain Name System. Đây là một hệ thống có nhiệm vụ dịch từ tên miền ra địa chỉ IP được dùng để gán cho tên miền đó.
    -  Địa chỉ IPv4 hoặc IPv6 rất khó nhớ đối với người dùng thông thường. Nên thay vì bắt họ phải nhớ một dãi số để truy cập một website, để cho họ nhớ một chuỗi ký tự có nghĩa và dễ nhớ. Nên dns đã ra đời để thay thế chuỗi đó
    - Có thể xem DNS giống như một cuốn danh bạ điện thoại vậy. Thay vì lưu giữ tên công ty với số điện thoại tương ứng, DNS sẽ lưu giữ tên miền (ví dụ tuhocnetworksecurity) với địa chỉ IP tương ứng.
    - Các bạn có thể thử check địa chỉ IP ứng với tên miền bằng câu lệnh sau trên Kali Linux:
                   vincent@kali:~$ nslookup 
> google.com
Server:     64.59.135.143
Address:    64.59.135.143#53
 
Non-authoritative answer:
Name:   google.com
Address: 172.217.14.206
Name:   google.com
Address: 2607:f8b0:400a:801::200e

VI, DHCP là gì?
1. DHCP là gì?
    - DHCP được viết tắt từ cụm từ Dynamic Host Configuration Protocol (có nghĩa là Giao thức cấu hình máy chủ). DHCP có nhiệm vụ giúp quản lý nhanh, tự động và tập trung việc phân phối địa chỉ IP bên trong một mạng. Ngoài ra DHCP còn giúp đưa thông tin đến các thiết bị hợp lý hơn cũng như việc cấu hình subnet mask hay cổng mặc định.

2. Cách thức hoạt động của DHCP
    - Được giải thích một cách ngắn gọn nhất về cách thức hoạt động của DHCP chính là khi một thiết bị yêu cầu địa chỉ IP từ một router thì ngay sau đó router sẽ gán một địa chỉ IP khả dụng cho phép thiết bị đó có thể giao tiếp trên mạng.

- Như ở các hộ gia đình hay các doanh nghiệp nhỏ thì router sẽ hoạt động như một máy chủ DHCP nhưng ở các mạng lớn hơn thì DHCP như một máy chỉ ở vai trò là máy tính.

- Cách thức hoạt động của DHCP còn được giải thích ở một cách khác thì khi một thiết bị muốn kết nối với mạng thì nó sẽ gửi một yêu cầu tới máy chủ, yêu cầu này gọi là DHCP DISCOVER. Sau khi yêu cầu này đến máy chủ DHCP thì ngay tại đó máy chủ sẽ tìm một địa chỉ IP có thể sử dụng trên thiết bị đó tồi cung cấp cho thiết bị địa chỉ cùng với gói DHCPOFFER

- Khi nhận được IP thì thiết bị tiếp tục phản hồi lại máy chủ DHCP gói mang tên DHCPREQUEST. Lúc này là lúc chấp nhận yêu cầu thì máy chủ sẽ gửi tin báo nhận (ACK) để xác định thiết bị đó đã có IP, đồng thời xác định rõ thời gian sử dụng IP vừa cấp đến khi có địa chỉ IP mới.


3. Những ưu và nhược điểm khi sử dụng DHCP
  *Ưu điểm của DHCP
     - Máy tính hay bất cứ thiết bị nào phải cấu hình đúng cách thì mới có thể kết nối với mạng được. DHCP cho phép cấu hình tự động nên dễ dàng cho các thiết bị máy tính, điện thoại, các thiết bị thông minh khác...có thể kết nối mạng nhanh.

     - Vì DHCP thực hiện theo kiểu gán địa chỉ IP nên sẽ không xảy ra trường hợp trùng địa chỉ IP, vậy việc gán theo cách thủ công của IP tĩnh sẽ dễ dàng hơn và giúp hệ thống mạng luôn hoạt động ổn định.

     - DHCP giúp quản lý mạng mạnh hơn vì các cài đặt mặc định và thiết lập tự động lấy địa chỉ sẽ cho mọi thiết bị kết nối mạng đều có thể nhận được địa chỉ IP.

     - DHCP quản lý cả địa chỉ IP và các tham số TCP/IP trên cùng một màn hình như vậy sẽ dễ dàng theo dõi các thông số và quản lý chúng qua các trạm.

     - Khi đánh tự động nhờ máy chủ DHCP giúp cho người quản lý quản lý có khoa học hơn và không bị nhầm lẫn.

     - Ngoài ra người quản lý có thể thay đổi cấu hình và thông số của các địa chỉ IP giúp việc nâng cấp cơ sở hạ tầng được dễ dàng hơn.

     - Một ưu điểm nữa là các thiết bị có thể di chuyển tự do từ mạng này sang mạng khác và nhận địa chỉ IP tự động mới vì các thiết bị này có thể tự nhận IP.
     Nhược điểm của DHCP
    * Nhược điểm DHCP
    - DHCP mang lại nhiều ưu điểm, song bên cạnh đó cũng còn mặt hạn chế. Chẳng hạn  như việc ta không nên sử dụng địa chỉ IP động, địa chỉ IP thay đổi đối với các thiết bị cố định và cần truy cập liên tục. Ví dụ như không nên sử dụng IP động cho các thiết bị máy in ở các văn phòng.

    - Mặc dù có rất nhiều lợi ích khi sử dụng DHCP, vẫn có một số hạn chế mà chúng ta cần lưu ý. Không nên sử dụng địa chỉ IP động, địa chỉ IP thay đổi đối với các thiết bị cố định và cần truy cập liên tục như máy in và file server.

    - Bởi DHCP sử dụng chủ yếu với các hộ gia đình hay văn phòng. Đối với các thiết bị dùng trong văn phòng, như máy in thì việc việc gán chúng với các địa chỉ IP thay đổi không mang tính thực tiễn. Lúc đó mỗi khi kết nối với máy tính khác thì máy in đó sẽ phải thường xuyên cập nhật cài đặt để máy tính có thể kết nối với máy in.
    - Cũng giống như việc bạn điều khiến máy tính từ xa và cần có quyền truy cập thì bạn phải có địa chỉ IP. Nếu như địa chỉ IP đó động thì những gì máy tính đã ghi lại sẽ không chính xác được lâu. Vậy nên nếu trong trường hợp này thì bạn nên sử dụng IP tĩnh là phù hợp hơn cả.

VII, Giao thức SNMP
1. SNMP là gì?
- SNMP (Simple Network Management Protocol) là một giao thức tầng ứng dụng được Hội đồng Kiến trúc Internet (IAB) xác định trong RFC1157 để trao đổi thông tin quản lý giữa các thiết bị mạng. Nó là một phần của Transmission Control Protocol/Internet Protocol (TCP/IP).
2. SNMP Manager
- Trình quản lý hoặc hệ thống quản lý là một thực thể riêng biệt có trách nhiệm giao tiếp với các thiết bị mạng được triển khai SNMP agent. Đây thường là một máy tính được sử dụng để chạy một hoặc nhiều hệ thống quản lý mạng.
- Các chức năng chính của SNMP manager:
 + Agent truy vấn
 + Nhận response từ các agent
 + Đặt các biến trong agent
 + Xác nhận các sự kiện không đồng bộ từ các agent


