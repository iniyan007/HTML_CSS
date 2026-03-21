# Tabbed Content Interface Using CSS

## Objective

The objective of this task is to create a tabbed interface where selecting a tab displays its corresponding content section. The implementation must be achieved using only HTML and CSS without JavaScript.

---

## Features Implemented

* Tab navigation using radio buttons and labels
* Dynamic content switching using the `:checked` pseudo-class
* Smooth transitions between tab contents
* Clean and responsive UI design
* Background blur effect using CSS pseudo-elements

---

## Structure of the Implementation

The tabbed interface consists of three main components:

1. **Radio Inputs**

   * Used to control which tab is active
   * Hidden from the user interface

2. **Labels**

   * Act as clickable tabs
   * Associated with radio inputs using the `for` attribute

3. **Content Sections**

   * Each tab has a corresponding content block
   * Only one content block is visible at a time

### Example Structure

```html id="g7h3nm"
<input type="radio" id="Home" name="tabs" checked>
<label for="Home">Home</label>

<div class="tab-content">
  <div id="home-content">...</div>
</div>
```

---

## Working Principle

### 1. Tab Selection

* Each tab is linked to a radio input
* When a label is clicked, the corresponding input becomes checked

---

### 2. Displaying Content

The `:checked` pseudo-class is used to control visibility:

```css id="m9y1ke"
#Home:checked ~ .tab-content #home-content {
  opacity: 1;
}
```

* Only the selected tab’s content is made visible
* Other contents remain hidden

---

### 3. Hiding Content

```css id="r6zjkl"
.tab-content > div {
  opacity: 0;
  pointer-events: none;
}
```

* All content sections are hidden by default
* Prevents interaction with inactive tabs

---

## Smooth Transition Implementation

Instead of using `display: none`, which cannot be animated, the following properties are used:

```css id="t8u4dn"
opacity: 0;
transform: translateY(10px);
transition: opacity 0.4s ease, transform 0.4s ease;
```

### Active State

```css id="p3x7qf"
opacity: 1;
transform: translateY(0);
```

### Result

* Smooth fade-in effect
* Slight upward motion for better visual feedback
* No layout shift during transitions

---

## Layout and Positioning

* Content sections are stacked using `position: absolute`
* Parent container uses `position: relative` to control layout

```css id="h4z2pk"
.tab-content {
  position: relative;
}
```

---

## Background Blur Effect

A blurred background image is created using a pseudo-element:

```css id="w8c2df"
header::before {
  background: url("images/landscape.jpg") center/cover no-repeat;
  filter: blur(6px);
}
```

* Ensures the background is blurred without affecting foreground content
* Maintains clarity of the tab interface

---

## Key Concepts Used

* CSS `:checked` pseudo-class
* General sibling selector (`~`)
* CSS transitions and transforms
* Flexbox for layout
* Positioning (relative and absolute)
* Pseudo-elements for background effects

## Conclusion

This task demonstrates how to build an interactive tabbed interface using only HTML and CSS. By leveraging radio inputs and the `:checked` pseudo-class, content switching is handled efficiently while maintaining smooth transitions and a modern user interface.
