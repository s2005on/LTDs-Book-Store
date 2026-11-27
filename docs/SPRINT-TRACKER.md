# Nhật ký dự án cá nhân

Đối chiếu kết quả từng tuần với [kế hoạch 4 tuần](05-schedule.md). Tổng 36 giờ trong kế hoạch là ước lượng. Giờ thực tế và phản hồi người dùng được ghi khi có dữ liệu.

| Ngày | Việc có thể đối chiếu | Minh chứng | Ý nghĩa với bước tiếp theo |
|---|---|---|---|
| 16/11/2026 | Sửa quy trình CI và đóng gói | [PR #4](https://github.com/s2005on/LTDs-Book-Store/pull/4) | Có bước kiểm tra gói ứng dụng theo phiên bản. |
| 17/11/2026 | Sắp xếp README và mục lục tài liệu | [PR #12](https://github.com/s2005on/LTDs-Book-Store/pull/12) | Có đường dẫn từ trang dự án tới hồ sơ học phần. |
| 20/11/2026 | Lập kế hoạch cá nhân, ghi thử nghiệm bản Pro | [438d1fe](https://github.com/s2005on/LTDs-Book-Store/commit/438d1fed4c12583baa248107244e8bde13fb5046) | Có tiêu chí cho lọc sách, giỏ hàng và luồng đơn. |
| 20/11/2026 | Đồng bộ ứng dụng, ảnh, test và hồ sơ Pro | [PR #14](https://github.com/s2005on/LTDs-Book-Store/pull/14) · [CI trên Windows và Ubuntu](https://github.com/s2005on/LTDs-Book-Store/actions/runs/44733697561) | Dùng [1d5f3e6](https://github.com/s2005on/LTDs-Book-Store/tree/1d5f3e6656c9f7d7f931f476d78f053edf95d91b) làm mốc so sánh các lần sửa giao diện. |
| 28/11/2026 | Đối chiếu hướng dẫn cuối kỳ và tách hồ sơ hiện hành khỏi bản nháp cũ | [Mục lục](README.md) · [Sổ bàn giao](FINAL-HANDOVER.md) | Tiếp tục cải tiến UI, chốt tài liệu thi sau khi chọn bản demo. |

## Ghi một lần nâng cấp giao diện

Mỗi lần hoàn thành một thay đổi, thêm một dòng. Nếu một tuần khác kế hoạch, ghi lý do và việc chuyển tiếp. Với một lỗi hiển thị, lưu cùng kích thước màn hình để dễ đối chiếu trước và sau.

| Tuần / ngày thực hiện | Mục tiêu theo kế hoạch | Thay đổi thực tế và lý do | Commit / PR | Thiết bị, kết quả thử và phản hồi | Việc tiếp theo |
|---|---|---|---|---|---|

Ưu tiên thử lại tác vụ chịu ảnh hưởng. Ví dụ, nếu sửa bộ lọc, chọn lần lượt hai lớp và đối chiếu từng sách hiển thị với danh mục. Nếu sửa giỏ, đổi số lượng rồi tải lại trang để kiểm tra tổng tiền và số lượng. Chỉ ghi người dùng thử và kết quả sau khi buổi thử diễn ra.
