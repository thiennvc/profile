# 📚 INDEX - TÀI LIỆU HƯỚNG DẪN

## 🎯 BẮT ĐẦU TỪ ĐÂU?

### 🚀 Người mới bắt đầu
1. Đọc **[README_VIETNAMESE.md](README_VIETNAMESE.md)** - Tổng quan
2. Đọc **[QUICK_START.md](QUICK_START.md)** - Bắt đầu nhanh
3. Thực hành sửa file đầu tiên!

### 📖 Tìm hiểu chi tiết
- **[HUONG_DAN_CHINH_SUA.md](HUONG_DAN_CHINH_SUA.md)** - Hướng dẫn đầy đủ tất cả tính năng

### 🎚️ Chỉnh giao diện
- **[AN_HIEN_TABS.md](AN_HIEN_TABS.md)** - Ẩn/hiện các tab navbar

---

## 📖 TÀI LIỆU THEO CHỦ ĐỀ

### 1️⃣ Cơ bản
| Tài liệu | Nội dung | Độ ưu tiên |
|----------|----------|------------|
| `README_VIETNAMESE.md` | Tổng quan dự án | ⭐⭐⭐ |
| `QUICK_START.md` | Quick reference | ⭐⭐⭐ |

### 2️⃣ Nội dung
| Tài liệu | Nội dung | Độ ưu tiên |
|----------|----------|------------|
| `HUONG_DAN_CHINH_SUA.md` | Hướng dẫn toàn diện | ⭐⭐⭐ |
| `AN_HIEN_TABS.md` | Quản lý sections | ⭐⭐ |

---

## 🗺️ CẤU TRÚC DỰ ÁN

```
toha/
├── 📄 hugo.yaml                    ⭐ File cấu hình chính
│
├── 📚 TÀI LIỆU (Tiếng Việt)
│   ├── README_VIETNAMESE.md         Tổng quan
│   ├── QUICK_START.md               Quick reference
│   ├── HUONG_DAN_CHINH_SUA.md      Hướng dẫn đầy đủ
│   ├── AN_HIEN_TABS.md             Quản lý tabs
│   └── INDEX.md                     ← Bạn đang đọc file này
│
├── 📁 data/
│   ├── 📁 en/                      ⭐ Nội dung tiếng Anh
│   │   ├── author.yaml              Thông tin cá nhân
│   │   ├── site.yaml                Thông tin website
│   │   └── sections/                Các sections (About, Experiences...)
│   │
│   └── 📁 vi/                      ⭐ Nội dung tiếng Việt
│       ├── author.yaml              Thông tin cá nhân
│       ├── site.yaml                Thông tin website
│       └── sections/                Các sections (Giới thiệu, Kinh nghiệm...)
│
├── 📁 static/images/               🖼️ Thư mục ảnh
│   ├── author/                      Ảnh cá nhân
│   ├── site/                        Logo, background
│   └── companies/                   Logo công ty
│
├── 📁 content/                     📝 Blog posts
│   └── posts/
│
└── 📁 public/                      🚀 Output (auto-generated)
```

---

## 🎯 NHIỆM VỤ THEO MỨC ĐỘ

### ⭐ Cấp cơ bản (Bắt buộc)
- [ ] Đọc `QUICK_START.md`
- [ ] Đổi tên trong `hugo.yaml`
- [ ] Sửa thông tin trong `data/en/author.yaml`
- [ ] Cập nhật phần About
- [ ] Thay ảnh đại diện
- [ ] Push lên GitHub

### ⭐⭐ Cấp trung bình
- [ ] Đọc `HUONG_DAN_CHINH_SUA.md`
- [ ] Sửa phần Experiences
- [ ] Sửa phần Education, Skills
- [ ] Ẩn/hiện các tab (đọc `AN_HIEN_TABS.md`)
- [ ] Tối ưu hình ảnh

### ⭐⭐⭐ Cấp nâng cao
- [ ] Thêm nội dung tiếng Việt đầy đủ
- [ ] Viết blog posts
- [ ] Customize theme (CSS)
- [ ] Thêm Google Analytics

---

## 🔍 TÌM NHANH

### Tôi muốn...

| Mục đích | Đọc tài liệu | File cần sửa |
|----------|--------------|--------------|
| Đổi tên website | `QUICK_START.md` | `hugo.yaml` |
| Đổi email, phone | `QUICK_START.md` | `data/en/author.yaml` |
| Sửa giới thiệu | `QUICK_START.md` | `data/en/sections/about.yaml` |
| Thêm kinh nghiệm | `HUONG_DAN_CHINH_SUA.md` | `data/en/sections/experiences.yaml` |
| Ẩn một tab | `AN_HIEN_TABS.md` | `data/en/sections/TÊN-TAB.yaml` |
| Thêm tiếng Việt | `HUONG_DAN_CHINH_SUA.md` | Tạo thư mục `data/vi/` |
| Thay ảnh | `HUONG_DAN_CHINH_SUA.md` | `static/images/author/` |

---

## 🆘 GẶP VẤN ĐỀ?

### Checklist debug
1. ✅ Kiểm tra cú pháp YAML (dấu space, `:`, `-`)
2. ✅ Xem log lỗi trên Cloudflare Pages
3. ✅ Test local với `hugo server -D`
4. ✅ Đọc phần "Khắc phục lỗi" trong `HUONG_DAN_CHINH_SUA.md`

### Công cụ hữu ích
- **YAML validator:** https://www.yamllint.com
- **Nén ảnh:** https://tinypng.com
- **Toha Docs:** https://toha-docs.netlify.app

---

## 📞 LIÊN HỆ & HỖ TRỢ

- **Toha Theme:** https://github.com/hugo-toha/toha
- **Hugo Docs:** https://gohugo.io/documentation/
- **Cloudflare Pages:** https://developers.cloudflare.com/pages/

---

## ✅ CHECKLIST HOÀN THÀNH

- [ ] Đã đọc README_VIETNAMESE.md
- [ ] Đã đọc QUICK_START.md
- [ ] Đã sửa thông tin cá nhân
- [ ] Đã test website local
- [ ] Đã deploy lên Cloudflare
- [ ] Website hiển thị đúng tại https://profile-6z0.pages.dev
- [ ] Nút chuyển ngôn ngữ hoạt động tốt

---

**Chúc bạn tùy chỉnh website thành công! 🎊**

_Cập nhật lần cuối: 2026-01-18_
