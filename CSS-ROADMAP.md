🎨 15-Day CSS Roadmap for Beginners — From Zero to Stylish Hero
"In 2025, everyone wants to get into web development, but most students ask me — where to begin? So as a senior and your coding guide, I've taken the responsibility to give you the most beginner-friendly CSS roadmap that I wish I had when I started."

💡 First: What is CSS?
CSS (Cascading Style Sheets) is the language that makes your website look good — it's how you control fonts, colors, layout, animation, responsiveness, and more.

"You already know HTML builds the structure... but CSS is what brings it to life — it's what gives your website vibe, style, and modern feel."

✍️ How Do We Write CSS?
There are 2 main ways to write CSS:

🧵 1. CSS by Itself (Vanilla CSS)
This is where you write .css files and link them. Simple and widely used.

```html
<!-- HTML file linking to external CSS -->
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

```css
/* styles.css */
body {
  font-family: Arial, sans-serif;
  color: #333;
}
```

🧶 2. CSS Preprocessors (SCSS/SASS)
Advanced and powerful. It gives you nesting, variables, functions, reusability, and helps with bigger projects. You'll use this in frameworks and teams.

```scss
// SCSS syntax example
$primary-color: #3498db;

.container {
  max-width: 1200px;
  
  .header {
    background-color: $primary-color;
    
    h1 {
      font-size: 2rem;
    }
  }
}
```

🗺️ 15-Day Complete CSS Roadmap (Beginner to Pro)
Let's break it down, step-by-step in natural, beginner-friendly flow:

📘 Day 1–2: CSS Basics – Styling Starts Here
What is CSS and how it works with HTML

Three ways to apply CSS: Inline, Internal, External

```html
<!-- Inline CSS -->
<p style="color: blue; font-size: 18px;">This is styled inline</p>

<!-- Internal CSS -->
<head>
  <style>
    p { 
      color: green; 
      margin-bottom: 15px; 
    }
  </style>
</head>

<!-- External CSS (link shown above) -->
```

File linking with <link rel="stylesheet">

Selectors: Element, .class, #id, and grouping (h1, h2, p)

```css
/* Element selector */
p { 
  line-height: 1.6; 
}

/* Class selector */
.highlight { 
  background-color: yellow; 
}

/* ID selector */
#header { 
  position: sticky; 
  top: 0; 
}

/* Grouping selectors */
h1, h2, p { 
  font-family: 'Roboto', sans-serif; 
}
```

Writing clean and readable code

🧠 Practice: Create a personal card with name, photo, and basic style.

```css
/* Personal card example */
.profile-card {
  width: 300px;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.profile-card img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
}

.profile-card h2 {
  margin-top: 15px;
  margin-bottom: 5px;
  color: #333;
}

.profile-card .title {
  color: #666;
  font-style: italic;
  margin-bottom: 15px;
}
```

🧱 Day 3: The Box Model (This is Core)
Every element = box.

margin, border, padding, content

```css
/* Box model visualization */
.box {
  /* Content area */
  width: 300px;
  height: 200px;
  
  /* Padding - space inside the border */
  padding: 20px;
  /* or individual sides */
  padding-top: 10px;
  padding-right: 15px;
  padding-bottom: 10px;
  padding-left: 15px;
  
  /* Border */
  border: 2px solid #333;
  border-radius: 8px;
  
  /* Margin - space outside the border */
  margin: 30px;
  /* or individual sides */
  margin-top: 20px;
  margin-right: 10px;
  margin-bottom: 20px;
  margin-left: 10px;
}
```

Difference between content-box and border-box

```css
/* Default box-sizing */
.content-box {
  box-sizing: content-box; /* width/height apply to content only */
  width: 300px;
  padding: 20px;
  border: 5px solid #333;
  /* Total width: 300px + 20px + 20px + 5px + 5px = 350px */
}

/* More intuitive box-sizing */
.border-box {
  box-sizing: border-box; /* width/height include padding and border */
  width: 300px;
  padding: 20px;
  border: 5px solid #333;
  /* Total width: exactly 300px */
}

/* Best practice: apply border-box to all elements */
* {
  box-sizing: border-box;
}
```

Width, height, max-width, min-height

```css
.responsive-container {
  width: 80%; /* Percentage of parent */
  max-width: 1200px; /* Won't exceed this size */
  min-height: 500px; /* At least this tall */
  height: auto; /* Height based on content */
}
```

🧠 Practice with colored boxes to visually understand spacing.

✒️ Day 4: Typography & Text Styling
font-family, font-size, line-height

```css
/* Typography basics */
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  color: #333;
}

h1 {
  font-family: 'Georgia', serif;
  font-size: 2.5rem; /* 40px if base font is 16px */
  line-height: 1.2;
  margin-bottom: 0.5em;
}
```

text-align, text-transform, text-decoration

```css
.article-title {
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.link {
  text-decoration: none; /* Removes underline */
  color: #0066cc;
}

.link:hover {
  text-decoration: underline;
  color: #004499;
}

.quote {
  font-style: italic;
  text-align: right;
}
```

letter-spacing, word-spacing

How to import Google Fonts

```html
<!-- In the head of your HTML -->
<head>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet">
</head>
```

```css
/* Using Google Fonts */
body {
  font-family: 'Roboto', sans-serif;
}

h1, h2, h3 {
  font-family: 'Open Sans', sans-serif;
  font-weight: 600;
}
```

🧠 Try styling a heading and paragraph combo beautifully.

🎨 Day 5: Colors, Backgrounds & Gradients
Color systems: HEX, RGB, RGBA, HSL

```css
/* Different color formats */
.color-examples {
  color: #3498db;            /* HEX */
  color: rgb(52, 152, 219);  /* RGB */
  color: rgba(52, 152, 219, 0.7); /* RGBA with opacity */
  color: hsl(204, 70%, 53%); /* HSL (hue, saturation, lightness) */
  color: hsla(204, 70%, 53%, 0.7); /* HSLA with opacity */
}
```

background-color, background-image

```css
.header {
  background-color: #2c3e50;
  color: white;
  padding: 20px;
}

.hero {
  background-image: url('background.jpg');
  background-size: cover;
  background-position: center;
  height: 500px;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

Linear and radial gradients

```css
.gradient-examples {
  /* Simple linear gradient */
  background: linear-gradient(to right, #3498db, #2c3e50);
  
  /* Multiple color stops */
  background: linear-gradient(to bottom, #f1c40f, #e67e22, #e74c3c);
  
  /* Diagonal gradient */
  background: linear-gradient(45deg, #1abc9c, #3498db);
  
  /* Radial gradient */
  background: radial-gradient(circle, #3498db, #2c3e50);
  
  /* Repeating gradient */
  background: repeating-linear-gradient(45deg, #3498db, #3498db 10px, #2c3e50 10px, #2c3e50 20px);
}
```

Transparent overlays

```css
.image-with-overlay {
  position: relative;
  height: 400px;
}

.image-with-overlay img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6); /* Black with 60% opacity */
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  text-align: center;
}
```

🧠 Create a hero section with gradient background and text.

🔎 Day 6: CSS Selectors & Combinators
Attribute selector: input[type="email"]

```css
/* Attribute selectors */
input[type="text"] {
  border: 1px solid #ddd;
  padding: 8px;
}

input[type="email"] {
  border: 1px solid #3498db;
}

/* Partial attribute matches */
a[href^="https"] { /* Starts with https */
  color: green;
}

a[href$=".pdf"] { /* Ends with .pdf */
  font-weight: bold;
}

a[href*="example"] { /* Contains example */
  text-decoration: underline;
}
```

Pseudo-classes: :hover, :active, :checked

```css
/* Pseudo-classes */
.button {
  background-color: #3498db;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.button:hover {
  background-color: #2980b9;
}

.button:active {
  background-color: #1f6aa5;
  transform: translateY(2px);
}

input:focus {
  outline: 2px solid #3498db;
}

input[type="checkbox"]:checked + label {
  color: #3498db;
  font-weight: bold;
}

/* First, last, nth elements */
li:first-child {
  font-weight: bold;
}

li:last-child {
  margin-bottom: 0;
}

li:nth-child(odd) {
  background-color: #f9f9f9;
}
```

Pseudo-elements: ::before, ::after

```css
/* Pseudo-elements */
.quote::before {
  content: '"';
  font-size: 2em;
  color: #3498db;
  margin-right: 5px;
}

.quote::after {
  content: '"';
  font-size: 2em;
  color: #3498db;
  margin-left: 5px;
}

/* Decorative elements */
.fancy-header::before,
.fancy-header::after {
  content: "";
  display: inline-block;
  width: 30px;
  height: 1px;
  background-color: #333;
  margin: 0 15px;
  vertical-align: middle;
}
```

Combinators: >, +, ~, (space)

```css
/* Combinators */
/* Descendant selector (space) */
article p { /* All p inside article */
  line-height: 1.6;
}

/* Child selector (>) */
article > p { /* Only direct p children of article */
  margin-bottom: 1em;
}

/* Adjacent sibling (+) */
h2 + p { /* p immediately after h2 */
  font-weight: bold;
}

/* General sibling (~) */
h2 ~ p { /* Any p after h2 */
  color: #555;
}
```

🧠 Build a hover effect card with ::after decoration.

🧷 Day 7: Positioning & Display
static, relative, absolute, fixed, sticky

```css
/* Position properties */
.static {
  position: static; /* Default - follows normal document flow */
}

.relative {
  position: relative; /* Positioned relative to normal position */
  top: 20px;
  left: 20px; /* Offset from where it would normally be */
}

.absolute {
  position: absolute; /* Positioned relative to nearest positioned ancestor */
  top: 0;
  right: 0; /* Top-right corner of nearest positioned ancestor */
}

.fixed {
  position: fixed; /* Positioned relative to viewport */
  bottom: 20px;
  right: 20px; /* Stays visible while scrolling */
}

.sticky {
  position: sticky; /* Hybrid of relative and fixed */
  top: 0; /* Sticks to top when scrolled to */
  background: white;
  z-index: 100;
}
```

top, left, bottom, right values

z-index and element stacking

```css
/* Z-index and stacking */
.back {
  position: relative;
  z-index: 1;
}

.middle {
  position: relative;
  z-index: 2; /* Higher value appears on top */
}

.front {
  position: relative;
  z-index: 3;
}
```

Display types: block, inline, inline-block, none

```css
/* Display types */
.block {
  display: block; /* Takes full width, starts on new line */
  width: 100%;
  margin-bottom: 10px;
}

.inline {
  display: inline; /* Takes only needed width, stays in line */
  /* width and height have no effect */
}

.inline-block {
  display: inline-block; /* Inline but respects width/height */
  width: 100px;
  height: 100px;
  vertical-align: top;
}

.hidden {
  display: none; /* Completely removed from layout */
}

.invisible {
  visibility: hidden; /* Hidden but still takes up space */
}
```

🧠 Create a sticky header and a popup box.

## 🧩 Day 8: Flexbox – The Modern Layout Solution

> "Flexbox is like having superpowers for aligning elements. Once you understand it, you'll wonder how you ever lived without it!"

### ✨ What is Flexbox?

Flexbox (Flexible Box Layout) is a one-dimensional layout system designed to arrange items in rows OR columns. It's perfect for:

- Navigation bars
- Card layouts
- Centering elements (finally, an easy way!)
- Distributing space between items
- Creating flexible layouts that adapt to screen size

### 🛠️ How to Use Flexbox

**Step 1: Activate Flexbox on parent container**
```css
.container {
  display: flex; /* or display: inline-flex */
}
```

**Step 2: Choose a direction**
```css
.container {
  display: flex;
  flex-direction: row;        /* Default: left to right */
  /* flex-direction: column;  /* Top to bottom */
  /* flex-direction: row-reverse;  /* Right to left */
  /* flex-direction: column-reverse;  /* Bottom to top */
}
```

### 🧭 Understanding Axes

Flexbox has two axes that are crucial to understand:
- **Main axis**: The direction items are placed (follows flex-direction)
- **Cross axis**: Perpendicular to the main axis

![Flexbox Axes Diagram]

### ⚖️ Aligning & Distributing Items

**Along the main axis (justify-content):**
```css
.container {
  display: flex;
  justify-content: flex-start;      /* Default - items at start */
  /* justify-content: flex-end;     /* Items at end */
  /* justify-content: center;       /* Items at center */
  /* justify-content: space-between; /* Items with space between them */
  /* justify-content: space-around;  /* Items with space around them */
  /* justify-content: space-evenly;  /* Items with equal space around them */
}
```

**Along the cross axis (align-items):**
```css
.container {
  display: flex;
  align-items: stretch;     /* Default - items stretch to fill container */
  /* align-items: flex-start; /* Items at start */
  /* align-items: flex-end;   /* Items at end */
  /* align-items: center;     /* Items at center */
  /* align-items: baseline;   /* Items aligned by text baseline */
}
```

### 📏 Spacing & Wrapping

**Adding space between items:**
```css
.container {
  display: flex;
  gap: 20px;         /* Equal space between items */
  /* row-gap: 20px;  /* Space between rows */
  /* column-gap: 20px; /* Space between columns */
}
```

**Controlling wrapping behavior:**
```css
.container {
  display: flex;
  flex-wrap: nowrap;       /* Default - single line */
  /* flex-wrap: wrap;      /* Multiple lines if needed */
  /* flex-wrap: wrap-reverse; /* Multiple lines, reversed */
}
```

### 🧵 Individual Item Properties

Control how individual items behave within a flex container:

```css
.item {
  flex-grow: 0;    /* Default - don't grow */
  /* flex-grow: 1;  /* Grow to fill available space */
  
  flex-shrink: 1;  /* Default - can shrink if needed */
  /* flex-shrink: 0;  /* Don't shrink */
  
  flex-basis: auto;  /* Default size before growing/shrinking */
  
  /* Shorthand for all three: */
  /* flex: 0 1 auto;  /* Default (don't grow, can shrink, auto basis) */
  /* flex: 1;         /* Grow and shrink equally from auto basis */
  
  order: 0;        /* Default - follows source order */
  /* order: 1;      /* Appears later in visual order */
  /* order: -1;     /* Appears earlier in visual order */
  
  align-self: auto;  /* Default - follows container's align-items */
  /* align-self: flex-start;  /* Override for individual item */
}
```

### 🌐 Real-World Examples

**1. Navbar with logo and links:**
```css
.navbar {
  display: flex;
  justify-content: space-between;  /* Logo left, links right */
  align-items: center;            /* Vertically centered */
  padding: 0 20px;
}

.nav-links {
  display: flex;
  gap: 20px;  /* Space between each link */
}
```

**2. Centered card with fixed width:**
```css
.card-container {
  display: flex;
  justify-content: center;  /* Center horizontally */
  align-items: center;      /* Center vertically */
  min-height: 100vh;        /* Full viewport height */
}

.card {
  width: 300px;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}
```

**3. Equal-height columns:**
```css
.features {
  display: flex;
  gap: 20px;
}

.feature-card {
  flex: 1;  /* Each card gets equal width */
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
}
```

### ✅ Day 8 Practice Challenge

**Build a flexible pricing table layout:**
- Create 3 pricing cards in a row
- Each card should have the same height regardless of content
- Highlight the middle "recommended" card (make it slightly larger)
- Cards should stack vertically on mobile screens
- Add a sticky header to each card
- Align the "Buy Now" buttons to the bottom of each card

**Checklist:**
- [ ] Set up container with display: flex
- [ ] Use appropriate justify-content for spacing
- [ ] Make cards equal width with flex: 1
- [ ] Apply gap between cards
- [ ] Use flex-direction: column for the card contents
- [ ] Position "Buy Now" buttons at the bottom using margin-top: auto
- [ ] Test how it looks at different screen widths

## 🧱 Day 9: CSS Grid – Mastering Complex Layouts

> "If Flexbox is one-dimensional layout, Grid is two-dimensional layout on steroids. It's the most powerful layout system CSS has ever had."

### ✨ What is CSS Grid?

CSS Grid Layout is a two-dimensional layout system that lets you create complex layouts with rows AND columns simultaneously. Perfect for:

- Page layouts with multiple sections
- Photo galleries
- Dashboard interfaces
- Magazine-style layouts
- Any design with complex alignment needs

### 🛠️ How to Use CSS Grid

**Step 1: Activate Grid on parent container**
```css
.container {
  display: grid;
}
```

**Step 2: Define your grid structure**
```css
.container {
  display: grid;
  grid-template-columns: 200px 1fr 200px;  /* 3 columns */
  grid-template-rows: 100px auto 100px;    /* 3 rows */
  gap: 20px;                              /* Space between grid cells */
}
```

### 📐 Sizing Grid Tracks

CSS Grid introduces powerful sizing options:

```css
.container {
  display: grid;
  
  /* Fixed size columns */
  grid-template-columns: 100px 200px 100px;
  
  /* Flexible size with fr unit */
  grid-template-columns: 1fr 2fr 1fr;  /* Proportional widths */
  
  /* Mixed units */
  grid-template-columns: 200px 1fr 2fr;
  
  /* Auto size based on content */
  grid-template-columns: auto 1fr auto;
  
  /* Repeat pattern */
  grid-template-columns: repeat(3, 1fr);  /* 3 equal columns */
  grid-template-columns: repeat(2, 100px 1fr);  /* Pattern repeats: 100px, 1fr, 100px, 1fr */
  
  /* Min/max sizing for responsiveness */
  grid-template-columns: repeat(3, minmax(100px, 1fr));
}
```

### 🏁 Positioning Items in the Grid

**By line numbers:**
```css
.item {
  /* Format: grid-column: start / end; */
  grid-column: 1 / 3;  /* Start at line 1, end at line 3 (spans 2 columns) */
  grid-row: 2 / 4;     /* Start at line 2, end at line 4 (spans 2 rows) */
  
  /* Shorthand: */
  /* grid-area: row-start / column-start / row-end / column-end; */
  grid-area: 2 / 1 / 4 / 3;  /* Same as above combined */
}
```

**Using span keyword:**
```css
.item {
  grid-column: 1 / span 2;  /* Start at line 1, span 2 columns */
  grid-row: 2 / span 2;     /* Start at line 2, span 2 rows */
}
```

### 🌟 Named Grid Areas

Create visual layouts directly in your CSS:

```css
.container {
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "header header header"
    "nav    main   sidebar"
    "footer footer footer";
  gap: 20px;
}

.header { grid-area: header; }
.nav { grid-area: nav; }
.main { grid-area: main; }
.sidebar { grid-area: sidebar; }
.footer { grid-area: footer; }
```

### ⚖️ Alignment in Grid

Just like Flexbox, Grid has powerful alignment properties:

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  
  /* Align all items horizontally within their cells */
  justify-items: stretch;  /* Default - fill width */
  /* justify-items: start; */
  /* justify-items: end; */
  /* justify-items: center; */
  
  /* Align all items vertically within their cells */
  align-items: stretch;  /* Default - fill height */
  /* align-items: start; */
  /* align-items: end; */
  /* align-items: center; */
  
  /* Align the entire grid horizontally within container */
  justify-content: start;  /* Default */
  /* justify-content: end; */
  /* justify-content: center; */
  /* justify-content: space-between; */
  /* justify-content: space-around; */
  
  /* Align the entire grid vertically within container */
  align-content: start;  /* Default */
  /* align-content: end; */
  /* align-content: center; */
  /* align-content: space-between; */
  /* align-content: space-around; */
}

/* For individual items, override the container's alignment */
.item {
  justify-self: center;
  align-self: center;
}
```

### 🌐 Real-World Examples

**1. Classic website layout:**
```css
.site-layout {
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;
  grid-template-areas:
    "header header header"
    "nav    main   sidebar"
    "footer footer footer";
  gap: 20px;
  min-height: 100vh;
}
```

**2. Photo gallery:**
```css
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 20px;
}

.gallery-item:nth-child(4n+1) {
  grid-column: span 2;
  grid-row: span 2;
}
```

**3. Dashboard layout:**
```css
.dashboard {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: auto auto 1fr;
  gap: 15px;
  height: 100vh;
}

.header {
  grid-column: 1 / -1;  /* Span all columns */
}

.stats {
  grid-column: 1 / 3;
}

.notifications {
  grid-column: 3 / -1;
}

.main-chart {
  grid-column: 1 / -1;
}
```

### ✅ Day 9 Practice Challenge

**Build a blog homepage layout:**
- Create a grid-based layout with header, navigation, featured post, sidebar, and footer
- The featured post should span multiple grid cells
- Include a gallery of article cards (at least 6) in a responsive grid
- Implement proper spacing between all elements
- Make the layout adapt to different screen sizes

**Checklist:**
- [ ] Set up container with display: grid
- [ ] Define grid areas with meaningful names
- [ ] Create responsive column sizing with minmax()
- [ ] Position at least one item to span multiple cells
- [ ] Use appropriate gap between grid items
- [ ] Test the layout at different screen widths

## 📱 Day 10: Responsive Design – Adapting to Any Screen

> "In 2025, responsive design isn't optional—it's expected. Your websites need to look good on everything from 4K monitors to folding phones."

### 📏 Understanding Responsive Design

Responsive design means creating websites that look good on all devices by adapting the layout and content to the screen size. It's built on three core principles:

1. **Fluid layouts** that use relative units
2. **Media queries** that apply different styles at different breakpoints
3. **Flexible images** that scale appropriately

### 📐 Responsive Units (Use These Instead of Pixels)

```css
/* Relative to parent element */
.container {
  width: 80%;        /* Percentage of parent width */
}

/* Relative to font size */
.element {
  margin-bottom: 1.5em;  /* 1.5x the font size of this element */
  padding: 1.25rem;      /* 1.25x the root element's font size */
}

/* Relative to viewport */
.hero {
  height: 80vh;      /* 80% of viewport height */
  width: 90vw;       /* 90% of viewport width */
  padding: 5vmin;    /* 5% of the viewport's smaller dimension */
}

/* Grid-specific */
.grid {
  grid-template-columns: repeat(3, 1fr);  /* Three equal-width columns */
}
```

### 📱 Media Queries – The Heart of Responsive Design

Media queries let you apply CSS conditionally based on device characteristics:

```css
/* Basic structure */
@media media-type and (condition) {
  /* CSS rules to apply when condition is true */
}

/* Common media queries */

/* Mobile-first approach (recommended) */
/* Base styles for mobile devices (outside media queries) */

/* For tablets and up */
@media screen and (min-width: 768px) {
  .container {
    display: flex;
  }
}

/* For desktops and up */
@media screen and (min-width: 1024px) {
  .container {
    max-width: 1200px;
    margin: 0 auto;
  }
}

/* Desktop-first approach (alternative) */
/* Base styles for desktops (outside media queries) */

/* For tablets and down */
@media screen and (max-width: 1023px) {
  .container {
    padding: 15px;
  }
}

/* For mobile devices */
@media screen and (max-width: 767px) {
  .menu {
    flex-direction: column;
  }
}
```

### 🧙‍♂️ Advanced Media Query Features

```css
/* Testing device orientation */
@media screen and (orientation: landscape) {
  .gallery {
    flex-direction: row;
  }
}

/* Testing for hover capability */
@media (hover: hover) {
  .button:hover {
    background-color: #0056b3;
  }
}

/* Dark mode detection */
@media (prefers-color-scheme: dark) {
  :root {
    --bg-color: #121212;
    --text-color: #f5f5f5;
  }
}

/* Reducing motion for accessibility */
@media (prefers-reduced-motion: reduce) {
  * {
    animation: none !important;
    transition: none !important;
  }
}

/* High-resolution screens (e.g., Retina displays) */
@media (min-resolution: 2dppx) {
  .logo {
    background-image: url('logo@2x.png');
  }
}
```

### 📊 Breakpoint Strategy

Decide on a consistent set of breakpoints for your project:

```css
/* Example breakpoint system */
:root {
  --breakpoint-sm: 576px;   /* Small devices (phones) */
  --breakpoint-md: 768px;   /* Medium devices (tablets) */
  --breakpoint-lg: 992px;   /* Large devices (desktops) */
  --breakpoint-xl: 1200px;  /* Extra large devices */
  --breakpoint-xxl: 1400px; /* Super large screens */
}

/* Usage */
@media screen and (min-width: var(--breakpoint-md)) {
  /* Tablet styles */
}
```

**Pro tip:** Don't only base breakpoints on devices, but on where your design breaks!

### 🖼️ Responsive Images & Media

```css
/* Basic responsive image */
img {
  max-width: 100%;
  height: auto;
}

/* Art direction with <picture> element */
<picture>
  <source media="(min-width: 1024px)" srcset="image-large.jpg">
  <source media="(min-width: 768px)" srcset="image-medium.jpg">
  <img src="image-small.jpg" alt="Responsive image">
</picture>

/* Responsive videos */
.video-container {
  position: relative;
  width: 100%;
  padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
}

.video-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
```

### 📱 Mobile-First vs Desktop-First

**Mobile-First (Recommended):**
1. Write base styles for mobile devices
2. Use `min-width` media queries to enhance for larger screens
3. Benefits: Forces you to prioritize content, typically results in leaner code

```css
/* Mobile styles (default) */
.card {
  width: 100%;
}

/* Tablet and up */
@media screen and (min-width: 768px) {
  .card {
    width: 48%;
  }
}

/* Desktop and up */
@media screen and (min-width: 1024px) {
  .card {
    width: 30%;
  }
}
```

**Desktop-First (Alternative):**
1. Write base styles for desktop devices
2. Use `max-width` media queries to adapt for smaller screens
3. May be better for desktop-heavy applications or complex UIs that need to be simplified for mobile

```css
/* Desktop styles (default) */
.card {
  width: 30%;
}

/* Tablet and down */
@media screen and (max-width: 1023px) {
  .card {
    width: 48%;
  }
}

/* Mobile and down */
@media screen and (max-width: 767px) {
  .card {
    width: 100%;
  }
}
```

### 🌐 Real-World Examples

**1. Responsive navigation:**
```css
/* Mobile-first navigation */
.nav {
  display: flex;
  flex-direction: column;
}

.nav-toggle {
  display: block; /* Show hamburger menu on mobile */
}

/* Desktop navigation */
@media screen and (min-width: 768px) {
  .nav {
    flex-direction: row;
  }
  
  .nav-toggle {
    display: none; /* Hide hamburger menu on desktop */
  }
}
```

**2. Card layout that adapts:**
```css
.card-grid {
  display: grid;
  gap: 20px;
  grid-template-columns: 1fr;  /* One column on mobile */
}

@media screen and (min-width: 576px) {
  .card-grid {
    grid-template-columns: repeat(2, 1fr);  /* Two columns on tablets */
  }
}

@media screen and (min-width: 992px) {
  .card-grid {
    grid-template-columns: repeat(3, 1fr);  /* Three columns on desktop */
  }
}

@media screen and (min-width: 1200px) {
  .card-grid {
    grid-template-columns: repeat(4, 1fr);  /* Four columns on large screens */
  }
}
```

**3. Font size adjustment:**
```css
:root {
  font-size: 16px;  /* Base font size for mobile */
}

@media screen and (min-width: 768px) {
  :root {
    font-size: 18px;  /* Larger base font for tablets */
  }
}

@media screen and (min-width: 1200px) {
  :root {
    font-size: 20px;  /* Even larger for big screens */
  }
}

/* Now all rem units will scale proportionally */
h1 { font-size: 2rem; }
p { font-size: 1rem; }
```

### ✅ Day 10 Practice Challenge

**Make a responsive portfolio layout:**
- Create a header with navigation that converts to a hamburger menu on mobile
- Design a grid of portfolio projects that changes columns based on screen size
- Include a sidebar that moves below the main content on small screens
- Ensure text is readable on all devices without horizontal scrolling
- Optimize images for different screen sizes

**Checklist:**
- [ ] Use relative units (%, rem, vh/vw) for layout
- [ ] Create at least 3 media queries for different screen sizes
- [ ] Test how text and images respond to different viewport widths
- [ ] Ensure navigation is usable on both mobile and desktop
- [ ] Verify all content remains accessible on small screens
- [ ] Check that your layout doesn't break at any common screen width

🌀 Day 11: Transitions & Animations
transition: all 0.3s ease;

```css
/* Basic transitions */
.button {
  background-color: #3498db;
  color: white;
  padding: 10px 20px;
  border-radius: 4px;
  transition: all 0.3s ease;
  /* can also specify individual properties */
  /* transition: background-color 0.3s ease, transform 0.2s ease-out; */
}

.button:hover {
  background-color: #2980b9;
  transform: translateY(-2px);
}

/* Transition timing functions */
.ease { transition-timing-function: ease; }
.linear { transition-timing-function: linear; }
.ease-in { transition-timing-function: ease-in; }
.ease-out { transition-timing-function: ease-out; }
.ease-in-out { transition-timing-function: ease-in-out; }
.custom { transition-timing-function: cubic-bezier(0.68, -0.55, 0.27, 1.55); }
```

@keyframes and animation properties

```css
/* Basic animation */
@keyframes slide-in {
  0% {
    transform: translateX(-100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}

.animated-element {
  animation: slide-in 1s ease-out forwards;
  /* animation shorthand: name duration timing-function delay iteration-count direction fill-mode */
}

/* Complex animation with multiple steps */
@keyframes pulse-and-rotate {
  0% {
    transform: scale(1) rotate(0deg);
    background-color: #3498db;
  }
  50% {
    transform: scale(1.2) rotate(180deg);
    background-color: #e74c3c;
  }
  100% {
    transform: scale(1) rotate(360deg);
    background-color: #3498db;
  }
}

.fancy-animation {
  width: 100px;
  height: 100px;
  background-color: #3498db;
  animation: pulse-and-rotate 3s infinite ease-in-out;
}
```

transform: scale(), rotate(), translateX()

```css
/* Transforms */
.scale {
  transform: scale(1.5); /* 150% of original size */
}

.rotate {
  transform: rotate(45deg); /* 45-degree rotation */
}

.translate {
  transform: translateX(50px) translateY(20px); /* Move right 50px, down 20px */
  /* Shorthand: transform: translate(50px, 20px); */
}

.skew {
  transform: skewX(15deg) skewY(5deg);
}

/* Combining transforms (applied right-to-left) */
.combined {
  transform: translateX(50px) rotate(45deg) scale(1.5);
}

/* Transform origin */
.rotate-corner {
  transform-origin: top left; /* Rotate around top-left corner */
  transform: rotate(45deg);
}
```

🧠 Animate a button hover and loading spinner.

```css
/* Loading spinner animation */
.spinner {
  width: 40px;
  height: 40px;
  border: 4px solid rgba(0, 0, 0, 0.1);
  border-radius: 50%;
  border-top-color: #3498db;
  animation: spin 1s infinite linear;
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
```

🧬 Day 12: Advanced CSS – Custom Properties & SCSS
CSS Variables:

```css
/* CSS Custom Properties (Variables) */
:root {
  --main-color: #ff6600;
  --secondary-color: #333;
  --padding-standard: 15px;
  --border-radius: 4px;
  --font-heading: 'Georgia', serif;
}

.button {
  background-color: var(--main-color);
  padding: var(--padding-standard);
  border-radius: var(--border-radius);
}

.card {
  border: 1px solid var(--secondary-color);
  padding: calc(var(--padding-standard) * 2);
}

/* Changing variables with media queries */
@media (prefers-color-scheme: dark) {
  :root {
    --main-color: #ff9933;
    --secondary-color: #eee;
  }
}
```

Use with: color: var(--main-color)

SCSS Syntax: Nesting, Mixins, Loops

```scss
// SCSS Variables
$primary-color: #3498db;
$secondary-color: #2c3e50;
$border-radius: 4px;

// SCSS Nesting
.card {
  background-color: white;
  border-radius: $border-radius;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  
  .card-header {
    background-color: $primary-color;
    color: white;
    padding: 15px;
    
    h2 {
      margin: 0;
      font-size: 1.5rem;
    }
  }
  
  .card-body {
    padding: 15px;
    
    p {
      line-height: 1.6;
      margin-bottom: 15px;
      
      &:last-child {
        margin-bottom: 0;
      }
    }
  }
}

// SCSS Mixin
@mixin flex-center {
  display: flex;
  align-items: center;
  justify-content: center;
}

.centered-content {
  @include flex-center;
  height: 100vh;
}

// SCSS Mixin with parameters
@mixin button-style($bg-color, $text-color) {
  background-color: $bg-color;
  color: $text-color;
  padding: 10px 20px;
  border-radius: $border-radius;
  border: none;
  cursor: pointer;
  
  &:hover {
    background-color: darken($bg-color, 10%);
  }
}

.primary-button {
  @include button-style($primary-color, white);
}

.secondary-button {
  @include button-style($secondary-color, white);
}

// SCSS Loop
$space-amounts: (5, 10, 15, 20, 25, 30);

@each $space in $space-amounts {
  .m-#{$space} { margin: #{$space}px; }
  .mt-#{$space} { margin-top: #{$space}px; }
  .mb-#{$space} { margin-bottom: #{$space}px; }
  .p-#{$space} { padding: #{$space}px; }
  .pt-#{$space} { padding-top: #{$space}px; }
  .pb-#{$space} { padding-bottom: #{$space}px; }
}
```

Setup SCSS with live Sass compiler

🧹 Day 13: CSS Reset, Normalize & Specificity
Resetting browser styles using * { margin: 0; padding: 0; }

```css
/* Simple CSS Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* More comprehensive reset */
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}

/* Modern reset with accessibility considerations */
body {
  min-height: 100vh;
  scroll-behavior: smooth;
  text-rendering: optimizeSpeed;
  line-height: 1.5;
}

ul, ol {
  list-style: none;
}

a {
  text-decoration: none;
  color: inherit;
}

img {
  max-width: 100%;
  display: block;
}
```

Normalize vs Reset

```css
/* Normalize.css (snippet - this preserves useful defaults) */
html {
  line-height: 1.15;
  -webkit-text-size-adjust: 100%;
}

body {
  margin: 0;
}

main {
  display: block;
}

h1 {
  font-size: 2em;
  margin: 0.67em 0;
}

/* See normalize.css for full implementation */
```

CSS Specificity rules

```css
/* Specificity examples */

/* Specificity: 1 */
p {
  color: blue;
}

/* Specificity: 10 */
.text {
  color: red; /* This overrides element selector */
}

/* Specificity: 100 */
#unique {
  color: green; /* This overrides class selector */
}

/* Specificity: 11 (1 class + 1 element) */
.text p {
  color: purple;
}

/* Specificity: 1 + !important */
p {
  color: orange !important; /* This overrides everything */
}

/* Inline styles (Specificity: 1000) */
<p style="color: pink;">Inline styled text</p>
```

Inline > ID > Class > Element

Importance of clean and manageable code

```css
/* Bad: Hard to maintain, high specificity */
.container .content .section ul.features li.feature-item span.highlight {
  color: red;
}

/* Better: Flatter hierarchy, easier to override when needed */
.feature-highlight {
  color: red;
}
```

🧰 Day 14: Real World Add-ons
Scroll Snap: scroll-snap-type, scroll-padding

```css
/* Basic scroll snap */
.container {
  height: 100vh;
  overflow-y: scroll;
  scroll-snap-type: y mandatory;
}

.section {
  height: 100vh;
  scroll-snap-align: start;
}

/* With padding for fixed headers */
.container-with-header {
  height: 100vh;
  overflow-y: scroll;
  scroll-snap-type: y mandatory;
  scroll-padding-top: 80px; /* Height of fixed header */
}
```

Sticky footers and headers

```css
/* Sticky footer with flexbox */
body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  margin: 0;
}

main {
  flex: 1; /* Takes up all available space */
}

footer {
  padding: 20px;
  background-color: #333;
  color: white;
}

/* Sticky header */
header {
  position: sticky;
  top: 0;
  background-color: white;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  z-index: 1000;
}
```

Button styles, toggle switches

```css
/* Modern button */
.button {
  display: inline-block;
  padding: 12px 24px;
  background-color: #3498db;
  color: white;
  border: none;
  border-radius: 4px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 1px;
  cursor: pointer;
  box-shadow: 0 2px 5px rgba(0,0,0,0.2);
  transition: all 0.3s ease;
}

.button:hover {
  background-color: #2980b9;
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.button:active {
  transform: translateY(0);
  box-shadow: 0 1px 3px rgba(0,0,0,0.2);
}

/* Toggle switch */
.switch {
  position: relative;
  display: inline-block;
  width: 60px;
  height: 34px;
}

.switch input { 
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  transition: .4s;
  border-radius: 34px;
}

.slider:before {
  position: absolute;
  content: "";
  height: 26px;
  width: 26px;
  left: 4px;
  bottom: 4px;
  background-color: white;
  transition: .4s;
  border-radius: 50%;
}

input:checked + .slider {
  background-color: #2196F3;
}

input:checked + .slider:before {
  transform: translateX(26px);
}
```

Image maps, fieldset, legend usage

```css
/* Styled fieldset and legend */
fieldset {
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 15px;
  margin-bottom: 20px;
}

legend {
  padding: 0 10px;
  font-weight: bold;
  color: #555;
}

/* Responsive image map */
.img-map-container {
  position: relative;
  max-width: 100%;
}

.img-map-container img {
  width: 100%;
  height: auto;
}

.img-map-container .hotspot {
  position: absolute;
  width: 20px;
  height: 20px;
  background-color: rgba(52, 152, 219, 0.7);
  border-radius: 50%;
  cursor: pointer;
  transition: all 0.3s ease;
}

.img-map-container .hotspot:hover {
  transform: scale(1.5);
  background-color: rgba(41, 128, 185, 0.9);
}
```

iframe and embed tags

```css
/* Responsive iframe */
.iframe-container {
  position: relative;
  overflow: hidden;
  width: 100%;
  padding-top: 56.25%; /* 16:9 Aspect Ratio */
}

.iframe-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
  border: none;
}
```

🚀 Day 15: Final Projects
Now, show off everything you learned with hands-on projects:

Responsive Personal Portfolio

```css
/* Portfolio project snippet */
/* Common styles for the personal portfolio */
:root {
  --primary-color: #5c6bc0;
  --secondary-color: #ff7043;
  --dark-bg: #2c3e50;
  --light-bg: #f5f7fa;
  --text-color: #333;
  --light-text: #f5f5f5;
}

/* Layout */
.portfolio-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Hero section */
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  background-color: var(--dark-bg);
  color: var(--light-text);
  position: relative;
  overflow: hidden;
}

.hero::after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background: linear-gradient(135deg, rgba(92, 107, 192, 0.8), rgba(255, 112, 67, 0.8));
  z-index: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  max-width: 800px;
}

/* Projects grid */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 30px;
  padding: 50px 0;
}

.project-card {
  background-color: white;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 30px rgba(0,0,0,0.15);
}
```

Login/Signup Form UI

```css
/* Login form snippet */
.auth-container {
  max-width: 400px;
  margin: 50px auto;
  padding: 30px;
  border-radius: 8px;
  background-color: white;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  margin-bottom: 8px;
  font-weight: 600;
  color: #555;
}

.form-control {
  width: 100%;
  padding: 12px;
  border: 1px solid #ddd;
  border-radius: 4px;
  font-size: 16px;
  transition: border-color 0.3s;
}

.form-control:focus {
  border-color: #3498db;
  outline: none;
  box-shadow: 0 0 0 3px rgba(52,152,219,0.2);
}

.btn-submit {
  width: 100%;
  padding: 12px;
  background-color: #3498db;
  color: white;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.3s;
}

.btn-submit:hover {
  background-color: #2980b9;
}
```

Pricing Cards or Services Section

Blog Grid Layout

Interactive Navigation Menu

CSS-Only Image Slider

```css
/* CSS-only image slider */
.slider-container {
  width: 100%;
  overflow: hidden;
}

.slider {
  display: flex;
  width: 500%;  /* For 5 images */
  transition: transform 0.5s ease-in-out;
  animation: slide 20s infinite;
}

.slide {
  width: 20%;  /* 100% / 5 images */
}

.slide img {
  width: 100%;
  height: auto;
}

@keyframes slide {
  0% { transform: translateX(0); }
  20% { transform: translateX(0); }
  25% { transform: translateX(-20%); }
  45% { transform: translateX(-20%); }
  50% { transform: translateX(-40%); }
  70% { transform: translateX(-40%); }
  75% { transform: translateX(-60%); }
  95% { transform: translateX(-60%); }
  100% { transform: translateX(-80%); }
}
```

"The more you build, the more you understand. Don't wait to feel 'ready'. Get your hands dirty."

🧭 Bonus: What's Next After CSS?
JavaScript (DOM, Events, Logic)

React.js or Vue.js (Dynamic frontends)

Tailwind CSS or Bootstrap (Productivity in real-world)

Hosting (GitHub Pages, Netlify)

👋 Final Words from Mahendra
"CSS is not hard. It's just new. Once you break the fear and start writing a few lines daily, you'll love it. Don't rush — enjoy the small wins. Learn the flow. Style with your heart. This roadmap is not just for study, it's for your future."

