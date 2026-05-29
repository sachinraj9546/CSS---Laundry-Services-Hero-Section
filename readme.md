# Laundry Services Landing Page

A responsive landing page for a laundry service built using HTML and CSS. This project focuses on creating a mobile-friendly responsive design that works across different screen sizes.

## What This Project Does

The page displays a laundry service hero section with a responsive navigation menu. On desktop screens, the navigation is visible in the header. On mobile devices (screens smaller than 768px), the navigation collapses into a hamburger menu that slides in from the right when clicked.

## Key Learning Points

### 1. Understanding CSS Selectors and Pseudo-Classes

I learned that the `:focus` pseudo-class selector works when an element has keyboard focus. The selector `.hamburger-btn:focus + .menu-list` targets the menu that comes right after (adjacent sibling) the hamburger button. This was tricky to understand at first because I had to ensure the menu div was positioned as a direct sibling in the HTML for this to work.

### 2. CSS Transforms and Transitions

Instead of using `display: none` and `display: block` to toggle the menu visibility, I used `transform: translateX()` to slide the menu in and out smoothly. I learned that:

- `translateX(100%)` pushes the menu completely off-screen to the right
- `translateX(0)` brings it to normal position
- Adding `transition: transform 0.3s ease-in-out;` makes the movement smooth instead of instant

### 3. Responsive Design with Media Queries

I used `@media (max-width: 768px)` to target mobile devices and `@media (max-width: 1250px)` for tablets. The main changes on mobile are:

- Hide the desktop navigation (`.nav { display: none; }`)
- Show the hamburger button (`display: block`)
- Change the main layout from horizontal to vertical (`flex-direction: column`)

### 4. Flexbox for Layout

Used flexbox throughout the design to organize elements:

- Nav bar items are arranged horizontally with `flex`
- Main content uses flexbox to position the text and image side-by-side on desktop, stacked on mobile

## Challenges I Faced

1. **The :focus selector issue** - At first, I didn't realize the menu had to be a direct HTML sibling of the button for the `:focus + .menu-list` selector to work. I spent time debugging why the selector wasn't firing, then realized I needed to check the DOM structure.

2. **Understanding transforms vs display** - It took a moment to understand why `transform: translateX()` is better than `display: none/block`. The key difference is that transforms create smooth animations, while display changes are instant.

3. **Media query breakpoints** - Deciding which breakpoints to use (768px for mobile, 1250px for tablet) wasn't obvious at first. I tested different sizes to see what made sense based on typical device widths.

## Technologies Used

- HTML5
- CSS3 (Flexbox, Media Queries, Transforms, Transitions, Pseudo-classes)
- Google Fonts (Roboto, Lato)

## How to Test It

1. Open `index.html` in your browser
2. On desktop, you should see the full navigation menu in the header
3. On a mobile device or in mobile view (use browser DevTools), click the hamburger button (☰) to see the menu slide in from the right
4. Click elsewhere or press Escape to close the menu
5. Resize the browser window to test how it adapts at different sizes

## What I Would Do Differently

If I were to rebuild this from scratch, I might:

- Consider adding a close button on the mobile menu for better UX
- Use a checkbox input instead of :focus for more persistent menu state (though :focus works for this assignment)
- Add smoother transitions to all interactive elements
- Test more thoroughly on actual mobile devices, not just browser DevTools

## Author

Sachin Kumar
