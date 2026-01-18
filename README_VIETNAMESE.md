# 📚 TÀI LIỆU HƯỚNG DẪN WEBSITE

## 📖 Các file hướng dẫn

### 1. 🚀 **QUICK_START.md** - Bắt đầu nhanh
- Các file hay sửa nhất
- Thao tác cơ bản
- Checklist sau khi chỉnh sửa
- ⭐ **ĐỌC FILE NÀY TRƯỚC**

### 2. 📝 **HUONG_DAN_CHINH_SUA.md** - Hướng dẫn đầy đủ
- Cấu trúc thư mục chi tiết
- Hướng dẫn từng bước
- Thêm ngôn ngữ Tiếng Việt
- Tối ưu hình ảnh
- Khắc phục lỗi

---

## 🌐 Thông tin Website

**URL:** https://profile-6z0.pages.dev

**Ngôn ngữ hiện có:**
- 🇬🇧 English
- 🇻🇳 Tiếng Việt

**Nút chuyển ngôn ngữ:** Góc trên bên phải navbar (icon cờ)

---

## 🗂️ Cấu trúc file quan trọng

```
📁 data/
├── 📁 en/              ← Nội dung tiếng Anh
│   ├── author.yaml     ⭐ Thông tin cá nhân
│   ├── site.yaml       ⭐ Thông tin website
│   └── 📁 sections/
│       ├── about.yaml           ⭐ Giới thiệu
│       ├── experiences.yaml     ⭐ Kinh nghiệm
│       ├── education.yaml       ⭐ Học vấn
│       ├── skills.yaml          📊 Kỹ năng
│       ├── projects.yaml        💼 Dự án
│       ├── accomplishments.yaml 🏆 Chứng chỉ
│       └── ...
│
└── 📁 vi/              ← Nội dung tiếng Việt
    ├── author.yaml     ⭐ Thông tin cá nhân
    ├── site.yaml       ⭐ Thông tin website
    └── 📁 sections/
        ├── about.yaml           ⭐ Giới thiệu
        ├── experiences.yaml     ⭐ Kinh nghiệm
        └── ...

📄 hugo.yaml            ⭐ File cấu hình chính (Title, URL, Languages)

📁 static/images/       🖼️ Thư mục chứa hình ảnh
```

**⭐ = File quan trọng nhất cần chỉnh sửa**

---

## ✏️ Quy trình chỉnh sửa cơ bản

```
1. Sửa file YAML
   ↓
2. Lưu file (Ctrl + S)
   ↓
3. Test local (tùy chọn)
   hugo server -D
   ↓
4. Commit & Push
   git add .
   git commit -m "Update content"
   git push origin main
   ↓
5. Đợi 2-3 phút
   ↓
6. Kiểm tra website live
   https://profile-6z0.pages.dev
```

---

## 🎯 Nhiệm vụ nhanh

### Đổi tên website
📂 `hugo.yaml` → Dòng 3: `title: "TÊN BẠN"`

### Đổi email/phone
📂 `data/en/author.yaml` hoặc `data/vi/author.yaml`

### Ẩn 1 tab
📂 `data/en/sections/TÊN-TAB.yaml` → `enable: false`

### Thay ảnh đại diện
📂 `static/images/author/profile.jpg` (thay file ảnh)

---

## 📞 Hỗ trợ

**Toha Theme Docs:** https://toha-docs.netlify.app  
**Hugo Docs:** https://gohugo.io/documentation/

---

**Chúc bạn tùy chỉnh website thành công! 🎊**
