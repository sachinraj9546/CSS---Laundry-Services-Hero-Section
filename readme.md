# Laundry Services Landing Page

## Project Overview

This project is a responsive landing page for a laundry service created using HTML and CSS. The page contains a navigation bar, a hero section with text and an image, and a mobile navigation menu that appears when the hamburger button receives focus.

The main goal of this assignment was to practice responsive design, media queries, Flexbox, and the `:focus` pseudo-class.

---

## Features

* Responsive navigation bar
* Hero section with text and image
* Mobile hamburger menu
* Uses the `:focus` pseudo-class
* Media queries for different screen sizes
* Flexbox layout
* Simple slide-in menu effect using CSS transitions

---

## Concepts Used

### Flexbox

I used Flexbox to arrange items in the navigation bar and hero section.

Example:

```css
display: flex;
justify-content: space-between;
align-items: center;
```

This helped me place elements next to each other and keep the layout organized.

### Media Queries

I used media queries to make the page responsive.

```css
@media (max-width: 768px)
```

When the screen width becomes smaller:

* Desktop navigation is hidden
* Hamburger menu button is shown
* Hero section changes from row layout to column layout

### :focus Pseudo-Class

The mobile menu is displayed using the `:focus` pseudo-class.

```css
.hamburger-btn:focus + .menu-list {
    display: block;
}
```

I learned that the `+` selector only works when the target element is the immediate next sibling in the HTML structure.

### CSS Transition

I added a transition and transform property to create a simple slide effect for the mobile menu.

```css
transform: translateX(100%);
transition: transform 0.3s ease;
```

---

## What I Learned

While working on this project, I learned how responsive layouts are created using media queries.

The part that took me the most time was understanding the `:focus` pseudo-class and the adjacent sibling selector (`+`). At first, I did not understand why the menu was not appearing. After checking the HTML structure, I realized that the menu div must come directly after the hamburger button for the selector to work.

I also learned how `transform: translateX()` can move elements and how transitions can make UI interactions look smoother.

---

## Challenges

### Understanding the HTML Structure

I initially placed elements in the wrong order, which caused the `:focus + .menu-list` selector not to work. After rearranging the elements, the menu started appearing correctly.

### Responsive Design

It took some testing to adjust the layout for smaller screens. I used browser developer tools to check how the page looked on mobile and tablet screen sizes.

### Menu Animation

Adding the slide effect was a little confusing at first because I had to understand how `translateX()` changes the position of an element.

---

## Technologies Used

* HTML5
* CSS3
* Flexbox
* Media Queries
* CSS Transitions
* Google Fonts (Roboto)

---

## How to Run the Project

1. Download the project files.
2. Open `index.html` in any web browser.
3. Resize the browser window to test responsiveness.
4. Switch to mobile view and click the hamburger icon to view the menu.

---

## Author

Sachin Kumar

