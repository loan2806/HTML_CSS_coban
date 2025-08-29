# 📘 CSS từ cơ bản đến nâng cao

## 1. Giới thiệu CSS
- **CSS là gì?**
  - CSS (Cascading Style Sheets) dùng để định dạng và thiết kế giao diện cho HTML.
- **Cách nhúng CSS**
  1. **Inline** (trực tiếp trong thẻ):
     ```html
     <p style="color:red;">Xin chào</p>
     ```
  2. **Internal** (trong `<style>` của HTML):
     ```html
     <style>
       p { color: blue; }
     </style>
     ```
  3. **External** (file `.css` riêng):
     ```html
     <link rel="stylesheet" href="style.css">
     ```

---

## 2. Bộ chọn (Selectors)
- **Theo thẻ, class, id**
  ```css
  p { color: red; }       /* selector theo thẻ */
  .className { color: blue; }  /* theo class */
  #idName { color: green; }    /* theo id */
  ```
- **Kết hợp**
  ```css
  div p { color: red; }     /* descendant */
  div > p { color: blue; }  /* child */
  h1 + p { color: green; }  /* sibling */
  ```
- **Pseudo-class**
  ```css
  a:hover { color: red; }
  input:focus { border: 1px solid blue; }
  ```
- **Pseudo-element**
  ```css
  p::first-line { font-weight: bold; }
  ```

---

## 3. Màu sắc và đơn vị
- **Màu**
  - HEX: `#ff0000`
  - RGB: `rgb(255, 0, 0)`
  - RGBA (có độ mờ): `rgba(255, 0, 0, 0.5)`
- **Đơn vị**
  - px (pixel – tuyệt đối)
  - em/rem (tương đối theo font-size)
  - % (theo phần trăm kích thước cha)
  - vw, vh (viewport width/height)

---

## 4. Văn bản & Font
- **Font**
  ```css
  p {
    font-family: Arial, sans-serif;
    font-size: 16px;
    font-style: italic;
    font-weight: bold;
  }
  ```
- **Text**
  ```css
  h1 {
    text-align: center;
    text-transform: uppercase;
    text-decoration: underline;
    letter-spacing: 2px;
    word-spacing: 5px;
  }
  ```

---

## 5. Box Model
- **Cấu trúc**: `margin → border → padding → content`
- Ví dụ:
  ```css
  div {
    width: 200px;
    padding: 10px;
    border: 2px solid black;
    margin: 20px;
    box-sizing: border-box; /* tính cả border+padding trong width */
  }
  ```

---

## 6. Background
```css
body {
  background-color: lightblue;
  background-image: url("bg.png");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
```
- **Gradient**
  ```css
  div {
    background: linear-gradient(to right, red, yellow);
  }
  ```

---

## 7. Border & Outline
```css
div {
  border: 2px solid red;
  border-radius: 10px;
  outline: 2px dashed blue; /* không chiếm chỗ như border */
}
```

---

## 8. Hiển thị (Display)
- **Block**: chiếm hết chiều ngang (p, div).
- **Inline**: chỉ vừa nội dung (span).
- **Inline-block**: vừa gọn + set được width/height.
```css
span { display: inline-block; width: 100px; }
```

---

## 9. Vị trí (Positioning)
```css
.box {
  position: relative;
  top: 10px; left: 20px;
}
.fixed {
  position: fixed; bottom: 0; right: 0;
}
```

---

## 10. Flexbox
- **Căn giữa nhanh**
  ```css
  .container {
    display: flex;
    justify-content: center; /* ngang */
    align-items: center;     /* dọc */
  }
  ```
- **Thuộc tính khác**:
  - `flex-direction: row | column`
  - `flex-wrap: wrap`
  - `order`, `flex-grow`, `align-self`

---

## 11. Grid Layout
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
}
.item {
  grid-column: 1 / 3; /* chiếm 2 cột */
}
```

---

## 12. Transition & Animation
```css
.box {
  transition: all 0.3s ease;
}
.box:hover {
  transform: scale(1.2);
}

/* Animation */
@keyframes move {
  from { left: 0; }
  to { left: 100px; }
}
div {
  animation: move 2s infinite alternate;
}
```

---

## 13. Transform
```css
div {
  transform: translate(50px, 20px) rotate(45deg) scale(1.5);
}
```

---

## 14. Responsive Design
```css
@media (max-width: 768px) {
  body { background: lightgreen; }
}
```
- Dùng **vw/vh** cho thiết kế fluid.
- Dùng **Mobile-first**: viết CSS cho màn nhỏ trước, sau đó mở rộng.

---

## 15. CSS nâng cao
- **nth-child**
  ```css
  li:nth-child(odd) { color: red; }
  ```
- **Variables**
  ```css
  :root { --main-color: blue; }
  h1 { color: var(--main-color); }
  ```
- **calc()**
  ```css
  div { width: calc(100% - 50px); }
  ```

---

## 16. Công cụ hỗ trợ
- **Preprocessor**: Sass, Less (dùng biến, mixin, nesting).
- **Frameworks**: Bootstrap (dễ responsive), Tailwind (utility-first).
- **CSS-in-JS**: styled-components, emotion.

---

## 17. Thực hành tối ưu
- **Tổ chức file**: tách theo module/component.
- **BEM naming**: `block__element--modifier`.
- **Tối ưu**: minify CSS, dùng CDN, tránh CSS dư thừa.

---

👉 Đây là tài liệu đầy đủ: Lý thuyết + Công dụng + Cách dùng + Ví dụ code để học và thực hành.
