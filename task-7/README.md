# 📘 Task-7 Documentation: Pure CSS Carousel/Slider

## 🔷 Objective

The objective of this task is to design and implement a **pure CSS-based image carousel (slider)** that allows users to navigate through multiple images **without using JavaScript**.

The slider supports:

* Manual navigation using buttons
* Smooth sliding transitions
* Responsive design for different screen sizes

---

## 🔷 Technologies Used

* **HTML5** – Structure of the carousel
* **CSS3** – Styling, layout, and animations

---

## 🔷 Features Implemented

### ✅ 1. Manual Slide Navigation

* Used **hidden radio buttons** (`input type="radio"`) to control slide selection.
* Each radio button corresponds to one image.
* Labels (`<label>`) act as clickable navigation dots.

### ✅ 2. CSS-Based Sliding Effect

* Implemented sliding using:

  * `transform: translateX()`
  * `transition: 0.5s ease-in-out`
* When a radio button is selected (`:checked`), the slider moves accordingly.

### ✅ 3. Grid Layout for Images

* Used **CSS Grid**:

  ```css
  grid-template-columns: repeat(4, 100%);
  ```

* This places all images side-by-side horizontally.

### ✅ 4. Responsive Design

* Used relative units:

  * `vw` (viewport width)
  * `vh` (viewport height)
* Ensures the slider adapts to different screen sizes.

### ✅ 5. Background Styling

* Added a full-screen background image using:

  ```css
  background-size: cover;
  background-attachment: fixed;
  ```

### ✅ 6. Navigation Buttons (Dots)

* Styled circular buttons using:

  ```css
  border-radius: 50%;
  ```
* Positioned centrally using:

  ```css
  transform: translateX(-50%);
  ```

---

## 🔷 Working Mechanism

### 📌 Step 1: Radio Buttons Control State

Each slide is linked to a radio button:

```html
<input type="radio" name="slider" id="slider-image-1" checked>
```

---

### 📌 Step 2: CSS `:checked` Selector

When a radio button is selected, it triggers movement:

```css
#slider-image-2:checked ~ .wrapper .wrapper-holder {
    transform: translateX(-100%);
}
```

---

### 📌 Step 3: Sliding Effect

* Images are placed in a horizontal row.
* The `transform` property shifts the container left/right.
* `transition` ensures smooth animation.

---

## 🔷 Conclusion

This project demonstrates how a fully functional image carousel can be built using **only HTML and CSS**, without JavaScript. It highlights the use of:

* CSS selectors (`:checked`)
* Layout techniques (Grid)
* Transforms and transitions

This approach is lightweight, efficient, and suitable for simple UI components.
