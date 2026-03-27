# 📄 Interactive Multi-Page Website Simulator (CSS Only)

## 🚀 Objective

Create a fully functional multi-section website that simulates navigation between different pages **without using JavaScript**.
This project demonstrates how powerful CSS can be by handling **state, layout, and transitions** entirely through styles.

---

## 🧠 Concept Overview

Instead of loading separate HTML pages, this project uses:

* Internal sections (`<div>` elements with unique IDs)
* Anchor links (`href="#section"`)
* The CSS `:target` pseudo-class

This combination allows us to mimic real page navigation.

---

## 🔑 Key Features

### 1. 📌 CSS `:target` Navigation

* Each "page" is a `<div>` with a unique `id`
* Clicking navigation links updates the URL fragment
* CSS displays only the targeted section

```css
.page {
  display: none;
}

.page:target {
  display: block;
}
```

---

### 2. 🎬 Page Transitions with Animation

Smooth transitions are applied using CSS animations:

```css
@keyframes fadeIn {
  from { opacity: 0; }
  to   { opacity: 1; }
}

.page:target {
  animation: fadeIn 0.5s ease-in-out;
}
```

---

### 3. 🧭 Navigation Bar

* Built using `<nav>` and anchor tags
* Responsive and simple layout using Flexbox

```css
nav {
  display: flex;
  gap: 20px;
}
```

---

### 4. 📱 Responsive Design

The layout adapts to different screen sizes using:

* Flexbox (`.card-grid`)
* Flexible widths (`flex: 1 1 200px`)
* Clean spacing and scalable typography

---

### 5. 🧩 Layout Techniques Used

| Feature            | Technique              |
| ------------------ | ---------------------- |
| Navigation         | Flexbox                |
| Cards layout       | Flexbox (wrap)         |
| Form layout        | Block + spacing        |
| Sections switching | `:target` pseudo-class |

---

## 📄 Pages / Sections

### 🏠 Home

* Hero section with introduction
* Explanation of how the project works

### 💼 Work

* Displays project cards
* Uses Flexbox grid layout

### 👥 About

* Team member list styled as cards

### ✉️ Contact

* Simple form UI (no backend functionality)

---

## ⚙️ Important CSS Logic

### Default Page Visibility

```css
.page {
  display: none;
}
```

### Show Active Section

```css
.page:target {
  display: block;
}
```

### Default Home Page

```css
#home {
  display: block;
}
```

### Hide Home When Others Are Active

```css
#work:target ~ #home,
#about:target ~ #home,
#contact:target ~ #home {
  display: none;
}
```

---

## 🎯 Requirements Fulfilled

✅ Used `:target` pseudo-class for navigation
✅ No JavaScript used
✅ Smooth CSS animations (fade effect)
✅ Responsive design with Flexbox
✅ Clean and accessible navigation
✅ Structured layout using modern CSS

---

## 📌 Conclusion

This project demonstrates how **advanced CSS techniques** can replicate multi-page navigation behavior without JavaScript.
It’s a great way to understand:

* CSS state management
* Layout systems (Flexbox)
* Animations and transitions
