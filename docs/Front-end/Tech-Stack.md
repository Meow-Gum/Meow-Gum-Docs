## 🧰 Công nghệ sử dụng

Ứng dụng được xây dựng trên một stack hiện đại, tập trung vào hiệu suất, khả năng mở rộng và trải nghiệm người dùng mượt mà. Các công nghệ chính được sử dụng bao gồm:

---

### ⚛️ React
- **Phiên bản**: 18.3.1
- Là thư viện UI chính để xây dựng giao diện người dùng theo mô hình component-based.
- Sử dụng tính năng mới nhất như `StrictMode`, `React Hooks`, và JSX.

### 🎨 Tailwind CSS
- **Phiên bản**: 3.4.17
- Framework CSS utility-first giúp xây dựng giao diện nhanh chóng và đồng bộ.
- Tích hợp biến theme tối/sáng với CSS variables.
- Cấu hình responsive và dark mode bằng tiện ích sẵn có.

### 🧱 ShadCN/UI & Radix UI
- Giao diện UI components được xây dựng dựa trên [shadcn/ui](https://ui.shadcn.com/). 
- Thư viện Radix UI cung cấp các component accessible, unstyled và dễ tùy biến:
  - Button, Card, Input, Dialog, Tabs,...
- Hỗ trợ class variance authority (`class-variance-authority`) để tạo biến thể component linh hoạt.

### 🔁 React Router
- **Phiên bản**: 6.20.1
- Quản lý điều hướng giữa các trang với hỗ trợ:
  - Protected Routes
  - Redirect
  - Nested routes

### 🎞️ Framer Motion
- **Phiên bản**: ^11.0.0
- Là thư viện animation mạnh mẽ dành cho React, hỗ trợ tạo hiệu ứng chuyển động mượt mà và dễ dàng tùy biến.
- Được tích hợp vào ứng dụng để:
  - Tạo hiệu ứng enter/exit khi chuyển trang
  - Animation cho component như hover, scale, opacity,...
  - Hỗ trợ layout animations, giúp giao diện thay đổi mượt mà theo trạng thái
  
### 📦 Redux Toolkit
- **Phiên bản**: 2.0.1
- Công cụ quản lý trạng thái toàn cục, giúp kiểm soát logic nghiệp vụ và state của ứng dụng.
- Sử dụng `createSlice`, `createAsyncThunk` và `reducers` để tổ chức logic gọn gàng và dễ bảo trì.

### 🔄 Axios + Interceptors
- **Phiên bản**: 1.6.2
- Xử lý HTTP request đến backend API.
- Sử dụng interceptor để:
  - Tự động thêm token vào header
  - Bắt lỗi chung: 401, 403, 500,...
  - Redirect khi hết hạn phiên đăng nhập

### 🧪 TypeScript
- **Phiên bản**: ~5.8.3
- Đảm bảo type safety và nâng cao khả năng maintain code qua hệ thống interface/type rõ ràng.
- Hỗ trợ cấu trúc đường dẫn alias `@/*` nhờ `tsconfig.json`.

### 🛠️ Vite
- **Phiên bản**: 6.3.5
- Công cụ build hiện đại, cung cấp tốc độ khởi chạy và tải lại cực nhanh.
- Hỗ trợ Typescript, JSX, CSS modules,...

### 📐 PostCSS & Autoprefixer
- Tự động thêm tiền tố vendor cho CSS nhằm đảm bảo tương thích đa nền tảng.

### 🧹 ESLint
- Kiểm tra linting với config nghiêm ngặt, hỗ trợ viết code sạch và đúng chuẩn.

---

## 📌 Một số thư viện phụ trợ khác

| Thư viện | Mục đích |
|---------|----------|
| `lucide-react` | Icon library phong phú và dễ tích hợp |
| `clsx` | Kết hợp classnames linh hoạt |
| `tailwind-merge` | Ghi đè classnames an toàn trong component UI |
| `@radix-ui/react-slot` | Tạo component linh hoạt bằng `<Slot />` |

---

## 🧠 Tổng kết

Với việc áp dụng kiến trúc **Feature-First**, kết hợp cùng **Redux Toolkit**, **Tailwind CSS**, và **React Router v6**, ứng dụng đạt được sự phân tầng rõ ràng, dễ bảo trì và phát triển lâu dài. Đây là lựa chọn tối ưu cho các ứng dụng web vừa và lớn, đặc biệt phù hợp với các sản phẩm MVP hoặc demo học thuật.