1. VẤN ĐỀ LÀ GÌ?

- **Trang portal.greenlog.vn tải chậm, mất 20 giây mới hiển thị đầy đủ. Hình ảnh bản đồ không xuất hiện dù mạng vẫn ổn định, có thể do lỗi tải tài nguyên hoặc hình ảnh quá nặng.**

2. YÊU CẦU LÀ GÌ?

- **Sử dụng tab Network để phân tích thời gian tải, tìm lỗi 404, xác định tài nguyên dung lượng lớn và đề xuất cách tối ưu tốc độ trang web.**

3. CÁCH LÀM:

- Phần 1. Phân tích:

+ Nhấn F12 → chọn tab Network → tích Disable Cache → tải lại trang.
+ Quan sát biểu đồ Waterfall để xác định tài nguyên tải lâu nhất.
+ Kiểm tra các Request màu đỏ có mã 404 để tìm file bị thiếu.
+ Kiểm tra kích thước hình ảnh và thời gian tải để tìm nguyên nhân gây chậm.
+ Đây là những nút thắt cổ chai khiến trang web mất nhiều thời gian tải.

- Phần 2. Triển khai:

Thực hiện 3 bước tối ưu:
+ Bước 1: Sửa lỗi 404 bằng cách kiểm tra và sửa lại đường dẫn tài nguyên bị thiếu.
+ Bước 2: Nén hình ảnh, sử dụng định dạng WebP để giảm dung lượng và tăng tốc độ tải bản đồ.
+ Bước 3: Bật Browser Cache để lưu CSS, JavaScript và hình ảnh tĩnh, giúp trình duyệt không phải tải lại toàn bộ tài nguyên mỗi lần truy cập.

Đảm bảo các file CSS và JavaScript quan trọng được tải thành công với mã 200 OK trước khi giao diện hiển thị hoàn chỉnh.

- Phần 3. Kiểm thử:

Khi tải lại trang nhận mã 304 Not Modified:
+ Đây là tín hiệu tốt, cho biết tài nguyên không thay đổi so với phiên bản đã lưu trong Cache.
+ Trình duyệt có thể sử dụng lại tài nguyên cũ thay vì tải lại toàn bộ file.
+ Nhờ đó giảm lượng dữ liệu truyền qua mạng, tiết kiệm băng thông và giúp trang web tải nhanh hơn.

