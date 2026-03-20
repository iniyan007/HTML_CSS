# 📘 CSS Card Component with Hover Effects

## 🎯 Objective

The objective of this task is to design and develop a visually appealing **card component** using HTML and CSS. The card should display an image, title, and description, along with smooth hover effects to enhance user interaction.

---

## 🧩 Features Implemented

* Responsive card layout using **CSS Grid**
* Card structure with:

  * Image
  * Title
  * Description
  * Call-to-action button
* Smooth **hover animations**
* Soft **shadow effects** for depth
* Clean and modern UI design
* Responsive design using **media queries**

---

## 🏗️ Structure of the Card

Each card is built using the following structure:

* **Container (`.card__container`)**

  * Holds multiple cards in a grid layout
* **Card (`.card__article`)**

  * Main wrapper for each card
* **Image (`.card__img`)**

  * Displays the product image
* **Data Section (`.card__data`)**

  * Contains description, title, and button

---

## 🎨 Styling Details

### 1. Layout

* CSS Grid is used to align cards in **3 columns**
* Cards are centered using `place-items: center`

```css
.card__container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```

---

### 2. Card Design

* Rounded corners using `border-radius`
* Soft shadow applied for depth
* Border added for visual emphasis

```css
.card__img {
  border-radius: 1.5rem;
  box-shadow:
    0 0 20px rgba(0, 0, 0, 0.05),
    0 0 40px rgba(0, 0, 0, 0.06);
}
```

---

### 3. Hidden Content (Card Info)

* The card data is initially hidden below the image
* Positioned using `absolute` and `bottom: -9rem`
* Hidden using `opacity: 0`

---

## ✨ Hover Effects

### 1. Reveal Animation

* On hover, the hidden content slides upward
* Implemented using **CSS keyframes**

```css
.card__article:hover .card__data {
  animation: show-data 1s forwards;
  opacity: 1;
}
```

---

### 2. Smooth Transition

* Opacity and movement are animated for smoothness
* Creates a **professional UI interaction**

---

### 3. Scale Effect

* Card slightly enlarges on hover

```css
.card__article:hover {
  transform: scale(1.05);
  transition-duration: 0.5s;
}
```

---

### 4. Animation Flow

* Content moves up → slight bounce → settles
* Reverse animation applied when hover ends

---

## 📱 Responsive Design

Media queries are used to ensure the layout works across devices:

* Adjust font sizes for smaller screens
* Convert navbar to vertical layout
* Reduce spacing and padding

---

## 🧠 Key Concepts Used

* CSS Grid for layout
* Positioning (`relative`, `absolute`)
* CSS Animations (`@keyframes`)
* Transitions for smooth effects
* Box shadows for depth
* Responsive design using media queries

---

## ✅ Conclusion

This task demonstrates how to build a modern card component with:

* Clean layout
* Smooth animations
* Interactive hover effects

The implementation improves user experience by making the UI visually engaging and responsive across devices.

---

## 🚀 Future Improvements

* Add dynamic data using JavaScript or React
* Include rating, price, or badges
* Enhance animations using libraries like Framer Motion
* Add accessibility improvements

---
