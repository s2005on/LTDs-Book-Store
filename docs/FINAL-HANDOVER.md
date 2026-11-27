# Hồ sơ bàn giao LTD's Book Store

## Mốc dùng để phát triển giao diện

| Nội dung | Đối chiếu |
|---|---|
| Mã nguồn | **v1.3.0 Pro Edition** tại [1d5f3e6](https://github.com/s2005on/LTDs-Book-Store/tree/1d5f3e6656c9f7d7f931f476d78f053edf95d91b), nhập qua [PR #14](https://github.com/s2005on/LTDs-Book-Store/pull/14). |
| Người mua | Lọc sách, thêm vào giỏ, gửi đơn, xem lại mã và trạng thái trong tài khoản. |
| Quản trị | Quản lý sách, ảnh, tồn kho và cập nhật trạng thái đơn. |
| Vận hành | [Chạy trên Windows](../START-HERE.md). Dùng dữ liệu thử khi tạo tài khoản và đơn hàng. |
| Kiểm chứng | [CI trên Windows và Ubuntu](https://github.com/s2005on/LTDs-Book-Store/actions/runs/44733697561) đã đạt tại mốc trên. Xem [kế hoạch thử](TEST-PLAN.md) và [minh chứng](evidence/README.md). |
| Trạng thái bàn giao | Đang nâng cấp UI. Commit trình diễn và kết quả nghiệm thu cuối sẽ được ghi sau. |

## Khi chọn bản trình diễn

1. Ghi commit, ngày thử, môi trường và cách chạy lại từ bản tải sạch.
2. Với tài khoản khách, đặt sách còn hàng, ghi mã, tải lại và đối chiếu số lượng, tổng tiền. Với tài khoản quản trị, xác nhận đơn rồi kiểm tra trạng thái phía khách.
3. Thử một điều kiện bị từ chối, chẳng hạn đặt số lượng vượt tồn kho. Ghi phản hồi quan sát được và kiểm tra không phát sinh đơn mới.
4. Lưu kết quả đạt, chưa đạt hoặc chưa thử, cùng lỗi còn mở và ảnh hoặc log đã bỏ thông tin riêng tư. Dùng cùng commit trong báo cáo và demo ngày thi.
