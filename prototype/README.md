# Prototype Trợ lý buổi 3

**Phụ trách:** Nguyen Quoc Hung · 2A202603553.

## Chạy
Mở `index.html` trong Chrome, Edge hoặc Firefox. File gồm toàn bộ HTML, CSS, JavaScript và dữ liệu cần dùng; không tải font hay thư viện bên ngoài. Không cần API key. Có thể phục vụ thư mục repo bằng `python -m http.server 8000` và mở `http://localhost:8000/prototype/` nếu trình duyệt hạn chế mở file trực tiếp.

## Luồng S06
1. Chọn S06; đọc nhãn Cần rà soát và phản ví dụ kiểm tra.
2. Bấm Xem mục nguồn để thấy câu gốc §3.3 và cảnh báo về nguồn.
3. Bấm Nhờ TA hỗ trợ. Lúc này hàng chờ vẫn 0; Huỷ bản xem trước không tạo yêu cầu.
4. Xác nhận chuyển TA. Hàng chờ tăng, hiện mã TA-001 và trạng thái chờ; ngoài giờ không có cam kết trả lời ngay.
5. Sang Hàng chờ TA; đổi mốc giờ bằng nút phía trên nếu mô phỏng ca làm việc buổi sáng. Bấm Nhận xử lý.
6. Nút Duyệt và đăng FAQ vẫn bị khoá đến khi TA tích xác nhận kiểm nguồn. Bản nháp là ghi chú cần rà soát, không tự khẳng định tài liệu đã sửa.
7. Sau khi duyệt và đăng, FAQ mới xuất hiện; màn hình học viên cũng thấy trạng thái phản hồi của yêu cầu.

## Luồng S04
1. Chọn S04. Thấy hạn từ trang khoá học và chỉ một gợi ý bước đầu.
2. Ẩn gợi ý, rồi Hiện lại gợi ý; không có nút xem đáp án.
3. Có thể xác nhận chuyển TA để hỏi thêm. Tại màn hình TA, nội dung bài đang mở vẫn không được đăng FAQ; hộp kiểm và nút đăng bị khoá.
4. Nhập câu xin xác nhận đáp số bài 3; bản mẫu giữ giới hạn, không trả lời đúng/sai về con số.

## Các nhánh khác
S01 giải thích có nguồn; S02 hỏi lại; S03 không tạo slide; S11 giải thích bài đã hết hạn. Ô câu hỏi tiếp nhận các biến thể đã có nhánh và đưa câu chưa nhận diện vào hỏi lại. Báo câu trả lời sai cho phép sửa câu hỏi rồi chạy lại nhánh. Yêu cầu đã xếp hàng có thể rút trước khi TA nhận; yêu cầu trùng đang chờ không tạo thêm bản ghi.

## Ảnh đánh số
- `01-hoc-vien.jpg`: 1 nguồn và G11; 2 giới hạn và G10; 3 sửa và G9; 4 xác nhận chuyển TA.
- `02-hang-cho-ta.jpg`: 5 cổng duyệt FAQ; 6 FAQ vẫn chưa xuất bản khi chưa duyệt. Ảnh tập trung vào phần chi tiết cổng duyệt.

## Dữ liệu và giới hạn
Nội dung A/B của track được đưa vào file, bao gồm nguyên văn mệnh đề cần rà soát ở §3.3. Phản ví dụ 0,25 → 0,5 là phép kiểm toán học do nhóm dựng. Không có dịch vụ gửi tin, không kết nối TA, không sửa tài liệu hay gia hạn thật. Dữ liệu phiên lưu cục bộ nếu localStorage khả dụng; không dùng dữ liệu cá nhân thật.

Đây là bộ phản hồi mô phỏng có luật chọn nhánh, không phải agent hoặc model đang chạy. Vai TA không có bảo vệ phía máy chủ. Nếu sửa JavaScript bằng công cụ phát triển thì có thể thay đổi mô phỏng; cổng duyệt thể hiện thiết kế quyền, không được xem là cơ chế bảo mật sản phẩm thật.

Kết quả kiểm tra: `kiem-thu.md` và `qa_results.json`. Bản mẫu không đáp ứng phần bonus lời gọi AI thật.
