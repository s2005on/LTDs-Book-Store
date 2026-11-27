# Bộ tài liệu đồ án LTD's Book Store

[Buổi 9 – Phạm vi cá nhân, nghiệm thu và thử nghiệm tích hợp](B9.md) · [Lịch 4 tuần](05-schedule.md)

Tài liệu kỹ thuật, quản lý dự án, kiểm thử và bàn giao của **LTD's Book Store**. [Quay về README chính](../README.md).

## Hồ sơ dự án cá nhân cuối kỳ

Mốc phát triển hiện tại là **v1.3.0 Pro Edition**, đã nhập qua [PR #14](https://github.com/s2005on/LTDs-Book-Store/pull/14). Giao diện còn được chỉnh sửa. Khi chuẩn bị buổi thi, chọn một commit để dùng chung cho báo cáo, bản chạy và demo.

| Yêu cầu CSE3045 | Hồ sơ đang dùng | Phần cần hoàn thiện |
|---|---|---|
| Ý tưởng, người dùng, yêu cầu và thiết kế | [Phạm vi và tiêu chí](B9.md) · [Kiến trúc và dữ liệu](03-system-design.md) | Đối chiếu với chức năng thực tế sau các lần sửa UI. |
| Lập kế hoạch và giải trình từng tuần | [Kế hoạch 4 tuần](05-schedule.md) · [Nhật ký và mốc Git](SPRINT-TRACKER.md) | Ghi ngày thật, chênh lệch so với kế hoạch, lý do thay đổi và kết quả thử. |
| Sản phẩm, kiểm thử và bàn giao | [Trạng thái bản Pro](FINAL-HANDOVER.md) · [Minh chứng](evidence/README.md) | Lưu kết quả của luồng thành công và một ca lỗi trên bản chọn để demo. |
| Đóng góp cá nhân và nguồn | [Phần việc và nguồn](TEAM.md) | Xác nhận phần tự làm, phần tái sử dụng, công cụ hỗ trợ và phản hồi thực tế. |
| Báo cáo và thuyết trình | Báo cáo cá nhân khoảng 20–30 trang theo hướng dẫn học phần, tài liệu trình bày và demo | Soạn sau khi chốt giao diện. Nộp cùng repo và commit hoặc tag theo lịch thi. |

## 1. Bắt đầu và tổng quan

| Nội dung | Liên kết |
|---|---|
| Giới thiệu, cấu trúc thư mục, sơ đồ hệ thống | [README dự án](../README.md) |
| Cài và khởi động trên Windows | [START-HERE.md](../START-HERE.md) |
| Kiến trúc API/SQLite | [03 — System Design](03-system-design.md) |
| Trạng thái ZIP và mã trên GitHub | [REPO-SYNC-STATUS.md](REPO-SYNC-STATUS.md) |
| Tiếp nhận phiên bản v1.2.1 | [RELEASE-INTAKE-v1.2.1.md](RELEASE-INTAKE-v1.2.1.md) |

## 2. Phân tích yêu cầu và thiết kế

| Hồ sơ | Nội dung |
|---|---|
| [01 — Project Charter](01-project-charter.md) | Mục tiêu, phạm vi, tiêu chí nghiệm thu |
| [02 — Requirements](02-requirements.md) | Yêu cầu chức năng và User Stories |
| [03 — System Design](03-system-design.md) | Kiến trúc, API, bảng dữ liệu |
| [04 — WBS](04-wbs.md) | Phân rã công việc |
| [05 — Schedule](05-schedule.md) | Mốc tiến độ |
| [08 — MVP Demo](08-mvp-demo.md) | Kịch bản trình diễn giai đoạn đầu |

## 3. Quản lý dự án cá nhân

| Hồ sơ | Nội dung |
|---|---|
| [06 — Scrum / Team](06-scrum-team.md) | Vai trò, nguyên tắc làm việc |
| [07 — Sprint 0 Backlog](07-sprint-0-backlog.md) | Backlog giai đoạn khởi động |
| [Sprint Tracker](SPRINT-TRACKER.md) | Mục tiêu Sprint, Issue/PR, công việc còn lại |
| [Team](TEAM.md) · [Stakeholders](STAKEHOLDERS.md) | Trách nhiệm, bên liên quan |
| [Risks](RISKS.md) · [Quality](QUALITY.md) | Rủi ro, tiêu chí chất lượng |
| [Configuration](CONFIG.md) | Quản lý cấu hình và dữ liệu |

## 4. Git, kiểm thử và phát hành

| Tài liệu | Nội dung |
|---|---|
| [Workflow](WORKFLOW.md) | Issue → branch → PR → CI → merge → release |
| [Git conventions](GIT.md) · [PR review](PR-REVIEW.md) | Quy tắc nhánh/commit, review |
| [Test Plan](TEST-PLAN.md) | Test cases, kiểm tra responsive, phân quyền |
| [Academic Traceability](ACADEMIC-TRACEABILITY.md) | User Story ↔ bằng chứng ↔ chức năng |
| [Evidence folder](evidence/README.md) | Nơi lưu ảnh/log kiểm thử thật |
| [Version Intake](VERSION-INTAKE.md) | Quy trình nhận ZIP mới |
| [Versioning](VERSIONING.md) · [Release Checklist](RELEASE-CHECKLIST.md) | SemVer, điều kiện tạo tag |
| [Changelog](../CHANGELOG.md) · [GitHub Actions](https://github.com/s2005on/LTDs-Book-Store/actions) | Lịch sử và kết quả CI |

## 5. Báo cáo học phần và bàn giao

| Hồ sơ | Nội dung |
|---|---|
| [B2 Report](B2-REPORT.md) | Môi trường, kỹ thuật và minh chứng |
| [Midterm](MIDTERM.md) | Khung báo cáo giữa kỳ |
| [Sprint 0 Report](SPRINT0-REPORT.md) | Dấu mốc lịch sử ban đầu |
| [Final Report](FINAL-REPORT.md) | Bản nháp lịch sử v0.5.1 |
| [Final Handover](FINAL-HANDOVER.md) | Kiểm tra trước bàn giao |
| [Verification](../VERIFICATION.md) | Kết quả xác minh và giới hạn |
| [Release notes v0.2.0](RELEASE-v0.2.0.md) | Hồ sơ mốc cũ, không đại diện cho bản mới |

## 6. Hướng dẫn lưu minh chứng phục vụ giảng viên

Mỗi lần phát triển/kiểm thử một bản:

1. Ghi **tên ZIP, VERSION, commit SHA, ngày, hệ điều hành**.
2. Kèm Issue/PR liên quan, ảnh giao diện desktop/mobile và kết quả Python/JavaScript.
3. Chỉ đánh dấu **Đạt** khi tự chạy kiểm thử hoặc có CI của **đúng commit**.
4. Che thông tin cá nhân, không đưa `.env`, SQLite thật hay token lên GitHub.
5. Khi chốt bản demo, lưu link commit hoặc tag trong hồ sơ bàn giao.

Hướng dẫn chạy bản dùng để đối chiếu nằm tại [START-HERE.md](../START-HERE.md).
