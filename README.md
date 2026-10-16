# Bố Cục Trang Web Với display

Bài thực hành CSS — Luyện tập sử dụng `display: block`, `display: inline-block`, `width`, `max-width` để tạo bố cục trang web cơ bản.

---

## 🎯 Mục tiêu

- Hiểu sự khác biệt giữa `display: block` và `display: inline-block`.
- Dùng `display: inline-block` để xếp nhiều phần tử cạnh nhau theo hàng ngang.
- Kiểm soát kích thước bằng `width` và `max-width`.

---

## 📁 Cấu trúc dự án

```
display-layout/
├── index.html   # Cấu trúc HTML: h1, nav, section (3 cột), footer
├── style.css    # CSS: display block / inline-block, width, max-width
└── README.md    # Mô tả dự án
```

---

## 🔑 Kỹ thuật CSS sử dụng

### `display: block`
- Áp dụng cho `<h1>`, `<footer>` → chiếm **toàn bộ chiều rộng** dòng.
- Có thể đặt `width`, `height`, `margin`, `padding`.

```css
h1 {
    display: block;    /* mặc định của h1 */
    max-width: 100%;
}
```

### `display: inline-block`
- Áp dụng cho `<nav> a` → các liên kết xếp **ngang nhau**.
- Áp dụng cho `.box` → 3 cột xếp **cạnh nhau** trong `<section>`.

```css
nav a  { display: inline-block; margin: 0 15px; }

.box   { display: inline-block; width: 30%; }
```

### `max-width`
- Giới hạn độ rộng tối đa của `<section>`, tránh nội dung quá rộng.

```css
section { max-width: 960px; margin: auto; }
```

---

## ⚠️ Lưu ý: Khoảng trắng với `inline-block`

Các phần tử `inline-block` bị ảnh hưởng bởi **khoảng trắng trong HTML**. Giải pháp:

```css
section { font-size: 0; }      /* Xoá khoảng trắng */
.box    { font-size: 14px; }   /* Khôi phục font-size cho nội dung */
```

---

## 🖥️ Bố cục trang

```
┌─────────────────────────────────────────┐
│   <h1>  Bố cục trang web với display    │  display: block
├─────────────────────────────────────────┤
│  <nav>  [Trang chủ] [Giới thiệu] ...   │  a: display: inline-block
├──────────┬──────────────┬───────────────┤
│  .box    │     .box     │    .box       │  display: inline-block
│  Cột 1  │    Cột 2     │   Cột 3      │  width: 30%
├──────────┴──────────────┴───────────────┤
│            <footer>                     │  display: block
└─────────────────────────────────────────┘
```

---

## 🚀 Cách chạy

Mở file `index.html` trực tiếp trên trình duyệt — không cần server.

---

## 👤 Tác giả

- **Học viên:** Ha Thi My Binh
- **Khóa học:** CodeGym — Thực hành CSS Display
