# 🚀 AdTool Pro - Split & Reactivate Ad Accounts

**HASoftware - Ads Solution - Auto Version**

## 📋 Mô tả

AdTool Pro là một công cụ tự động hóa mạnh mẽ để tách và kích hoạt tài khoản quảng cáo Facebook. Công cụ này kết hợp hai chức năng chính:

1. **🔧 Tách tài khoản quảng cáo** từ Business Manager thành tài khoản cá nhân
2. **🔓 Kích hoạt lại tài khoản** đã bị vô hiệu hóa

## ✨ Tính năng chính

### 🔧 Tách tài khoản quảng cáo

- Xử lý song song với giới hạn tài khoản thành công
- Giao diện web trực quan với thống kê real-time
- Tự động dừng khi đạt đủ số tài khoản thành công
- Dừng khi số lần thất bại vượt quá ngưỡng (mặc định: 500)
- Xử lý đồng thời tối đa 200 tài khoản

### 🔓 Kích hoạt tài khoản

- Tự động kích hoạt sau khi tách 5 phút
- Xử lý tuần tự các tài khoản đang chờ đóng
- Thống kê chi tiết tỷ lệ thành công/thất bại
- Hoạt động trực tiếp trên Business Manager hoặc Ads Manager

### 🎯 Tính năng tổng hợp

- Quy trình tự động hoàn chỉnh
- Giao diện thống nhất cho cả hai chức năng
- Báo cáo tổng hợp chi tiết
- Không tự đóng giao diện khi hoàn thành

## 🛠️ Cài đặt và sử dụng

### Phương pháp 1: Sử dụng Console (F12)

1. **Mở Business Manager Facebook**
2. **Mở Console (F12)**
3. **Copy và paste code từ file `AdTool_Pro_Combined.js`**
4. **Chương trình sẽ tự động khởi chạy**

### Phương pháp 2: Sử dụng Extension

#### Cài đặt Extension:

1. **Tải xuống thư mục `extension/`**
2. **Mở Chrome, vào `chrome://extensions/`**
3. **Bật "Developer mode"**
4. **Click "Load unpacked" và chọn thư mục `extension/`**
5. **Extension sẽ xuất hiện trên thanh công cụ**

#### Sử dụng Extension:

1. **Mở Business Manager hoặc Ads Manager**
2. **Click vào icon AdTool Pro trên thanh công cụ**
3. **Cấu hình các thông số:**
   - Số tài khoản thành công mục tiêu (mặc định: 600)
   - Số lượng xử lý đồng thời (mặc định: 200)
   - Ngưỡng thất bại để dừng (mặc định: 500)
4. **Click "Bắt đầu quá trình"**

## ⚙️ Cấu hình

### Thông số có thể điều chỉnh:

```javascript
// Cập nhật cài đặt
AdToolPro.updateSettings({
  tachTargetSuccess: 600, // Số tài khoản thành công mục tiêu
  maxConcurrentRequests: 200, // Số lượng xử lý đồng thời
  failureThreshold: 500, // Ngưỡng thất bại để dừng
});
```

### Các hàm điều khiển:

```javascript
// Bắt đầu quá trình
AdToolPro.start();

// Dừng quá trình
AdToolPro.stop();

// Xem thống kê
console.log(AdToolPro.stats);
```

## 📊 Thống kê và báo cáo

### Thống kê tách tài khoản:

- Tổng số tài khoản đã xử lý
- Số tài khoản thành công
- Số tài khoản thất bại
- Tỷ lệ thành công
- Thời gian thực hiện

### Thống kê kích hoạt tài khoản:

- Tổng số tài khoản cần kích hoạt
- Số tài khoản kích hoạt thành công
- Số tài khoản thất bại
- Số tài khoản bỏ qua
- Tỷ lệ thành công

### Báo cáo tổng hợp:

- Tổng số tài khoản hoàn tất
- Tổng thời gian thực hiện
- Tỷ lệ thành công tổng thể

## 🔄 Quy trình hoạt động

1. **Khởi tạo**: Kiểm tra môi trường và tạo giao diện
2. **Tách tài khoản**:
   - Lấy danh sách tài khoản Read-Only
   - Xử lý song song với giới hạn
   - Dừng khi đạt mục tiêu hoặc vượt ngưỡng thất bại
3. **Chờ kích hoạt**: Đợi 5 phút trước khi kích hoạt
4. **Kích hoạt tài khoản**:
   - Lấy danh sách tài khoản cần kích hoạt
   - Xử lý tuần tự từng tài khoản
   - Hoạt động trực tiếp trên Business Manager hoặc Ads Manager
5. **Hoàn thành**: Hiển thị báo cáo tổng hợp

## ⚠️ Lưu ý quan trọng

### Yêu cầu hệ thống:

- Trình duyệt Chrome/Firefox/Edge hiện đại
- Truy cập Business Manager Facebook
- Quyền quản lý tài khoản quảng cáo

### Lưu ý bảo mật:

- Chỉ sử dụng trên tài khoản của bạn
- Không chia sẻ access token
- Đóng tab khi không sử dụng

### Giới hạn:

- Tối đa 200 tài khoản xử lý đồng thời
- Ngưỡng thất bại mặc định: 500
- Thời gian chờ kích hoạt: 5 phút

## 🐛 Xử lý lỗi

### Lỗi thường gặp:

1. **"Không thể lấy access token"**

   - Giải pháp: Refresh trang và thử lại

2. **"Không tìm thấy tài khoản Read-Only"**

   - Giải pháp: Kiểm tra quyền truy cập Business Manager

3. **"Script không hoạt động"**
   - Giải pháp: Kiểm tra console để xem lỗi chi tiết

## 📞 Hỗ trợ

- **Email**: support@hasoftware.com
- **Website**: https://hasoftware.com
- **Documentation**: https://docs.hasoftware.com/adtool-pro

## 📄 License

Copyright © 2024 HASoftware. All rights reserved.

---

**HASoftware - Ads Solution - Auto Version**
_Công cụ tự động hóa mạnh mẽ cho quảng cáo Facebook_
