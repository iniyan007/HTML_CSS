# 📄 CSS Accordion Component Documentation

## 📌 Objective

The goal of this task is to build a **CSS-only accordion component** where content sections can **expand and collapse when clicked**, without using JavaScript.

---

## 🧩 Overview

An **accordion** is a UI component that allows users to toggle the visibility of content sections. This implementation uses the **checkbox hack** in CSS to control the open/closed state.

---

## 🏗️ Implementation Details

### 1. 📌 Structure (HTML)

* The accordion is built using an unordered list `<ul>` with multiple `<li>` items.
* Each item contains:

  * A **hidden checkbox input**
  * A **label** (acts as clickable header)
  * A **content div** (expandable section)

```html
<input type="checkbox" id="first">
<label for="first">What is Accordion</label>
<div class="content">...</div>
```

### ✔ Key Concept:

* Clicking the label toggles the checkbox state.
* The checkbox state is used to control content visibility via CSS.

---

### 2. 🎯 Checkbox Hack (Core Logic)

```css
#accordion input[type="checkbox"]{
    display: none;
}
```

* The checkbox is hidden from view.
* Its **checked state** is still accessible in CSS.

```css
#accordion input[type="checkbox"]:checked ~ .content{
    max-height: 400px;
}
```

✔ When checkbox is checked:

* The `.content` expands.

---

### 3. 🎨 Styling

#### Container Styling

```css
#accordion{
    margin: 100px auto;
    width: 600px;
}
```

#### Accordion Item

```css
#accordion li{
    background-color: #fffffff1;
    border-radius: 10px;
    padding: 10px;
}
```

#### Label (Header)

```css
#accordion li label{
    display: flex;
    justify-content: space-between;
    cursor: pointer;
}
```

✔ Makes the header clickable and aligned.

---

### 4. 🎬 Animation (Smooth Transition)

```css
#accordion .content{
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.5s ease;
}
```

✔ Initially:

* Content is hidden (`max-height: 0`)

✔ On expand:

```css
max-height: 400px;
```

✔ Transition:

* Smooth opening/closing animation

---

### 5. 🔄 Icon Rotation Effect

```css
#accordion li label span{
    transform: rotate(90deg);
    transition: 0.5s ease;
}
```

✔ Default:

* Arrow rotated (closed state)

```css
#accordion input[type="checkbox"]:checked ~ label span{
    transform: rotate(0deg);
}
```

✔ On open:

* Arrow rotates back → visual feedback

---

## 🔓 Behavior Options

### ✅ Current Behavior (Multiple Open Sections)

* Each checkbox works independently
* Multiple sections can be open simultaneously

### 🔒 To Allow Only One Section Open

Use **radio buttons instead of checkboxes**:

```html
<input type="radio" name="accordion">
```

✔ This ensures:

* Only one section is open at a time

---

## 📌 Conclusion

This task demonstrates how powerful CSS can be by creating an **interactive accordion component** using only HTML and CSS. The use of the **checkbox hack and transitions** provides a clean, efficient solution for expandable content.
