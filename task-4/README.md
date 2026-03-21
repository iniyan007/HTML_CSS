# CSS Navigation Bar with Pure CSS Dropdown Menu

## Objective

The objective of this task is to design and implement a responsive navigation bar with a dropdown submenu using only HTML and CSS. The dropdown should appear on hover for desktop users and remain functional on mobile devices using a responsive approach.

---

## Features Implemented

* Navigation bar with multiple menu items
* Dropdown submenu using nested unordered lists
* Smooth hover-based reveal using CSS transitions
* Responsive hamburger menu for smaller screens
* Clean and consistent UI design
* Mobile-friendly navigation without JavaScript

---

## Structure of the Navigation Menu

The navigation bar is built using nested `<ul>` elements:

* Main menu (`.menu`)

  * Contains primary navigation links
* Dropdown (`.dropdown`)

  * Contains submenu (`.submenu`)
* Submenu (`.submenu`)

  * Contains additional navigation options

### Example Structure

```html
<ul class="menu">
  <li><a href="#">Home</a></li>
  <li class="dropdown">
    <a href="#">Shop</a>
    <ul class="submenu">
      <li><a href="#">Fruits</a></li>
      <li><a href="#">Vegetables</a></li>
      <li><a href="#">Offers</a></li>
    </ul>
  </li>
</ul>
```

---

## Styling Details

### Navigation Bar

* Centered layout using Flexbox
* Background color applied for visual separation
* Links styled with padding, border radius, and hover effects

```css
.navbar nav {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---

### Dropdown Menu

* Positioned absolutely relative to parent
* Initially hidden using:

  * `opacity: 0`
  * `visibility: hidden`
  * slight upward transform

```css
.submenu {
  opacity: 0;
  visibility: hidden;
  transform: translateY(-6px);
}
```

---

## Hover Effect Implementation

The submenu becomes visible when the parent is hovered:

```css
.dropdown:hover .submenu,
.dropdown:focus-within .submenu {
  opacity: 1;
  visibility: visible;
  transform: translateY(0);
}
```

### Explanation

* `:hover` triggers the dropdown on desktop
* `:focus-within` improves accessibility
* `transform` and `opacity` create a smooth animation

---

## Smooth Transition

The dropdown uses transitions for a smooth appearance:

```css
transition: opacity 0.25s ease, transform 0.25s ease;
```

This ensures the submenu fades in and slides down smoothly.

---

## Mobile Responsiveness

### Hamburger Menu

* A checkbox (`.nav-toggle`) is used to control menu visibility
* A label with an icon acts as the hamburger button

```html
<input type="checkbox" id="nav-toggle" class="nav-toggle">
<label for="nav-toggle" class="hamburger">
  <img src="images/menu.png">
</label>
```

---

### Mobile Menu Behavior

* Menu becomes vertical
* Hidden by default
* Displayed when checkbox is checked

```css
.nav-toggle:checked ~ .menu {
  opacity: 1;
  visibility: visible;
}
```

---

### Mobile Dropdown Adjustment

* Submenu becomes part of normal flow
* Removed absolute positioning
* Background adjusted for visibility

```css
.submenu {
  position: static;
  opacity: 1;
  visibility: visible;
}
```

---

## Banner Section

* Full-screen background using gradient overlay
* Text centered using padding and alignment
* Typography enhanced using Google Fonts

---

## Additional Styling

* Consistent color theme applied across components
* Box shadows used for depth
* Border radius applied for smooth edges

---

## Key Concepts Used

* HTML nested lists for menu structure
* CSS Flexbox for layout
* CSS positioning (relative and absolute)
* CSS pseudo-classes (`:hover`, `:focus-within`)
* CSS transitions for smooth animations
* Responsive design using media queries
* Checkbox-based toggle for mobile navigation

---

## Conclusion

This task demonstrates how to build a fully functional navigation bar with a dropdown submenu using only HTML and CSS. The implementation ensures smooth interaction, visual consistency, and responsiveness across devices without relying on JavaScript.