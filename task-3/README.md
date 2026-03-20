# 📘 Responsive Grid Layout using CSS Grid

## 🎯 Objective

The objective of this task is to design a **responsive grid layout** that displays multiple items (cards) and adapts to different screen sizes. The layout should show three columns on desktop screens and automatically adjust to fewer columns on smaller devices, eventually stacking into a single column on mobile devices.

---

## 🧩 Features Implemented

* Responsive layout using **CSS Grid**
* Three-column layout for desktop screens
* Two-column layout for tablets
* Single-column layout for mobile devices
* Consistent spacing and alignment between items
* Smooth and adaptive resizing across screen sizes
* Clean and modern UI design

---

## 🏗️ Layout Structure

The layout consists of:

* **Container (`.container`)**

  * Centers content using grid
* **Grid Wrapper (`.card__container`)**

  * Defines the grid structure
* **Grid Items (`.card__article`)**

  * Individual cards displayed inside the grid

---

## 🎨 Grid Implementation

### Desktop View (3 Columns)

```css
.card__container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 5rem;
  justify-items: center;
}
```

* Uses `repeat(3, 1fr)` to create **three equal columns**
* Maintains equal spacing using `column-gap`

---

## 📱 Responsive Behavior

### Tablet View (2 Columns)

```css
@media (max-width: 768px){
  .card__container {
    grid-template-columns: repeat(2, 1fr);
    column-gap: 3rem;
  }
}
```

* Reduces layout to **two columns**
* Adjusts spacing for better fit

---

### Mobile View (1 Column)

```css
@media (max-width: 550px){
  .card__container {
    grid-template-columns: 1fr;
    column-gap: 0;
  }
}
```

* Stacks items into a **single column**
* Ensures readability and usability on small screens

---

## 📏 Spacing and Alignment

* Items are aligned using:

```css
.container {
  display: grid;
  place-items: center;
}
```

* Consistent spacing is maintained using:

  * `column-gap` for horizontal spacing
  * Padding and margins for vertical spacing

---

## 🎴 Card Styling

Each grid item (card) includes:

* Image with rounded corners and shadow
* Hidden content section revealed on hover
* Smooth hover animations and scaling effects

---

## ✨ Additional Enhancements

* Hover effects using `transform: scale()` for interactivity
* Smooth animations using `transition` and `@keyframes`
* Responsive typography adjustments using media queries

---

## 🧠 Key Concepts Used

* CSS Grid (`grid-template-columns`)
* Media Queries for responsiveness
* Fraction units (`fr`) for flexible layouts
* Spacing using `gap` and padding
* Responsive design principles

---

## ✅ Conclusion

This task demonstrates how to build a **fully responsive grid layout** using CSS Grid. The layout adapts seamlessly across devices:

* Desktop → 3 columns
* Tablet → 2 columns
* Mobile → 1 column

This ensures a consistent and user-friendly experience across all screen sizes.
