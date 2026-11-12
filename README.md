# Bài 18 - Json Array Model – Group Customers

Dự án Angular độc lập: đọc khách hàng từ JSON bằng HttpClient, hiển thị nhóm VIP/Normal bằng ngFor lồng nhau, xử lý lỗi bằng retry(3) và catchError.

## Chạy bài

Cài Node.js 22.12 trở lên (nhánh 22), hoặc Node.js 24. Mở terminal ngay tại folder `bài 18`:

```powershell
npm ci
npm start
```

Mở http://localhost:4200 để xem bài. Nếu cổng 4200 đang được dùng:

```powershell
npm start -- --port 4218
```

Sau đó mở http://localhost:4218.

## Build

```powershell
npm run build
```

Kết quả nằm tại `dist/my-app/browser`.

## Các file chính

- `public/assets/data/customers.json`: hai nhóm, năm khách hàng theo mẫu đề.
- `public/assets/avatars/`: ảnh chân dung lưu tại máy, lấy từ Wikipedia.
- `src/app/classes/ICustomer.ts`: model khách hàng và nhóm.
- `src/app/services/customer-http-service.ts`: đọc JSON và xử lý lỗi HTTP.
- `src/app/group-customers-component/`: component, HTML và CSS.
- `src/app/app-module.ts`: cấu hình ứng dụng độc lập.

Để kiểm tra thông báo lỗi, tạm đổi tên file JSON rồi tải lại trang. Đổi lại tên để hiển thị dữ liệu bình thường.

## Nộp bài / GitHub

Chỉ cần nộp toàn bộ folder `bài 18`, gồm cả các file cấu hình và `package-lock.json`. `.gitignore` đã loại trừ `node_modules`, `dist` và cache `.angular`.

Dự án tự chạy sau khi cài thư viện, không cần thư mục cha, server sách hay MongoDB.
