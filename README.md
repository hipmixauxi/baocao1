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
