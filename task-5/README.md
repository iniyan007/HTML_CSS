# Modal Popup Using the :target Pseudo-Class

## Objective

The objective of this task is to design and implement a modal popup window using only HTML and CSS, without relying on JavaScript. The modal should open and close based on user interaction and include smooth visual transitions.

---

## Features Implemented

* Modal popup controlled using the CSS `:target` pseudo-class
* Open and close functionality without JavaScript
* Centered modal using Flexbox
* Overlay backdrop with transparency and blur effect
* Smooth fade-in and fade-out transitions
* Clean and responsive layout

---

## Structure of the Implementation

The modal system consists of three main parts:

1. **Trigger Link**

   * An anchor tag used to open the modal

2. **Modal Container (`.modelbox`)**

   * Covers the entire screen
   * Acts as a backdrop overlay

3. **Modal Content (`.model-content`)**

   * Contains text and close button

### Example Structure

```html
<a href="#modelbox">Open Model</a>

<div id="modelbox" class="modelbox">
  <div class="model-content">
    <h2>Model Box</h2>
    <p>Content goes here</p>
    <a href="#" class="close-btn">&times;</a>
  </div>
</div>
```

---

## Working Principle

### 1. Opening the Modal

* Clicking the "Open Model" link updates the URL with `#modelbox`
* The element with `id="modelbox"` becomes the active target

```css
.modelbox:target {
  visibility: visible;
  opacity: 1;
}
```

---

### 2. Closing the Modal

* The close button links to `#`, which removes the target from the URL
* The modal returns to its hidden state

---

## Styling Details

### 1. Modal Overlay

```css
.modelbox {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;

  display: flex;
  align-items: center;
  justify-content: center;

  background: rgba(77, 77, 77, 0.475);
  backdrop-filter: blur(5px);

  visibility: hidden;
  opacity: 0;
  transition: all 0.5s ease;
}
```

* Covers the full viewport
* Uses a semi-transparent background
* Applies a blur effect for better visual focus

---

### 2. Centering the Modal

* Flexbox is used to center the modal content both horizontally and vertically

```css
display: flex;
align-items: center;
justify-content: center;
```

---

### 3. Modal Content Styling

```css
.model-content {
  width: 400px;
  background: #fff;
  padding: 30px;
  border-radius: 5px;
}
```

* White background for contrast
* Padding for spacing
* Rounded corners for a clean appearance

---

### 4. Transition Effects

```css
transition: all 0.5s ease;
```

* Smooth fade-in and fade-out effect
* Enhances user experience

---

## Key Concepts Used

* CSS `:target` pseudo-class for state control
* Anchor links for interaction
* CSS Flexbox for layout and centering
* CSS transitions for animation
* Positioning (`fixed`) for full-screen overlay
* Backdrop filtering for visual enhancement

---

## Conclusion

This task successfully demonstrates how to build a functional and visually appealing modal popup using only HTML and CSS. By leveraging the `:target` pseudo-class, the modal can be controlled efficiently without JavaScript, while maintaining smooth transitions and a user-friendly design.
