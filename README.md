# Website

Trang web này được xây dựng bằng [Docusaurus](https://docusaurus.io/), một công cụ tạo trang web tĩnh hiện đại.

## Cài đặt

```bash
npm install
```

## Phát triển cục bộ

```bash
npm start
```

Lệnh này sẽ khởi động máy chủ phát triển cục bộ và mở một cửa sổ trình duyệt. Hầu hết các thay đổi sẽ được phản ánh ngay lập tức mà không cần phải khởi động lại máy chủ.

## Build dự án

```bash
npm run build
```

Lệnh này sẽ tạo ra các file tĩnh trong thư mục `build`, có thể được triển khai trên bất kỳ dịch vụ lưu trữ nội dung tĩnh nào.
```

---

### Lưu ý nhỏ về syntax:
- Đảm bảo dùng backtick đúng để bao code block: ``` ````bash ... ````
- Với lệnh `build`, Docusaurus thường dùng script `"build"` trong `package.json`, nên chính xác là `npm run build` (không phải `npm build`).

Nếu bạn muốn mình kiểm tra hoặc định dạng lại theo đúng style của dự án bạn đang dùng (như Prettier, lint, v.v.) thì bạn có thể chia sẻ thêm nhé!