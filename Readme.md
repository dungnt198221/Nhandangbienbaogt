Nhận dạng biển báo giao thông

Link dataset: https://benchmark.ini.rub.de/gtsrb_dataset.html

Link model: https://colab.research.google.com/drive/1JLsZIyooEWGB3mBsLpe2ZmmOLYI_prdG?usp=sharing

Tổng quan dataset:
 
Vấn đề phân loại một ảnh, nhiều lớp
Hơn 40 lớp học
Tổng cộng hơn 50.000 hình ảnh
Cơ sở dữ liệu lớn, sống động như thật
Dữ liệu thực tế đáng tin cậy nhờ chú thích bán tự động
Các trường hợp biển báo giao thông vật lý là duy nhất trong tập dữ liệu
(nghĩa là mỗi biển báo giao thông trong thế giới thực chỉ xuất hiện một lần)

Kết cấu dấtet:

Kho lưu trữ tập huấn luyện có cấu trúc như sau:
Một thư mục cho mỗi lớp
Mỗi thư mục chứa một tệp CSV có chú thích ("GT-<ClassID>.csv") và hình ảnh đào tạo
Hình ảnh đào tạo được nhóm theo bài hát
Mỗi rãnh chứa 30 hình ảnh của một biển báo giao thông thực tế

Định dạng hình ảnh:

Mỗi hình ảnh chứa một biển báo giao thông
Hình ảnh có đường viền 10% xung quanh biển báo giao thông thực tế (ít nhất 5 pixel) để cho phép các phương pháp tiếp cận dựa trên cạnh
Hình ảnh được lưu trữ ở định dạng PPM ( Portable Pixmap, P6 )
Kích thước hình ảnh thay đổi từ 15x15 đến 250x250 pixel
Hình ảnh không nhất thiết phải là hình vuông
Biển báo giao thông thực tế không nhất thiết phải nằm ở giữa hình ảnh. Điều này đúng với những hình ảnh gần với đường viền hình ảnh trong hình ảnh đầy đủ của camera
Hộp giới hạn của biển báo giao thông là một phần của chú thích (xem bên dưới)

Định dạng chú thích:

Chú thích được cung cấp trong tệp CSV. Các trường được phân tách bằng dấu ";" (dấu chấm phẩy). Chú thích chứa các thông tin sau:
Filename : Tên file của hình ảnh tương ứng
Chiều rộng : Chiều rộng của hình ảnh
Height : Chiều cao của hình ảnh
ROI.x1 : Tọa độ X của góc trên bên trái của hộp giới hạn biển báo giao thông
ROI.y1 : Tọa độ Y của góc trên bên trái của hộp giới hạn biển báo giao thông
ROI.x2 : Tọa độ X của góc dưới bên phải của hộp giới hạn biển báo giao thông
ROI.y2 : Tọa độ Y của góc dưới bên phải của hộp giới hạn biển báo giao thông
