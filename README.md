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
###1.

 
