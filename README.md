# LTD's Book Store

**CSE3045 · [Hồ sơ cuối kỳ](docs/README.md) · [Hồ sơ Buổi 9](docs/B9.md) · [Kế hoạch cá nhân 4 tuần](docs/05-schedule.md)**

[![CI — Windows & Ubuntu](https://github.com/s2005on/LTDs-Book-Store/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/s2005on/LTDs-Book-Store/actions/workflows/ci.yml)
[![Release workflow](https://github.com/s2005on/LTDs-Book-Store/actions/workflows/release.yml/badge.svg)](https://github.com/s2005on/LTDs-Book-Store/actions/workflows/release.yml)

**Website bán sách Toán dành cho học sinh, phụ huynh và người quản lý cửa hàng.** Dự án xây dựng bằng **Python / FastAPI, SQLite, HTML, CSS và JavaScript**, ưu tiên chạy trực tiếp trên Windows để trình diễn đồ án.

**[Tài liệu đồ án](docs/README.md)** · **[Hướng dẫn chạy](START-HERE.md)** · **[Kiểm thử CI](https://github.com/s2005on/LTDs-Book-Store/actions)** · **[Issues](https://github.com/s2005on/LTDs-Book-Store/issues)** · **[Releases](https://github.com/s2005on/LTDs-Book-Store/releases)**

## 1. v1.3.0 Pro Edition

Người mua có thể lọc sách, quản lý giỏ hàng, đăng ký tài khoản, gửi đơn dùng dữ liệu thử và xem lại trạng thái trong tài khoản. Quản trị viên quản lý danh mục, ảnh bìa, tồn kho và xử lý đơn hàng. SQLite lưu đơn và từng dòng hàng. Phạm vi nghiệm thu cá nhân và kết quả thử nằm trong [hồ sơ Buổi 9](docs/B9.md).

## 2. Chạy nhanh trên Windows

1. Cài [Python 3.11 trở lên](https://www.python.org/downloads/) và bật **Add Python to PATH** khi cài.
2. Tải hoặc giải nén mã nguồn vào một thư mục độc lập.
3. Nhấp đúp **`RUN-WINDOWS.bat`**.
4. Lần đầu: nhập tên và mật khẩu quản trị theo hướng dẫn trong cửa sổ CMD.
5. Mở website ở **http://127.0.0.1:8017/**.

| Giao diện | URL trên máy tính |
|---|---|
| Trang cửa hàng | http://127.0.0.1:8017/ |
| Đăng nhập | http://127.0.0.1:8017/login.html |
| Quản lý sản phẩm | http://127.0.0.1:8017/admin.html |
| Health check | http://127.0.0.1:8017/health |

Lần chạy đầu cần Internet để cài thư viện trong `.venv`. Dữ liệu phát sinh lưu trong `server/data/`; **sao lưu thư mục này trước khi thay phiên bản**. Hướng dẫn chi tiết: [START-HERE.md](START-HERE.md).

## 3. Kiến trúc hệ thống

```mermaid
flowchart LR
    A["Khách hàng / Quản trị<br/>HTML · CSS · JavaScript"]
    B["FastAPI<br/>server/app.py"]
    C[("SQLite<br/>users · books · orders · order_items")]
    D["Ảnh tải lên<br/>server/data/uploads"]
    A -->|"HTTP / JSON"| B
    B --> C
    B --> D
```

Khi khách gửi đơn, FastAPI kiểm tra dữ liệu và tính tổng từ giá trên máy chủ. Khách dùng mã đơn để đối chiếu kết quả trong tài khoản.

## 4. Cấu trúc repository

```text
LTDs-Book-Store/
├── .github/
│   ├── ISSUE_TEMPLATE/        # Mẫu báo lỗi, tính năng, tiếp nhận phiên bản
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── workflows/
│       ├── ci.yml             # Test Python/Node trên Windows và Ubuntu
│       └── release.yml        # Test và phát hành ZIP khi có tag
├── server/
│   ├── app.py                 # API FastAPI và SQLite
│   ├── requirements.txt
│   └── web/                   # HTML, CSS, JS, catalog và ảnh sản phẩm
├── tests/                     # Kiểm thử Python + JavaScript
├── scripts/                   # Đóng gói ZIP và xác minh file
├── docs/                      # Hồ sơ đồ án, Sprint, thiết kế, QA và minh chứng
│   └── evidence/              # Quy định lưu ảnh/log kiểm thử đúng phiên bản
├── deploy/                    # Tài liệu triển khai (chưa dùng VPS)
├── RUN-WINDOWS.bat            # Chạy website trên Windows
├── start.py                   # Khởi động môi trường Python
├── VERSION                    # Phiên bản mã nguồn GitHub
└── CHANGELOG.md               # Lịch sử thay đổi
```

## 5. Quy trình phát triển và kiểm soát phiên bản

```mermaid
flowchart TD
    A["Tiếp nhận yêu cầu / ZIP phiên bản mới"] --> B["GitHub Issue + tiêu chí chấp nhận"]
    B --> C["Tạo nhánh feat/ · fix/ · docs/"]
    C --> D["Cập nhật code, ảnh, test, tài liệu"]
    D --> E["Nếu phát hành: cập nhật VERSION + CHANGELOG trong nhánh"]
    E --> F["Pull Request"]
    F --> G{"CI Windows + Ubuntu đạt?<br/>Đã review thay đổi?"}
    G -->|"Chưa"| D
    G -->|"Đạt"| H["Merge vào main"]
    H --> I["Kiểm tra CI trên main"]
    I --> J["Tag vX.Y.Z → GitHub Release + ZIP"]
```

**Nguyên tắc:** không đẩy mã trực tiếp vào `main` khi đang phát triển; không gắn tag khi ZIP local và mã nguồn GitHub còn khác nhau. Mỗi PR cần có phạm vi, lệnh kiểm thử, ảnh minh chứng khi thay đổi UI và lưu ý bảo mật. Xem [WORKFLOW.md](docs/WORKFLOW.md), [GIT.md](docs/GIT.md) và [VERSIONING.md](docs/VERSIONING.md).

## 6. Kiểm thử và bảo đảm chất lượng

```bash
python -m pip install -r server/requirements-test.txt
python -m unittest discover -s tests -v
node --check server/web/app.js
node --test tests/*.test.cjs
python scripts/package.py
python scripts/verify_package.py
```

GitHub Actions chạy kiểm thử trên **Windows và Ubuntu**, đóng gói và xác minh ZIP theo nội dung `VERSION`. **CI đạt không thay thế kiểm thử trực quan bằng trình duyệt**. Kế hoạch và minh chứng: [TEST-PLAN.md](docs/TEST-PLAN.md), [QUALITY.md](docs/QUALITY.md), [evidence/README.md](docs/evidence/README.md).

## 7. Hồ sơ phục vụ đồ án

| Nhóm | Tài liệu |
|---|---|
| Phân tích yêu cầu | [Project Charter](docs/01-project-charter.md) · [Requirements / User Stories](docs/02-requirements.md) |
| Thiết kế | [System Design](docs/03-system-design.md) · [WBS](docs/04-wbs.md) |
| Quản lý tiến độ | [Schedule](docs/05-schedule.md) · [Scrum](docs/06-scrum-team.md) · [Sprint Tracker](docs/SPRINT-TRACKER.md) |
| Kiểm chứng | [Test Plan](docs/TEST-PLAN.md) · [Ma trận minh chứng](docs/ACADEMIC-TRACEABILITY.md) |
| Báo cáo học phần | [B2](docs/B2-REPORT.md) · [Midterm](docs/MIDTERM.md) · [Final Report](docs/FINAL-REPORT.md) |
| Bàn giao | [Final Handover](docs/FINAL-HANDOVER.md) · [Release Checklist](docs/RELEASE-CHECKLIST.md) |

**[Mở toàn bộ mục lục tài liệu →](docs/README.md)**

## 8. An toàn và giới hạn

- Không commit `.env`, mật khẩu, token, `.venv/`, `server/data/`, file SQLite hoặc dữ liệu khách hàng.
- Chưa triển khai VPS; dịch vụ mặc định chỉ lắng nghe ở `127.0.0.1`.
- Không sử dụng tính năng thanh toán demo để nhận tiền thật.
- Kết quả kiểm thử/báo cáo chỉ được đánh dấu hoàn thành khi có log, commit và minh chứng đúng phiên bản.

© LTD's Book Store — đồ án website bán sách Toán.
