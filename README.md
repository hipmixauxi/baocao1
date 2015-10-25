#I. Mô hình OSI
##1. Khái niệm
  - Mô hình OSI(Open Systems Interconnection) là mô hình tham chiếu kết nối các hệ thống mở, hay còn được gọi là mô hình tham chiếu 7 tầng OSI.
  - Mô tả cách thức truyền tin từ chương trình ứng dụng của hệ thống máy tính này sang hệ thống máy tính khác bằng các phương tiện truyền thông vật lý.

##2. Cấu trúc
  - Gồm 7 tầng, mỗi tầng đảm nhiệm 1 chức năng riêng nhưng liên kết, không tách rời nhau.
+ Tầng dười cung cấp các tính năng cho tầng trên liền kề và sử dụng các tính năng của tầng dưới liền kề nó.
  - Mỗi 1 tầng có 1 giao thức riêng, nhằm thể hiện mối quan hệ giữa 2 tầng đồng mức.
  - Các tầng được sắp xếp như sau :
+ **A**pplication Layer: Tầng ứng dụng
+ **P**resentation Layer: Tầng trình diễn
+ **S**ession Layer: Tầng phiên
+ **T**ransport Layer: Tầng vận chuyển
+ **N**etwork Layer: Tầng mạng
+ **D**ata Link Layer: Tầng liên kết dữ liệu
+ **P**hysical Layer: Tầng vật lý
+ **Cách nhớ** : *Anh Phải sống tới ngày động phòng.*

##3. Các Tầng cụ thể
###1. Physical Layer (Tầng vật lý):
  - Là lớp thấp nhất của mô hình, định nghĩa tất cả các đặt tả về điện và vạt lý cho các thiết bị.
  - Mô tả giao diện điện, quang, cơ học và hức năng tới môi trường vật lý và mang tín hiệu cho tất cả các lớp cao hơn.
  - Cung cấp các dịch vụ:
+ Mã hóa dữ liệu: chuyển đổi tín hiệu thành các bit 0 - 1, hỗ trợ đồng bộ hóa bit và khung:
	Xác định trạng thái tín hiệu đại diện 0/1
	Nhận định giới hạn khung
+ Kỹ thuật truyền: xác định bit đã mã hóa được truyền theo băng thông rộng hay phát tín hiệu dải tần số.
+ Định nghĩa cách kết nối cable với card mạng.
+ Chiều truyền tín hiệu: 1 hay 2 chiều.
  - Đơn vị dữ liệu là các bit.
  - Thuộc nhóm Media Layer.

###2. Data Link Layer (Tầng liên kết dữ liệu):
  - Cung cấp khung truyền dữ liệu không có lỗi giữa các nút trong tầng vật lý.
  - Cho phép các tầng trên thực hiện truyền ảo không lỗi trên liên kết.
+ Thiết lập và kết thúc liên kết: thiết lập và kết thúc liên kết hợp lý giữa hai nút.
+ Kiểm soát lưu lượng truy cập khung: yêu cầu nút truyền "trở lại" khi không có bộ đệm khung nào.
+ Trình tự khung: truyền/nhận khung tuần tự.
+ Báo nhận khung: cung cấp/nhận báo nhận khung.
+ Đặt giới hạn khung: tạo và nhận diện ranh giới khung.
+ Kiểm tra lỗi khung: kiểm tra khung đã nhận xem có toàn vẹn không.
+ Quản lý truy cập phương tiện: xác định khi nút "có quyền" sử dụng các phương tiện vật lý.
  - Đơn vị dữ liệu : Frames
  - Thuộc nhóm Media Layer.

###3. Network Layer (Tầng mạng):
  - Lập địa chỉ, diễn dịch địa chỉ tên logic thành địa chỉ vật lý.
  - Kiểm soát hoạt động của mạng con, quyết định đường dẫn vật lý dựa trên điều kiện mạng, mức độ ưu tiên của dịch vụ và các yếu tố khác.
+ Định tuyến: định tuyến khung trong mạng
+ Điều khiển lưu lượng mạng con
+ Phân mảnh khung
+ Ánh xạ địa chỉ vật lý logic: dịch địa chỉ hoặc tên logic thành địa chỉ vật lý
+ Tính toán việc sử dụng mạng con
  - Đơn vị dữ liệu: Packets
  _ Thuộc nhóm Media Layer

###4. Transport Layer
  - Đảm bảo gói tin được gửi thành công, theo thứ tự và không có lỗi
  - Kích thước và độ phức tạp của giao thức truyền tải phụ thuộc vào loại dịch vụ nhận được từ Network Layer
  - Cung cấp:
+ Phân đoạn gói tin: nhận gói tin từ lớp Session, chia thành các đơn vị nhỏ hơn (nếu chưa đủ nhỏ) và chuyển xuống Network Layer
+ Báo nhận tin: báo nhận từ đầu cuối đáng tin cậy
+ Kiểm soát lưu lượng tin: yêu cầu trạm tuyền gửi trả khi không có bộ đệm tin
+ Đa hợp phiên: kết hợp 1 số luồng tin hoặc phiên vào 1 liên kết logic và theo dõi
  - Transport Layer có thể chậm nhận tin tương  đối lớn nhưng có những giới hạn kích thước nghiêm ngặt do Networ Layer áp đăt
  - Đơn vị dữ liệu:Segments
  - Thuộc nhóm: Host Layer

###5. Session Layer
  - Thiết lập phiên giữa các chương trình chạy trên các trạm khác nhau.
+ Thiết lập, bảo trì và kết thúc phiên
+ Hỗ trợ phiên: thực hiện các chức năng cho phép các quy trình giao tiếp qua mạng, thực hiện bảo mật, nhận dạng tên..v..v..
  - Đơn vị dữ liệu: Data
  - Thuộc nhóm: Host Layer

###6. Presentation Layer
  - Định dạng dữ liệu dùng cho tầng ứng dụng (Application)
  - Dịch dữ liệu từ 1 định dạng do tần ứng dụng sử dụng thành định dạng phổ biến tại trạm gửi, sau đó dịch lại thành dàng quen thuộc với tầng ứng dụng tại  trạm nhận.
  - Cung cấp:
+ Dịch mã kí tự
+ Chuyển đổi dữ liệu: thứ tự bit..v.v..
+ Nén dữ liệu: giảm số lượng bit cần truyền
+ Mã hóa dữ liệu: mã hóa mật khảu...v...
  - Đơn vị dữ liệu: Data
  - Thuộc nhóm: Host Layer

###7. Application Layer
  - Đóng vai trò như cửa sổ giao  tiếp giữa người dùng và quy trình ứng dụng để tuy cập dịch vụ mạng
  - Bao gồm các chức năng cần thiết:
+ Chuyển hướng thiết bị và chia sẻ tài nguyên
+ Truy cập tệp, máy in từ xa
+ Kết nối giữa các quy trình
+ Quản lý mạng
+ Dịch vụ thư mục
+ Nhắn tin điện tử
+ Điểm đầu cuối mạng ảo
  - Đơn vị dữ liệu: Data
  - Thuộc nhóm: Host Layer


#II. TCP/IP
##1. Khái niệm
  - TCP/IP (Tranmission Control Protocol/Internet Protocol) là một bộ các giao thức truyền thông cài đặt chồng giao thức mà internet và hầu hết các mạng máy tính thương mại đang chạy trên đó.
  - Được đặt tên theo 2 giao thức chính: Điểu khiển giao vận và giao thức liên mạng
  - Được coi là 1 tập hợp các tầng, mỗi tầng giải quyết 1 vấn đề liên quan đến truyền dữ liệu. Cung cấp dịch vụ cho tầng trên và sử dụng dịch vụ của tầng dưới.

##2. Các tầng
###1. Network Access Layer
  - Có thể tách thành 2 tầng: Physical Layer và Data Link Layer trong OSI
  - Sử dừng để truyền gói tin từ tầng mạng đến các host trong mạng.
  - Thành phần: bao gồm cả các thiết bị vật lý (hun,switch,cable,card...v...)
  - Các giao thức:
+ Ethernet: định nghĩa 1 loạt các chuẩn nối dây và phát tín hiệu cho tầng vật lý, 2 phương tiện truy cập mạng tại phần địa chỉ MAC và 1 định dạng chung cho việc đánh địa chỉ.
+ XDSL:kỹ thuật truyền thông điện tử qua đường điện thoại với tốc độ cao. Có thể vận chuyển cùng lúc 2 loại tín hiệu data và voice.
+ PPP-EAP
  - Đơn vị dữ liệu: Frames
  - Thuộc nhóm: Networks

###2. Internet Layer
  - Giải quyết các vấn đề truyền dẫn gói tin đi qua các mạng đến đúng đích.
  - Các giao thức:
+ IP: là giao thức hướng dữ liệu được sử dụng bởi các máy chủ nguồn và đích để truyền dữ liệu trong một liên mạng chuyển mạch gói
+ ICMP: giúp kiểm tra các kết nối 3 lớp có được thông hay không
+ ARP: phân giải địa chỉ động
+ DHCP: cấu hình tự động địa chỉ IP
  - Đơn vị dữ liệu: Packets
  - Thuộc nhóm: Networks

###3. Transport
  - Phân nhỏ các gói tin có kích thước lớn khi gửi và tập hợp khi nhận, đảm bảo toàn vẹn cho dữ liệu
  - Các giao thức:
+ TCP: có thể tạo kết nối giữa các máy chủ đc kết nối mạng, đảmm bảo truyền dữ liệu đến nơi đáng tin cậy và đúng thứ tự.
+ UDP: gửi những dữ liệu ngắn đến máy khác, không cung cấp tin cậy nhưng nhanh và hiệu quả hơn vs các mục tiêu nhỏ.
  - Đơn vị dữ liệu:Segments
  - Thuộc nhóm: Protocols

###4. Application
  - Nơi các chương trình mạng làm việc để liên lạc giữa các node mạng.
  - Bao gồm cả chức năng của Presentation và Session trong OSI
  - Các giao thức:
+ POP:  Post Office Protocol - giao thức email
+ DNS:Domain Name System - hệ thống tên  miền
+ HTTP:HyperText Transfer Protocol - giao thức truyền tải siêu văn bản
*Tạo ra phương thức cho trình duyệt web (browser) truy nhập tới máy phục vụ web và yêu cầu các tài liệu đa phương tiện (được tạo bởi ngôn ngữ đánh dấu siêu văn bản HTML) như văn bản, ảnh, âm thanh, hình ảnh động, phim số hoá.... Giao thức này là giao thức không lưu giữ trạng thái (stateless protocol), cổng tiêu chuẩn cho HTTP trên máy phục vụ web là 80 và có thể được xác định lại khi thiết lập cấu hình cho máy phục vụ web*
*Khi một máy trạm gửi một yêu cầu một trang web trên website (sử dụng HTTP) thông qua địa chỉ tên của website, đầu tiên là việc phân giải ngược địa chỉ tên website thành địa chỉ IP nhờ máy chủ DNS. Sau đó là quá trình bắt tay ba bước, khởi tạo kết nối lớp TCP giữa máy trạm và máy phục vụ web, hình thành kết nối lớp ứng dụng giữa máy trạm và máy phục vụ web. Máy trạm gửi yêu cầu trang web và máy phục vụ web phản hồi, gửi trả kết quả về máy trạm. Cuối cùng là tiến trình đóng kết nối lớp ứng dụng giữa máy trạm và máy phục vụ web, đóng kết nối lớp TCP.*
+ FTP: File Transfer Protocol - giao thức truyền tệp
*Dùng để truyền tập dữ liệu từ máy tính này sang máy tính khác. Các tập tin có thể ở dạng văn bản ASCII, tập tin nhị phân thực thi được...Mục tiêu chính của FTP là khuyến khích việc chia sẻ tài nguyên (dữ liệu, chương trình), truyền dữ liệu có hiệu quả và tin cậy. Có thể khai thác FTP theo hai chế độ: User FTP (cần có tài khoản riêng) và Anonymous FTP (không cần tài khoản riêng), có thể quy định quyền truy nhập của người sử dụng với từng thư mục, từng tệp dữ liệu, giới hạn số kết nối đồng thời tới cùng một nơi lưu trữ dữ liệu. Cổng tiêu chuẩn dành cho FTP hoạt động trên máy chủ là 20 và 21, trong đó cổng 20 dành cho kết nối truyền dữ liệu, cổng 21 dành cho kết nối điều khiển*
*Đầu tiên là tiến trình bắt tay ba bước, khởi tạo kết nối điều khiển (control connection) lớp TCP giữa máy trạm và máy phục vụ FTP. Sau đó là tiến trình xác thực FTP máy trạm, nếu có yêu cầu truyền dữ liệu, kết nối truyền dữ liệu (data connection) được hình thành. Tiếp theo là tiến trình truyền dữ liệu và cuối cùng là tiến trình đóng kết nối truyền dữ liệu. Kết nối điều khiển chỉ bị ngắt bỏ khi kết thúc phiên làm việc của FTP (lệnh QUIT)*
+ SMTP: Simple Mail Transfer Protocol - Giao thức truyền tải thư tín đơn giản
*Một hệ thống thư điện tử được chia làm hai phần UA (User Agent) và MTA (Message Transfer Agent). UA tương tác trực tiếp với người dùng cuối. MTA dùng để định tuyến thông điệp và gửi thông điệp. Giao thức truyền thư đơn giản SMTP (Simple Mail Transfer Protocol)  là một trong những giao thức khá phổ biến trong các hệ thống thư điện tử. SMTP hoạt động dựa trên TCP/IP, theo mô hình lưu giữ và chuyển tiếp (store and forward) thông điệp giữa các MTA hoạt động theo SMTP. Các máy chủ SMTP này làm chức năng nhận thông điệp, quyết định việc định tuyến thông điệp  sao cho các thông điệp đến được đúng hệ thống đích*
*Trước các tiến trình gửi nhận là tiến trình bắt tay ba bước của TCP giữa SMTP gửi và SMTP nhận, thiết lập kết nối TCP. Đây là kết nối song công toàn phần (full duplex connection) dùng để truyền điều khiển cùng với dữ liệu. Tiếp theo là tiến trình xác thực,  SMTP gửi/nhận các lệnh điều khiển, xử lý các phản hồi, và dữ liệu. Cuối cùng, kết nối  TCP bị ngắt bỏ khi SMTP phát  lệnh QUIT. Số hiệu cổng tiêu chuẩn SMTP trên máy chủ nhận là 25*
+ Telnet: TErminaL NETwork - thường cung cấp những phiên giao dịch đăng nhập giữa các áy tính trên mạng, dùng dòng lệnh có tính định hướng người dùng.
*mô phỏng thiết bị đầu cuối, thường được dùng để cung cấp truy cập từ xa tới máy chủ và các thiết bị mạng*
 
