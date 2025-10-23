# Hướng Dẫn Sử Dụng Website Cưới

## Tính Năng Chuyển Đổi Giữa Nhà Trai và Nhà Gái

Website cưới hiện tại đã được cập nhật để hỗ trợ hiển thị nội dung khác nhau cho nhà trai và nhà gái.

### Cách Sử Dụng

#### 1. **Giao Diện Nhà Trai (Mặc định)**
Khi truy cập website bình thường, giao diện sẽ hiển thị thông tin nhà trai:

```
https://your-website.com/
hoặc
https://your-website.com/index.html
```

**Nội dung hiển thị:**
- **Wedding Timeline:**
  - 09:00 Thứ Bảy, ngày 13.12.2025 - Chụp ảnh cùng gia đình
  - 09:30 Thứ Bảy, ngày 13.12.2025 - Lễ Thành Hôn
  - 10:00 Thứ Bảy, ngày 13.12.2025 - Tiệc Lễ Thành Hôn

- **Thông tin ưu tiên:** Nhà Trai (Nhà Văn Hoá xóm Vân Hoà, Hồng Vân, Hà Nội)

---

#### 2. **Giao Diện Nhà Gái**
Để hiển thị giao diện nhà gái, thêm parameter `?view=codau` vào URL:

```
https://your-website.com/?view=codau
hoặc
https://your-website.com/index.html?view=codau
```

**Các tùy chọn parameter hợp lệ:**
- `?view=codau`
- `?view=bride`
- `?view=nha-gai`

**Nội dung hiển thị:**
- **Wedding Timeline:**
  - 10:00 Thứ Hai, ngày 01.12.2025 - Chụp ảnh cùng gia đình
  - 10:30 Thứ Hai, ngày 01.12.2025 - Lễ Vu Quy
  - 11:00 Thứ Hai, ngày 01.12.2025 - Khai Tiệc

- **Thông tin ưu tiên:** Nhà Gái (Kỳ Tân, Tân Kỳ, Nghệ An)

---

### Ví Dụ Chia Sẻ Link

**Gửi cho khách mời nhà trai:**
```
https://your-website.com/
```

**Gửi cho khách mời nhà gái:**
```
https://your-website.com/?view=codau
```

---

### Tùy Chỉnh Thêm

Nếu bạn muốn thay đổi nội dung cho từng bên, chỉnh sửa file `wedding-switcher.js`:

1. **Timeline nhà trai:** Tìm phần `window.owiData.timeline` trong khối `else`
2. **Timeline nhà gái:** Tìm phần `window.owiData.timeline` trong khối `if (isBrideSide)`

---

### Kiểm Tra Hoạt Động

Mở Console trong trình duyệt (F12) và kiểm tra các log:
- "Đang hiển thị phiên bản nhà trai (mặc định)" - Khi không có parameter
- "Đang hiển thị phiên bản nhà gái" - Khi có parameter view=codau

---

### Hỗ Trợ

Nếu có vấn đề, vui lòng kiểm tra:
1. File `wedding-switcher.js` đã được load chưa
2. Console có báo lỗi không
3. URL parameter có đúng định dạng không

---

**Chúc bạn có một đám cưới thật tuyệt vời! 💒💕**
