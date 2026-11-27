# Minh chứng kiểm thử và tiến độ LTD's Book Store

Mốc ứng dụng đã kiểm tra là [1d5f3e6](https://github.com/s2005on/LTDs-Book-Store/tree/1d5f3e6656c9f7d7f931f476d78f053edf95d91b). [CI trên Windows và Ubuntu](https://github.com/s2005on/LTDs-Book-Store/actions/runs/44733697561) lưu kết quả tự động. [Hồ sơ B9](../B9.md) ghi riêng kết quả chạy trên ZIP. Ảnh và log dùng thử giao diện sẽ bổ sung theo từng commit.

## Quy tắc tên thư mục

`docs/evidence/<version>-<YYYY-MM-DD>/`, ví dụ `v0.9.0-2026-11-17/`.

Gợi ý danh sách file trong mỗi thư mục:
- `README.md`: mã commit/tag, OS/trình duyệt, người kiểm tra, ngày giờ, các bước test, kết luận và giới hạn.
- `01-home-desktop.png`, `02-home-mobile.png`: trang chủ trên hai kích thước.
- `03-book-detail.png`, `04-cart.png`: xem chi tiết và giỏ hàng.
- `05-login.png`, `06-admin-inventory.png`: xác thực và CRUD sách (dữ liệu giả).
- `07-coming-soon.png`: banner và giá/trạng thái chưa mở bán.
- `08-order-flow.png`: ghi mã đơn thử và trạng thái đã đối chiếu ở cả hai vai trò.
- `tests.txt`: lệnh, số lượng test đạt/trượt, commit, hệ điều hành.
- `ci-url.txt`: link run GitHub Actions của đúng commit.

## Mẫu README minh chứng

```md
# Kiểm thử vX.Y.Z — YYYY-MM-DD
- Commit/tag:
- Máy và trình duyệt:
- Cách chạy:
- Chức năng đã thử và kết quả:
- Các testcase đã thất bại, issue sửa:
- Chưa kiểm tra:
- Kết quả CI và URL:
```

**Không lưu:** tên/số điện thoại/địa chỉ khách thật, mật khẩu, file `.env`, token phiên, cơ sở dữ liệu thật. Trước khi đưa ảnh screenshot lên GitHub cần che thông tin cá nhân. Không dán bằng chứng giả hoặc kiểm thử chưa thực hiện.
