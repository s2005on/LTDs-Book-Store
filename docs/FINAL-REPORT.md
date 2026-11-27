# Bản nháp lịch sử của báo cáo v0.5.1

Bản nháp này ghi lại giai đoạn v0.5.1. Các nhận xét và việc cần làm bên dưới thuộc mốc đó. Hồ sơ hiện hành của v1.3.0 Pro Edition nằm trong [mục lục cuối kỳ](README.md) và [sổ bàn giao](FINAL-HANDOVER.md). Báo cáo nộp thi sẽ được biên soạn khi chốt phiên bản trình diễn.

## 1. Giới thiệu và mục tiêu
Website thương mại điện tử bán sách Toán lớp 6–10, giúp người mua tìm sách theo khối lớp/mục tiêu; chủ cửa hàng đăng nhập và quản lý danh mục, bìa, giá, trạng thái sách.

Quy trình phát triển độc lập của LTD's Book Store sử dụng GitHub Issues, nhánh làm việc, Pull Requests, kiểm thử tự động và hồ sơ nghiệm thu riêng của cửa hàng sách.

## 2. Hồ sơ phân tích và quản lý
- Charter và yêu cầu: [01-project-charter.md](01-project-charter.md), [02-requirements.md](02-requirements.md).
- WBS, lịch, Scrum, backlog: [04-wbs.md](04-wbs.md) đến [07-sprint-0-backlog.md](07-sprint-0-backlog.md), [SPRINT-TRACKER.md](SPRINT-TRACKER.md).
- Ma trận minh chứng: [ACADEMIC-TRACEABILITY.md](ACADEMIC-TRACEABILITY.md).
- Git/PR/CI/Release: [WORKFLOW.md](WORKFLOW.md), [VERSIONING.md](VERSIONING.md).

## 3. Kiến trúc và chức năng ở mã GitHub
- Frontend HTML/CSS/JavaScript trong `server/web/`, backend FastAPI `server/app.py`, SQLite `server/data/shop.sqlite3` khi chạy.
- Có đăng ký/đăng nhập khách và admin; quản trị có CRUD sản phẩm và upload ảnh, phân loại theo tình trạng; cửa hàng có tìm kiếm, lọc, chi tiết, giỏ demo.
- Chưa có backend tạo đơn hàng và quản lý trạng thái đơn trên `main` v0.5.1.
- Bản ZIP local v1.2.1 đã được phát triển thêm, nhưng phải nhập/test trên GitHub trước khi coi là sản phẩm source chính thức.
- VPS và thanh toán trực tuyến không thuộc bản nghiệm thu hiện tại.

## 4. Kiểm thử
- Bộ test hiện có: `tests/` (Python unit/API, Node tests); CI chạy Windows và Ubuntu.
- Chưa suy ra UI hoàn hảo chỉ từ CI: cần ảnh/screen thực của đúng commit tại [evidence/README.md](evidence/README.md).
- Kế hoạch kiểm thử theo chức năng: [TEST-PLAN.md](TEST-PLAN.md).
- Mỗi bản mới có báo cáo nhận ZIP: [VERSION-INTAKE.md](VERSION-INTAKE.md).

## 5. Vấn đề và phương án xử lý
- Chênh lệch bản ZIP v1.2.1 và mã trên GitHub: theo dõi [Issue #3](https://github.com/s2005on/LTDs-Book-Store/issues/10).
- Ảnh sách trên GitHub còn nhỏ: nhập ảnh gốc nét cao và test responsive trước release.
- Tài liệu từng giai đoạn có thể giữ trạng thái lịch sử, nhưng bản tổng kết phải nói rõ trạng thái thời điểm viết.

## 6. Hạn chế / việc cần hoàn thành trước bảo vệ
- [ ] Đồng bộ mã, ảnh, test của ZIP v1.2.1 vào PR.
- [ ] Kiểm tra quyền và quy trình order, nếu đã nhập backend đơn hàng.
- [ ] Ảnh minh chứng desktop/mobile/admin và log test, kèm SHA commit.
- [ ] Chốt phạm vi nghiệm thu cùng giảng viên và ghi phản hồi nếu có.
- [ ] Tạo tag và GitHub Release đúng mã sau CI.

## 7. Kết luận (điền sau khi nghiệm thu)
- Ngày bảo vệ:
- Commit/tag phiên bản trình diễn:
- Những yêu cầu đã đạt:
- Những yêu cầu chưa đạt:
- Phản hồi giảng viên:
- Hướng phát triển tiếp:
