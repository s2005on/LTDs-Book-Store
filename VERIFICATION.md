# Verification — LTD's Book Store

## Kết quả của v1.3.0 Pro Edition

[CI trên Windows và Ubuntu](https://github.com/s2005on/LTDs-Book-Store/actions/runs/44733697561) đã đạt trên commit [1d5f3e6](https://github.com/s2005on/LTDs-Book-Store/tree/1d5f3e6656c9f7d7f931f476d78f053edf95d91b). [Hồ sơ bàn giao hiện hành](docs/FINAL-HANDOVER.md) liệt kê phạm vi và các ca cần thử lại khi giao diện thay đổi.

## Lịch sử ngày 18/11/2026

Repository `main` vẫn ở **v0.5.1**. Bản ZIP local mới nhất là **v1.2.1 Auth Update** (đã kiểm tra VERSION=1.2.1, cấu trúc trang đăng nhập/đăng ký và tính toàn vẹn ZIP); các chức năng chưa được đồng bộ hay chạy CI trên GitHub. Xem [biên bản](docs/RELEASE-INTAKE-v1.2.1.md) và [trạng thái đồng bộ](docs/REPO-SYNC-STATUS.md). **Chưa coi ZIP v1.2.1 là GitHub Release.**

## Đối chiếu lịch sử ngày 17/11/2026

Mã trên GitHub `main` là v0.5.1 (chưa nhập mã nguồn ZIP v0.9.0). Không dùng kết quả kiểm thử một bản để xác nhận bản còn lại.

- GitHub Actions trên commit `f3e7aa8` báo **failure**, nhưng log cho thấy Python unittest, JS syntax và Node catalog tests **đã đạt** ở cả Ubuntu/Windows.
- Lỗi CI thực tế: `scripts/package.py` tạo `LTDs-Book-Store-v0.5.1.zip` nhưng workflow cũ tìm `LTDs-Book-Store-v0.5.0.zip`.
- PR `fix/ci-release-workflow` khắc phục bằng cách dùng VERSION và wildcard, xác minh ZIP; kết quả sau merge xem GitHub Actions.
- Bản ZIP local v0.9.0 đã được kiểm thử ở lượt làm trước, nhưng chưa đối chiếu bằng test ở trên repo GitHub.

## Những phần cần kiểm tra thêm

- Đồng bộ đầy đủ backend đơn hàng và ảnh nét cao từ ZIP v0.9.0 vào PR khác.
- Kiểm thử thủ công ở desktop/mobile, đặc biệt ảnh và trạng thái sách, cache trình duyệt.
- Backup/restore và dữ liệu thật; chưa triển khai VPS.
- Không cam kết có payment gateway hay bảo mật production chỉ từ các bài test local.

[CI trên GitHub](https://github.com/s2005on/LTDs-Book-Store/actions) · [Quy trình](docs/WORKFLOW.md) · [Chênh lệch repo/ZIP](docs/REPO-SYNC-STATUS.md)
