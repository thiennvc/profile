# 🚀 QUICK START - Chỉnh sửa nhanh

## ✏️ CÁC FILE THƯỜNG DÙNG NHẤT

### 1. Đổi tên và thông tin cơ bản
📂 `data/en/author.yaml` (Tiếng Anh) hoặc `data/vi/author.yaml` (Tiếng Việt)

```yaml
name: "TÊN CỦA BẠN"
email: "email@gmail.com"
phone: "+84 xxx xxx xxx"
```

### 2. Chỉnh title website
📂 `hugo.yaml`

```yaml
title: "Tên của bạn"
```

### 3. Giới thiệu bản thân
📂 `data/en/sections/about.yaml` hoặc `data/vi/sections/about.yaml`

```yaml
designation: Chức danh công việc
company:
  name: Tên công ty
summary: 'Mô tả về bạn...'
```

### 4. Kinh nghiệm làm việc
📂 `data/en/sections/experiences.yaml` hoặc `data/vi/sections/experiences.yaml`

```yaml
experiences:
- company:
    name: Tên công ty
  positions:
  - designation: Vị trí
    start: Tháng X 20XX
    end: Hiện tại
    responsibilities:
    - Công việc 1
    - Công việc 2
```

---

## 🔧 THAO TÁC THƯỜNG DÙNG

### ẨN một tab không muốn hiển thị

Ví dụ: Ẩn tab "Publications"

📂 `data/en/sections/publications.yaml`

```yaml
section:
  enable: false        # ← Đổi thành false
  showOnNavbar: false  # ← Đổi thành false
```

### THAY ĐỔI thứ tự các tab

Chỉnh số `weight` (số nhỏ = lên trước)

```yaml
section:
  weight: 1  # ← 1 = đầu tiên, 2 = thứ hai, 3 = thứ ba...
```

### THAY ẢNH đại diện

1. Đặt ảnh vào: `static/images/author/profile.jpg`
2. Kích thước khuyến nghị: **400x400px** đến **800x800px**
3. Nén ảnh trước tại: https://tinypng.com

---

## 🌐 NGÔN NGỮ

### Tạo nội dung Tiếng Việt

1. **Copy** thư mục `data/en/` → `data/vi/`
2. **Dịch** nội dung trong các file `.yaml` sang tiếng Việt
3. **Lưu** và build lại

### Nút chuyển ngôn ngữ

- Tự động hiện ở góc trên phải khi có 2+ ngôn ngữ
- Biểu tượng cờ 🇬🇧/🇻🇳

---

## 📤 DEPLOY LÊN CLOUDFLARE

### Cách 1: Từ VS Code / Terminal

```bash
git add .
git commit -m "Update content"
git push origin main
```

### Cách 2: Upload file lên GitHub

1. Vào https://github.com/thiennvc/profile
2. Kéo thả file đã sửa
3. Nhấn "Commit changes"

### ⏱️ Thời gian

- **2-3 phút** deploy tự động
- Xem tại: https://profile-6z0.pages.dev

---

## ✅ KIỂM TRA LOCAL (Tùy chọn)

```bash
# Xóa cache cũ
Remove-Item -Recurse -Force public

# Build
hugo

# Hoặc chạy server local
hugo server -D
# Mở: http://localhost:1313
```

---

## 🆘 LỖI THƯỜNG GẶP

### Build lỗi trên Cloudflare

✅ **Kiểm tra:**
- Cú pháp YAML đúng (dấu cách, dấu `:`, `-`)
- Đường dẫn ảnh tồn tại
- Không có ký tự đặc biệt

### Website không cập nhật

✅ **Giải pháp:**
- Đợi 2-3 phút
- Xóa cache: `Ctrl + Shift + R`
- Kiểm tra Cloudflare deploy status

---

## 📋 CHECKLIST SAU KHI CHỈNH SỬA

- [ ] Đổi tên và email trong `author.yaml`
- [ ] Update title trong `hugo.yaml`
- [ ] Sửa phần "About" 
- [ ] Cập nhật "Experiences"
- [ ] Thay ảnh đại diện
- [ ] Ẩn các tab không cần
- [ ] (Tùy chọn) Thêm nội dung tiếng Việt
- [ ] Test local
- [ ] Push lên GitHub
- [ ] Kiểm tra website live

---

Xem hướng dẫn đầy đủ tại: **`HUONG_DAN_CHINH_SUA.md`** 📖
