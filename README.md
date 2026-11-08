Các tính năng đã được tích hợp
1. Progressive Web App (PWA) — Cài đặt như App & Chế độ Toàn màn hình Offline
	Nút Cài App trên thanh Header (btnInstallPWAHeader) & hộp thoại pwaInstallModal: 
	Hỗ trợ hộp thoại cài đặt gốc (beforeinstallprompt) trên Android / Chrome / Edge PC và hướng dẫn thêm ra Màn hình chính trên iPhone/iPad (Safari).
	Nút Bật Toàn Màn Hình (Fullscreen App Mode): Ẩn toàn bộ thanh công cụ trình duyệt để trình chiếu bài giảng Chuyên đề Vật lí 10 trên lớp học rộng 100% màn hình.
	Tự động lưu cài đặt (LocalStorage) (saveUserPreferences): Tự động ghi nhớ tọa độ trường/địa điểm quan sát (như THPT Hương Thủy) và trạng thái bật/tắt các lớp bản đồ cho những lần mở sau.
	Bộ tệp chuẩn PWA để chạy Offline 100% khi đưa lên host: 
	index.html
	manifest.json
	sw.js (Service Worker lưu đệm Offline)
	icon.svg (Biểu tượng App Kỳ Đài Huế & Trăng Sao)
2. Tự động xoay bầu trời theo cảm biến La bàn & Con quay hồi chuyển 3D (La bàn AR)
	Nút La bàn AR trên thanh điều hướng hướng nhìn (btnGyroARMode) và trên thanh công cụ dưới cùng (btnGyroBottomDock) — hoặc nhấn phím tắt R: 
	Toán học ma trận xoay 3D không bị khóa trục (Gimbal-lock free) (computeSkyAnglesFromDeviceEuler): Khi học sinh giơ điện thoại ngang tầm mắt sẽ nhìn chân trời Huế (0°), ngửa dần điện thoại lên đỉnh đầu sẽ nhìn thẳng lên Thiên đỉnh (+90°), xoay người 360° sẽ quét qua Bắc (Kỳ Đài), Đông (Cầu Trường Tiền), Nam (Núi Ngự Bình), Tây (Chùa Thiên Mụ).
	Tương thích cả iOS 13+ & Android (toggleGyroARMode): Tự động xin quyền cảm biến DeviceOrientationEvent.requestPermission() trên iPhone/iPad và lọc mượt 60 FPS.
	Hiệu chuẩn nhanh & Mô phỏng trên Máy tính: Có nút Chuẩn hướng Bắc (hoặc vuốt nhẹ trên màn hình) để bù độ lệch từ trường của điện thoại; khi mở trên máy tính không có cảm biến sẽ hiện Kính ngắm AR kèm thanh trượt Góc ngẩng máy để giáo viên minh họa trực quan trên màn chiếu.
4. Studio Chụp & Xuất Ảnh Bầu Trời Huế (Chụp ảnh)
	Nút Chụp ảnh trên Header (btnSnapshotHeader) và ở thanh công cụ dưới (btnSnapshotBottomDock) — hoặc nhấn phím tắt P: 
	Kết xuất ảnh PNG độ phân giải cao (generateAnnotatedSkySnapshot) kèm hiệu ứng màn trập máy ảnh.
	Tự động đóng dấu Khung thông tin Thiên văn Huế: Hiển thị tên trường/lớp ("Chuyên đề Vật lí 10 • Tổ Vật Lí-CN - THPT Hương Thủy - TP. Huế" — cho phép học sinh sửa ghi chú tên mình trực tiếp), tọa độ (ϕⓜ,λ), giờ Huế (UTC+7), Giờ Sao Địa Phương (LST) và hướng nhìn.
	Đính kèm Thẻ Thiên thể đang chọn: Nếu đang bấm chọn một ngôi sao hay hành tinh (VD: Sao Mộc, Sao Bắc Cực, Tinh vân Lạp Hộ), ảnh chụp sẽ tự động in kèm bảng thông số (Cấp sao, Độ cao, Phương vị, RA/Dec, Giờ mọc - Qua đỉnh - Giờ lặn tại Huế) ở góc trên bên trái ảnh.
	Hỗ trợ 3 chế độ xuất: Tải file .PNG về máy, Sao chép ảnh vào Clipboard (để Ctrl+V dán thẳng vào Zalo, Word, PowerPoint), hoặc Chia sẻ nhanh trên điện thoại.
Cách sử dụng ngay: Tính năng "Mã QR Lớp Học" mới ngay trong Web App
Trên thanh công cụ phía trên bên phải của BAN_DO_SAO_Stellarium_HUE.html và index.html có nút Mã QR (phím tắt Q) (btnQrShareHeader):
	Tự động nhận diện link GitHub Pages: Khi trang web được mở trên GitHub Pages, bấm nút Mã QR sẽ tự động lấy đúng đường link trực tuyến hiện tại và hiển thị Mã QR cỡ lớn ngay giữa màn chiếu để học sinh ngồi dưới lớp dùng Camera / Zalo quét trực tiếp.
	Tải Thẻ Mã QR Lớp Học (.PNG) (btnDownloadQrPoster): Xuất ra một tấm Poster độ phân giải cao có tiêu đề Tổ Vật Lí - CN • Trường THPT Hương Thủy - TP. Huế, mã QR cỡ lớn và 4 bước hướng dẫn thực hành để bạn gửi vào nhóm Zalo lớp hoặc in dán tại phòng bộ môn.
