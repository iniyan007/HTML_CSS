# Complex Responsive Layout using CSS Grid & Flexbox

## 📌 Objective

Design a sophisticated and responsive webpage layout using a combination of **CSS Grid** and **Flexbox** techniques. The layout should demonstrate modern UI practices such as overlapping elements, sticky positioning, and responsive design.

---

## 🛠️ Technologies Used

* HTML5
* CSS3 (Grid + Flexbox)
* Google Fonts (Poppins)

---

## 🧩 Features Implemented

### 1. CSS Grid Layout

* The main layout uses **CSS Grid** to divide the page into:

  * Sidebar
  * Main Content
  * Extra Content
* Grid Template:

```css
grid-template-columns: 200px 1fr;
grid-template-areas:
    "sidebar main"
    "sidebar extra";
```

---

### 2. Flexbox for Inner Layout

* Flexbox is used for:

  * Navigation bar alignment
  * Card arrangement inside main section
* Example:

```css
.main {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}
```

---

### 3. Sticky Elements

* **Header** remains visible at the top:

```css
.header {
    position: sticky;
    top: 0;
}
```

* **Sidebar** stays fixed during scroll:

```css
.sidebar {
    position: sticky;
    top: 55px;
}
```

---

### 4. Overlapping Elements (z-index)

* Cards use `position` and `z-index` to create overlap effects:

```css
.highlight {
    position: relative;
    top: -20px;
    z-index: 10;
}

.sample {
    position: relative;
    z-index: -1;
}
```

---

### 5. Responsive Design

* Media query ensures layout adapts for smaller screens:

```css
@media (max-width: 768px) {
    .container {
        grid-template-columns: 1fr;
        grid-template-areas:
            "main"
            "extra"
            "sidebar";
    }
}
```

* Sidebar moves below content on smaller devices.

---

## 📸 Layout Overview

### Desktop View

* Sidebar on left
* Main content on right
* Extra content below main
* Sticky header and sidebar

### Mobile View

* Single column layout:

  * Main → Extra → Sidebar

---

## 🎯 Key Concepts Demonstrated

* CSS Grid for page structure
* Flexbox for alignment and spacing
* Sticky positioning for better UX
* Z-index layering for overlapping UI
* Responsive design using media queries

---

## 📚 Learning Outcomes

* Understanding when to use **Grid vs Flexbox**
* Creating modern responsive layouts
* Handling overlapping elements using `z-index`
* Building user-friendly sticky navigation
