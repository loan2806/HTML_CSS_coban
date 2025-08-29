# 📘 CSS từ cơ bản đến nâng cao (Bản chi tiết)

## 1. Giới thiệu CSS
### CSS là gì?
- CSS (Cascading Style Sheets) là ngôn ngữ dùng để định dạng giao diện web (màu sắc, bố cục, font chữ, hiệu ứng…).
- Tách biệt **nội dung (HTML)** và **hình thức (CSS)** giúp code gọn, dễ bảo trì.

### Ưu điểm
- Tăng tính thẩm mỹ.
- Tái sử dụng nhiều lần.
- Responsive trên nhiều thiết bị.

### 1.1 Cách nhúng CSS
1. **Inline CSS**
   ```html
   <p style="color:red;">Xin chào</p>
   ```
2. **Internal CSS**
   ```html
   <style>
     p { color: blue; }
   </style>
   ```
3. **External CSS**
   ```html
   <link rel="stylesheet" href="style.css">
   ```

---

## 2. Bộ chọn (Selectors)
- **Theo thẻ, class, id**
  ```css
  p { color: red; }
  .className { color: blue; }
  #idName { color: green; }
  ```
- **Kết hợp**
  ```css
  div p { color: red; }
  div > p { color: blue; }
  h1 + p { color: green; }
  ```
- **Pseudo-class**
  ```css
  a:hover { color: red; }
  input:focus { border: 1px solid blue; }
  li:first-child { font-weight: bold; }
  ```
- **Pseudo-element**
  ```css
  p::first-line { font-weight: bold; }
  p::before { content: "👉 "; color: orange; }
  ```

---

## 3. Màu sắc và đơn vị
- **Màu sắc**
  - HEX: `#ff0000`
  - RGB: `rgb(255, 0, 0)`
  - RGBA: `rgba(255, 0, 0, 0.5)`
  - HSL: `hsl(0, 100%, 50%)`
- **Đơn vị**
  - px: tuyệt đối
  - em/rem: tương đối với font-size
  - %: phần trăm kích thước cha
  - vw/vh: viewport width/height
  - fr: dùng trong CSS Grid

---

## 4. Văn bản & Font
```css
p {
  font-family: Arial, sans-serif;
  font-size: 16px;
  font-style: italic;
  font-weight: bold;
}

h1 {
  text-align: center;
  text-transform: uppercase;
  text-decoration: underline;
  letter-spacing: 2px;
  word-spacing: 5px;
  line-height: 1.5;
}
```

---

## 5. Box Model
- **Cấu trúc**: `margin → border → padding → content`
```css
div {
  width: 200px;
  padding: 10px;
  border: 2px solid black;
  margin: 20px;
  box-sizing: border-box;
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
  outline: 2px dashed blue;
}
```

---

## 8. Hiển thị (Display)
- Block
- Inline
- Inline-block
- None
```css
span { display: inline-block; width: 100px; }
```

---

## 9. Vị trí (Position)
- static
- relative
- absolute
- fixed
- sticky
```css
.fixed {
  position: fixed;
  bottom: 0;
  right: 0;
}
```

---

## 10. Flexbox
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

- Các thuộc tính khác:
  - flex-direction
  - flex-wrap
  - justify-content
  - align-items
  - order
  - flex-grow
  - align-self

---

## 11. Grid Layout
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
}

.item {
  grid-column: 1 / 3;
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

@keyframes move {
  from { left: 0; }
  to { left: 100px; }
}
div {
  position: relative;
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

- Mobile-first
- Dùng %, em/rem, vw/vh

---

## 15. CSS nâng cao
```css
li:nth-child(odd) { color: red; }

:root { --main-color: blue; }
h1 { color: var(--main-color); }

div { width: calc(100% - 50px); }

.clip { clip-path: circle(50%); }
```

---

## 16. Công cụ hỗ trợ
- Preprocessor: Sass, Less
- Frameworks: Bootstrap, Tailwind
- CSS-in-JS: styled-components, emotion

---

## 17. Thực hành & Tối ưu
- Tổ chức file CSS theo module/component
- Naming: BEM (`block__element--modifier`)
- Tối ưu:
  - Minify CSS
  - Dùng CDN
  - Tránh CSS dư thừa
  - will-change để tối ưu animation
