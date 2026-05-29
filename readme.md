# Laundry Services Landing Page

This project is a responsive landing page built using HTML and CSS.

The page contains a navigation bar, hero section, service description and a responsive menu for smaller screen sizes.

## Features

- Responsive layout using Flexbox
- Mobile-friendly navigation menu
- Uses the CSS `:focus` pseudo-class
- Media queries for tablet and mobile screens
- Simple and clean user interface

## Concepts Used

### Flexbox

Flexbox is used to arrange elements inside the navigation bar and hero section.

### Media Queries

Media queries are used to change the layout based on screen size.

```css
@media (max-width: 768px)
````

On mobile screens:

* Desktop navigation is hidden
* Hamburger button is displayed
* Hero section changes from row layout to column layout

### :focus Pseudo-Class

The mobile menu is displayed when the hamburger button receives focus.

```css
.hamburger-btn:focus + .menu-list {
    display: block;
}
```

This selector targets the menu list that is placed directly after the button.

## Challenges Faced

### Understanding the :focus Selector

Initially, I had difficulty understanding how the `:focus` pseudo-class works and how it can be used to show and hide elements.

I learned that the element being targeted must be positioned correctly in the HTML structure for the adjacent sibling selector (`+`) to work.

### Responsive Layout

It took some testing to find suitable breakpoints so that the layout looked good on desktop, tablet and mobile screens.

## Technologies Used

* HTML5
* CSS3
* Flexbox
* Media Queries
* Google Fonts

## How to Run

1. Download the project files.
2. Open `index.html` in a browser.
3. Resize the browser window to test responsiveness.
4. On mobile view, click the hamburger icon to display the menu.

## Author

Sachin Kumar
