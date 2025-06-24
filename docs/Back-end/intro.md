# Backend Docs

Backend của dự án Meow-Gum được xây dựng bằng ngôn ngữ **Go (Golang)** — một ngôn ngữ lập trình hệ thống hiệu năng cao, được thiết kế bởi Google nhằm tối ưu hóa khả năng xử lý concurrent và dễ sử dụng trong các ứng dụng mạng (networking) và hệ thống phân tán.

## 🚀 Lý do chọn Golang

Chúng tôi chọn Golang vì những lý do sau:

- **Hiệu năng cao**: Golang có tốc độ biên dịch và thực thi cực nhanh, phù hợp với các ứng dụng yêu cầu hiệu suất cao.
- **Concurrency built-in**: Hỗ trợ goroutine và channel giúp xử lý bất đồng bộ dễ dàng và hiệu quả hơn bao giờ hết.
- **Syntax đơn giản, dễ học**: Giúp team onboard nhanh chóng và giảm thiểu lỗi phát sinh.
- **Standard library mạnh mẽ**: Có sẵn HTTP server, JSON parsing, database/sql,...
- **Cross-platform**: Build ra binary chạy trên nhiều nền tảng mà không cần cài đặt runtime.

## 📦 Công nghệ chính sử dụng

| Công nghệ           | Mô tả |
|---------------------|-------|
| **Go**              | Phiên bản 1.22 - Ngôn ngữ chính để xây dựng backend |
| **Fiber**           | Framework web nhanh và hiện đại dựa trên Fasthttp |
| **GORM**            | ORM để thao tác với cơ sở dữ liệu Postgres/MySQL |
| **PostgreSQL**      | Cơ sở dữ liệu quan hệ chính của hệ thống |
| **Redis**           | Caching và session management |
| **JWT**             | Xác thực người dùng và tạo token bảo mật |
| **Swagger (swaggo)**| Tự động generate tài liệu API |