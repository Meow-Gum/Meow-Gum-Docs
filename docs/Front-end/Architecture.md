# 📁 Kiến Trúc Thiết Kế Thư Mục
Đây là tài liệu mô tả chi tiết cấu trúc thư mục, giúp lập trình viên nhanh chóng nắm bắt cách tổ chức codebase theo kiểu Feature-First Architecture kết hợp với Redux Toolkit và React Router.

## 🧩 Tổng Quan Cấu Trúc Thư Mục
- `src/`
  - `app/` - Core App: store, router
    - `store/` - Redux store + hooks
    - `router/` - Route configuration (React Router)
  
  - `components/` - Component UI chung, reusable
    - `ui/` - Component từ ShadCN (Button, Card, Input,...)
    - `common/` - Component logic chung như ProtectedRoute,...
  
  - `features/` - Feature modules (theo Feature-First)
    - `auth/` - Đăng nhập / đăng ký
    - `dashboard/` - Giao diện bảng điều khiển
  
  - `lib/` - Utility functions (ví dụ: cn - classnames)
  - `config/` - Cấu hình chung (API config, env,...)
  - `assets/` - Hình ảnh, SVG, icon,...
  
  - `index.css` - Tailwind CSS entry point
  - `main.tsx` - Root React App entry point

## 🏗️ Chi Tiết Từng Phần

### 1. app/store/ – Quản Lý Trạng Thái Toàn Cục

#### ✅ Mục đích:
- Tập trung quản lý trạng thái ứng dụng bằng Redux Toolkit
- Dễ bảo trì, test và tích hợp trong toàn bộ ứng dụng

#### 🔧 Các file chính:
- `store/index.ts`: Khởi tạo Redux store với reducer auth.
- `store/hooks.ts`: Custom hook useAppSelector, useAppDispatch để tương tác với store.

### 2. components/ – Component UI & Logic Chung

#### 🧱 Chức năng:
- Cung cấp component UI tái sử dụng (Button, Card, Input)
- Component logic chung như ProtectedRoute, InputWithIcon

#### 📁 Phân loại:
- `ui/`: Component từ ShadCN (được custom nhẹ để phù hợp với dự án)
- `common/`: Component logic dùng chung trong nhiều feature

### 3. features/ – Feature-First Modules
#### 💡 Giới thiệu:
- Đây là trái tim của kiến trúc
- Mỗi tính năng là một module độc lập với đầy đủ: component, slice, service, types
#### 📂 Feature Structure (Example: auth/)
- `auth/` - Module xác thực người dùng
  - `components/` - Các form và giao diện liên quan đến xác thực
  - `pages/` - Các component trang (Trang Đăng nhập/Đăng ký)
  - `slice/` - Redux slice cho các action bất đồng bộ (đăng nhập/đăng ký)
  - `services/` - Gọi API backend
  - `types.ts` - Định nghĩa kiểu dữ liệu

### ✨ Tại Sao Chọn Kiến Trúc Feature-First?

#### Phân Tách Rõ Ràng
- Mỗi tính năng hoàn toàn độc lập với các tính năng khác
- Các module tự chứa đầy đủ component, state và logic riêng

#### Dễ Bảo Trì & Mở Rộng
- Thêm hoặc xóa tính năng mà không ảnh hưởng đến các phần khác
- Phát triển và kiểm thử độc lập cho từng tính năng

#### Cấu Trúc Nhất Quán
- Tổ chức thư mục theo tiêu chuẩn thống nhất cho mọi tính năng
- Cho phép bất kỳ thành viên nào trong nhóm đều có thể làm việc hiệu quả với mọi tính năng

### 5. lib/ - Hàm Tiện Ích Chung

#### 🧰 File Chính
- `utils.ts`: Hàm hỗ trợ kết hợp classnames và tailwind-merge để tránh xung đột CSS

### 6. router/ – Định Tuyến URL

#### 📌 File chính
- `AppRouter.tsx`: Sử dụng react-router-dom để định tuyến, tích hợp ProtectedRoute

#### 🔄 Logic Chuyển Hướng
- Nếu đã đăng nhập nhưng cố vào `/auth` → chuyển sang `/dashboard`
- Nếu chưa đăng nhập nhưng truy cập `/dashboard` → chuyển sang `/auth`

### 7. assets/ – Tài Nguyên Giao Diện

#### 📁 Bao gồm
- SVG icons (email, google, facebook,...)
- Logo công ty
- Icon dùng trong giao diện xác thực

### 8. config/ – Cấu Hình Chung

#### 📄 File chính
- `axiosConfig.ts`: Cấu hình axios global, interceptor
- `.env` và `.env.example`: Cấu hình môi trường (VITE_API_BASE_URL,...)
