# 🎚️ ẨN/HIỆN CÁC TAB (SECTIONS)

## 📋 Danh sách tất cả các tabs

| # | Tab Name | File | Mô tả | Khuyến nghị |
|---|----------|------|-------|-------------|
| 1 | **About** | `about.yaml` | Giới thiệu bản thân | ✅ Giữ lại |
| 2 | **Experiences** | `experiences.yaml` | Kinh nghiệm làm việc | ✅ Giữ lại |
| 3 | **Education** | `education.yaml` | Học vấn | ✅ Giữ lại |
| 4 | **Skills** | `skills.yaml` | Kỹ năng kỹ thuật | ✅ Giữ lại |
| 5 | **Projects** | `projects.yaml` | Dự án đã làm | ⚠️ Tùy chọn |
| 6 | **Accomplishments** | `accomplishments.yaml` | Chứng chỉ, giải thưởng | ⚠️ Tùy chọn |
| 7 | **Achievements** | `achievements.yaml` | Thành tích nổi bật | ⚠️ Tùy chọn |
| 8 | **Publications** | `publications.yaml` | Bài viết xuất bản | ❌ Có thể ẩn |
| 9 | **Recent Posts** | `recent-posts.yaml` | Blog gần đây | ⚠️ Ẩn nếu không viết blog |
| 10 | **Featured Posts** | `featured-posts.yaml` | Blog nổi bật | ⚠️ Ẩn nếu không viết blog |

---

## 🔴 ẨN MỘT TAB

### Ví dụ 1: Ẩn tab "Publications"

**File:** `data/en/sections/publications.yaml`

```yaml
section:
  name: Publications
  id: publications
  enable: false          # ← ĐỔI TỪ true → false
  weight: 6
  showOnNavbar: false    # ← ĐỔI TỪ true → false
  template: sections/publications.html
```

**Làm tương tự cho tiếng Việt:**  
📂 `data/vi/sections/publications.yaml`

---

### Ví dụ 2: Ẩn tab "Recent Posts" (Blog)

**File:** `data/en/sections/recent-posts.yaml`

```yaml
section:
  name: Recent Posts
  id: recent-posts
  enable: false          # ← ĐỔI TỪ true → false
  weight: 9
  showOnNavbar: false    # ← ĐỔI TỪ true → false
```

---

### Ví dụ 3: Ẩn tab "Achievements"

**File:** `data/en/sections/achievements.yaml`

```yaml
section:
  name: Achievements
  id: achievements
  enable: false          # ← false = ẨN
  weight: 7
  showOnNavbar: false
```

---

## 🟢 HIỆN LẠI MỘT TAB

Chỉ cần đổi ngược lại:

```yaml
section:
  enable: true           # ← ĐỔI TỪ false → true
  showOnNavbar: true     # ← ĐỔI TỪ false → true
```

---

## 🔢 THAY ĐỔI THỨ TỰ TAB

Thay đổi giá trị `weight` (số càng nhỏ càng lên đầu):

```yaml
section:
  weight: 1  # ← 1 = Đầu tiên
  weight: 2  # ← 2 = Thứ hai
  weight: 3  # ← 3 = Thứ ba
```

### Ví dụ: Đưa "Skills" lên trước "Experiences"

**File:** `data/en/sections/skills.yaml`
```yaml
section:
  weight: 2  # ← Đổi từ 4 thành 2
```

**File:** `data/en/sections/experiences.yaml`
```yaml
section:
  weight: 3  # ← Đổi từ 3 thành 4
```

---

## 💡 GỢI Ý SETUP CHO CV CÁ NHÂN

### ✅ Giữ lại (Hiển thị):
- About
- Experiences
- Education
- Skills
- Accomplishments (nếu có chứng chỉ)

### ❌ Ẩn đi:
- Publications (nếu không phải nghiên cứu viên)
- Recent Posts (nếu không viết blog)
- Featured Posts (nếu không viết blog)
- Achievements (nếu trùng với Accomplishments)

---

## 🎯 SETUP NHANH - CV CHUYÊN NGHIỆP

### Bước 1: Ẩn các tab blog

**File:** `data/en/sections/recent-posts.yaml`
```yaml
section:
  enable: false
  showOnNavbar: false
```

**File:** `data/en/sections/featured-posts.yaml`
```yaml
section:
  enable: false
  showOnNavbar: false
```

### Bước 2: Ẩn Publications

**File:** `data/en/sections/publications.yaml`
```yaml
section:
  enable: false
  showOnNavbar: false
```

### Bước 3: Sắp xếp lại thứ tự

```
1. About           (weight: 1)
2. Experiences     (weight: 2)
3. Education       (weight: 3)
4. Skills          (weight: 4)
5. Projects        (weight: 5)
6. Accomplishments (weight: 6)
```

---

## 📤 LƯU VÀ DEPLOY

```bash
# Lưu thay đổi
git add .
git commit -m "Hide unused sections"
git push origin main
```

⏱️ Đợi 2-3 phút → Kiểm tra website!

---

## 🔍 KIỂM TRA LOCAL

```bash
hugo server -D
```

Mở browser: http://localhost:1313  
Kiểm tra navbar xem các tab đã ẩn/hiện đúng chưa.

---

**Pro tip:** Bắt đầu với setup tối giản (chỉ 4-5 tabs quan trọng), sau đó thêm dần các tab khác khi có nội dung! ✨
