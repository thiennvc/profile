# 📝 HƯỚNG DẪN CHỈNH SỬA WEBSITE TOHA

> Hướng dẫn chi tiết cách tùy chỉnh nội dung, giao diện, và ngôn ngữ cho website của bạn

---

## 🎯 MỤC LỤC

1. [Cấu trúc thư mục](#cấu-trúc-thư-mục)
2. [Thay đổi Title và thông tin cơ bản](#1-thay-đổi-title-và-thông-tin-cơ-bản)
3. [Thêm/Bỏ các Tab (Sections)](#2-thêmbỏ-các-tab-sections)
4. [Chỉnh sửa nội dung từng phần](#3-chỉnh-sửa-nội-dung-từng-phần)
5. [Thêm ngôn ngữ Tiếng Việt](#4-thêm-ngôn-ngữ-tiếng-việt)
6. [Tối ưu hình ảnh](#5-tối-ưu-hình-ảnh)
7. [Deploy lên Cloudflare](#6-deploy-lên-cloudflare)

---

## 📁 CẤU TRÚC THƯ MỤC

```
toha/
├── hugo.yaml              # File cấu hình chính
├── data/
│   ├── en/               # Nội dung tiếng Anh
│   │   ├── author.yaml   # Thông tin cá nhân
│   │   ├── site.yaml     # Thông tin website
│   │   └── sections/     # Các phần nội dung
│   │       ├── about.yaml
│   │       ├── experiences.yaml
│   │       ├── skills.yaml
│   │       └── ...
│   └── vi/               # (Sẽ tạo) Nội dung tiếng Việt
├── static/
│   └── images/           # Thư mục chứa hình ảnh
└── content/
    └── posts/            # Bài viết blog
```

---

## 1️⃣ THAY ĐỔI TITLE VÀ THÔNG TIN CƠ BẢN

### 📌 File: `hugo.yaml`

Mở file `hugo.yaml` và chỉnh sửa:

```yaml
# Dòng 1-3: Thay đổi URL và title chính
baseURL: "https://profile-6z0.pages.dev"
languageCode: en-us
title: "Nguyen Viet Chi Thien"  # ← Đổi tên của bạn ở đây

# Dòng 18-22: Title cho từng ngôn ngữ
languages:
  en:
    languageCode: en
    languageName: English
    title: "Nguyen Viet Chi Thien"  # ← Đổi tên tiếng Anh
    weight: 1
```

### 📌 File: `data/en/author.yaml`

Chỉnh sửa thông tin cá nhân:

```yaml
name: "NGUYEN VIET CHI THIEN"  # ← Tên của bạn
nickname: "Thien"              # ← Biệt danh
greeting: "Hi, I am"           # ← Lời chào
image: "images/author/profile.jpg"  # ← Ảnh đại diện

contactInfo:
  email: "thien.nguyenvietchi@gmail.com"  # ← Email của bạn
  phone: "+84 938 424440"                 # ← Số điện thoại
  location: "31/7 Quang Trung Street..."  # ← Địa chỉ

summary:
  - Senior IT Operations Specialist...    # ← Mô tả ngắn về bạn
  - Strong expertise in...
```

### 📌 File: `data/en/site.yaml`

Cập nhật thông tin meta cho SEO:

```yaml
copyright: © 2026 Nguyen Viet Chi Thien.  # ← Năm và tên bạn

description: Portfolio and CV of Nguyen Viet Chi Thien  # ← Mô tả website

openGraph:
  title: Thien's Portfolio        # ← Title khi share lên mạng xã hội
  description: CV của Thien       # ← Mô tả
  image: images/author/profile.jpg  # ← Ảnh khi share
  url: https://profile-6z0.pages.dev  # ← URL website
```

---

## 2️⃣ THÊM/BỎ CÁC TAB (SECTIONS)

### 🎚️ Ẩn/Hiện các tab trên navbar

Mỗi section có file riêng trong `data/en/sections/`. Để **ẨN** một tab:

**Ví dụ: Ẩn tab "Publications"**

Mở file `data/en/sections/publications.yaml`:

```yaml
section:
  name: Publications
  id: publications
  enable: false          # ← Đổi từ true thành false
  showOnNavbar: false    # ← Đổi từ true thành false
  weight: 6
```

### 📋 Danh sách các sections có thể ẩn/hiện:

| File | Tab hiển thị | Mục đích |
|------|-------------|----------|
| `about.yaml` | About | Giới thiệu |
| `experiences.yaml` | Experiences | Kinh nghiệm làm việc |
| `education.yaml` | Education | Học vấn |
| `skills.yaml` | Skills | Kỹ năng |
| `projects.yaml` | Projects | Dự án |
| `accomplishments.yaml` | Accomplishments | Chứng chỉ |
| `achievements.yaml` | Achievements | Thành tích |
| `publications.yaml` | Publications | Bài viết/Xuất bản |
| `recent-posts.yaml` | Recent Posts | Bài blog gần đây |
| `featured-posts.yaml` | Featured Posts | Bài blog nổi bật |

### 🔢 Thay đổi thứ tự Tab

Thay đổi giá trị `weight` (số càng nhỏ càng lên trước):

```yaml
section:
  weight: 1  # ← 1 = đầu tiên, 2 = thứ hai, ...
```

---

## 3️⃣ CHỈNH SỬA NỘI DUNG TỪNG PHẦN

### 📄 ABOUT (Giới thiệu)

File: `data/en/sections/about.yaml`

```yaml
designation: Senior IT Operations Specialist  # ← Chức danh
company:
  name: OCB Bank              # ← Tên công ty
  url: "https://www.ocb.com.vn/"

summary: 'Mô tả về bạn...'    # ← Giới thiệu chi tiết

socialLinks:
  - name: Email
    icon: "fas fa-envelope"
    url: "your-email@gmail.com"  # ← Email

badges:  # ← Các kỹ năng mềm hiển thị dạng thanh %
  - type: soft-skill-indicator
    name: Leadership
    percentage: 90       # ← % từ 0-100
    color: blue         # ← Màu: blue, green, orange, red, yellow
```

### 💼 EXPERIENCES (Kinh nghiệm)

File: `data/en/sections/experiences.yaml`

```yaml
experiences:
- company:
    name: OCB Bank                    # ← Tên công ty
    url: "https://www.ocb.com.vn/"
    location: Ho Chi Minh City        # ← Địa điểm
    overview: Ngân hàng thương mại... # ← Mô tả công ty
  positions:
  - designation: Senior IT Ops Specialist  # ← Chức vụ
    start: Feb 2023                   # ← Thời gian bắt đầu
    end: Present                      # ← Kết thúc (hoặc "Present")
    responsibilities:                 # ← Công việc đã làm
    - Quản lý hạ tầng IT
    - Vận hành hệ thống 24/7
```

**Thêm công ty mới:** Copy toàn bộ block `- company:` và paste dưới công ty cuối cùng.

### 🎓 EDUCATION (Học vấn)

File: `data/en/sections/education.yaml`

```yaml
degrees:
- name: Bachelor in Computer Science  # ← Tên bằng
  icon: fa-university
  timeframe: 2000-2004               # ← Thời gian
  institution:
    name: University of XYZ          # ← Tên trường
    url: "#"
  grade:
    text: "GPA: 3.5/4.0"            # ← Điểm (nếu có)
```

### 🛠️ SKILLS (Kỹ năng)

File: `data/en/sections/skills.yaml`

```yaml
skills:
- name: Virtualization              # ← Tên nhóm kỹ năng
  icon: "fa-server"
  summary: "VMware, Hyper-V..."     # ← Mô tả
  details:
  - VMware vSphere/ESXi
  - Microsoft Hyper-V
```

---

## 4️⃣ THÊM NGÔN NGỮ TIẾNG VIỆT

### Bước 1: Cập nhật `hugo.yaml`

Thêm block ngôn ngữ tiếng Việt:

```yaml
languages:
  en:
    languageCode: en
    languageName: English
    title: "Nguyen Viet Chi Thien"
    weight: 1
  
  vi:                                    # ← THÊM MỚI
    languageCode: vi
    languageName: Tiếng Việt
    title: "Nguyễn Việt Chí Thiện"
    weight: 2

defaultContentLanguage: en              # ← Ngôn ngữ mặc định
```

### Bước 2: Tạo thư mục nội dung tiếng Việt

```
data/
└── vi/                    # ← TẠO MỚI
    ├── author.yaml
    ├── site.yaml
    └── sections/
        ├── about.yaml
        ├── experiences.yaml
        └── ...
```

### Bước 3: Copy và dịch nội dung

**Cách nhanh nhất:**
1. Copy toàn bộ thư mục `data/en/` → `data/vi/`
2. Mở từng file trong `data/vi/` và **dịch sang tiếng Việt**

**Ví dụ:** `data/vi/author.yaml`

```yaml
name: "NGUYỄN VIỆT CHÍ THIỆN"
nickname: "Thiện"
greeting: "Xin chào, tôi là"
image: "images/author/profile.jpg"

contactInfo:
  email: "thien.nguyenvietchi@gmail.com"
  phone: "+84 938 424440"
  location: "31/7 Quang Trung, P. TTH, TP.HCM"

summary:
  - Chuyên viên IT Operations với hơn 16 năm kinh nghiệm
  - Chuyên môn về quản trị hệ thống, ảo hóa, mạng, bảo mật
```

### Bước 4: Nút chuyển ngôn ngữ tự động xuất hiện

Sau khi có 2 ngôn ngữ, nút chuyển đổi (cờ 🇬🇧/🇻🇳) sẽ **tự động hiện** ở góc trên phải navbar!

---

## 5️⃣ TỐI ƯU HÌNH ẢNH

### 📸 Quy chuẩn kích thước

| Loại ảnh | Vị trí file | Kích thước khuyến nghị |
|----------|-------------|------------------------|
| **Ảnh đại diện** | `static/images/author/profile.jpg` | 400x400px - 800x800px |
| **Background** | `static/images/site/background.jpg` | 1920x1080px |
| **Logo** | `static/images/site/main-logo.png` | 200x200px (PNG trong suốt) |
| **Favicon** | `static/images/site/favicon.png` | 64x64px hoặc 128x128px |
| **Ảnh công ty** | `static/images/companies/*.png` | 200x200px |

### 🔄 Hugo tự động scale ảnh

Hugo theme Toha đã **tự động resize** ảnh. Bạn chỉ cần:

1. **Đặt ảnh gốc** vào thư mục `static/images/`
2. **Ghi đường dẫn** trong file YAML (không cần `static/`):
   ```yaml
   image: "images/author/profile.jpg"
   ```

### 🗜️ Nén ảnh trước khi upload (khuyến nghị)

**Online tools:**
- https://tinypng.com (PNG, JPG)
- https://squoosh.app (Google)
- https://compressor.io

**Cách dùng:**
1. Upload ảnh lên tool
2. Download ảnh đã nén
3. Replace vào thư mục `static/images/`

---

## 6️⃣ DEPLOY LÊN CLOUDFLARE

### 🚀 Sau khi chỉnh sửa xong

```bash
# 1. Lưu thay đổi
git add .
git commit -m "Update profile content"

# 2. Push lên GitHub
git push origin main
```

### ⏱️ Thời gian deploy

- **Cloudflare Pages tự động build** khi bạn push code
- Thời gian: ~2-3 phút
- Xem tiến độ tại: https://dash.cloudflare.com

### ✅ Kiểm tra website

Sau khi deploy xong, truy cập:
👉 **https://profile-6z0.pages.dev**

---

## 🎨 MẸO CHỈNH SỬA NHANH

### 1. Test local trước khi deploy

```bash
# Chạy server local
hugo server -D

# Mở browser: http://localhost:1313
```

### 2. Chỉnh sửa từng bước nhỏ

- ✅ Sửa 1 file → commit → push → kiểm tra
- ❌ Tránh sửa nhiều file cùng lúc (dễ lỗi khó debug)

### 3. Backup trước khi sửa

```bash
# Tạo branch mới
git checkout -b update-content

# Sau khi test OK, merge về main
git checkout main
git merge update-content
git push origin main
```

### 4. Các file QUAN TRỌNG NHẤT cần sửa

| Mức độ | File | Nội dung |
|--------|------|----------|
| 🔴 Bắt buộc | `hugo.yaml` | Title, URL |
| 🔴 Bắt buộc | `data/en/author.yaml` | Thông tin cá nhân |
| 🟡 Nên sửa | `data/en/sections/about.yaml` | Giới thiệu |
| 🟡 Nên sửa | `data/en/sections/experiences.yaml` | Kinh nghiệm |
| 🟢 Tùy chọn | Các sections khác | Projects, Skills... |

---

## 🆘 KHẮC PHỤC LỖI

### Lỗi build trên Cloudflare

**Kiểm tra:**
1. Cú pháp YAML đúng (space indentation, dấu `:`, `-`)
2. Không có ký tự đặc biệt trong tên file
3. Ảnh tồn tại trong `static/images/`

**Tool kiểm tra YAML:**
- https://www.yamllint.com

### Website không cập nhật

1. Clear cache browser: `Ctrl + F5`
2. Kiểm tra Cloudflare deploy status
3. Đợi 2-3 phút để CDN cập nhật

---

## 📞 HỖ TRỢ

- **Toha Documentation:** https://toha-docs.netlify.app
- **Toha GitHub:** https://github.com/hugo-toha/toha
- **Hugo Documentation:** https://gohugo.io/documentation/

---

**Chúc bạn custom website thành công! 🎉**
