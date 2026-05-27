# Technical Paper on HTML and CSS

# 1. Box Model

The CSS Box Model explains how every HTML element is displayed as a box.

The box model has 4 parts:

- Content
- Padding
- Border
- Margin

Example:

```css
div{
    width: 200px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
}
```

### Importance

- Helps control spacing
- Makes layouts neat
- Prevents elements from touching each other

---

# 2. Inline vs Block Elements

HTML elements are divided into inline and block elements.

## Block Elements

Block elements start on a new line and take full width.

Examples:

- `<div>`
- `<p>`
- `<h1>`

Example:

```html
<div>Hello</div>
<p>Welcome</p>
```

## Inline Elements

Inline elements stay in the same line and only take required width.

Examples:

- `<span>`
- `<a>`
- `<strong>`

Example:

```html
<span>Hello</span>
<a href="#">Link</a>
```

### Difference

| Block Elements | Inline Elements |
|---|---|
| Start on new line | Stay in same line |
| Take full width | Take required width |

---

# 3. Positioning: Relative and Absolute

CSS positioning is used to move elements.

## Relative Position

Moves the element from its normal position.

Example:

```css
.box{
    position: relative;
    left: 20px;
}
```

## Absolute Position

Places the element relative to its parent element.

Example:

```css
.box{
    position: absolute;
    top: 50px;
    right: 20px;
}
```

### Uses

- Navigation bars
- Popups
- Images and buttons

---

# 4. Common CSS Structural Classes

Structural classes help create webpage layouts.

Example:

```css
.container{
    width: 80%;
    margin: auto;
}

.row{
    display: flex;
}
```

### Uses

- Page structure
- Responsive layouts
- Organizing content

---

# 5. Common CSS Styling Classes

Styling classes improve the look of the webpage.

Example:

```css
.text-center{
    text-align: center;
}

.btn{
    background-color: blue;
    color: white;
}
```

### Benefits

- Reusable code
- Better design
- Cleaner CSS

---

# 6. CSS Specificity

CSS specificity decides which style is applied when multiple styles target the same element.

Priority:

1. Inline styles
2. ID selectors
3. Class selectors
4. Element selectors

Example:

```css
#title{
    color: red;
}

.heading{
    color: blue;
}

h1{
    color: green;
}
```

The text becomes red because ID has higher priority.

---

# 7. CSS Responsive Queries

Media queries help websites work properly on mobile, tablet, and desktop screens.

Example:

```css
@media (max-width: 768px){
    body{
        background-color: lightgray;
    }
}
```

### Benefits

- Mobile-friendly design
- Better user experience
- Responsive layouts

---

# 8. Flexbox and Grid

## Flexbox

Flexbox is used for arranging items in a row or column.

Example:

```css
.container{
    display: flex;
    justify-content: center;
}
```

### Advantages

- Easy alignment
- Flexible layouts
- Responsive design

---

## Grid

CSS Grid is used for creating rows and columns.

Example:

```css
.container{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
}
```

### Advantages

- Better page layouts
- Easy to manage sections
- Responsive structure

---

# 9. Common Header Meta Tags

Meta tags give information about the webpage.

Example:

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="HTML and CSS Tutorial">
```

### Purpose

- Responsive design
- SEO improvement
- Character support

---

# 10. Semantic HTML

Semantic HTML tags clearly describe the meaning of the content.

Examples:

- `<header>`
- `<main>`
- `<footer>`
- `<article>`

### Benefits

- Better readability
- Improved SEO
- Easy maintenance

---

# 11. CSS Variables

CSS variables store reusable values.

Example:

```css
:root{
    --primary-color: blue;
}

button{
    background-color: var(--primary-color);
}
```

### Benefits

- Reusable values
- Easy theme changes
- Cleaner CSS

---

# Conclusion

HTML and CSS are very important technologies in web development. HTML creates the structure of the webpage, and CSS improves its design and layout. Concepts like box model, positioning, flexbox, grid, and media queries help developers create responsive and professional websites.

---

# References
 
1. W3Schools HTML Tutorial  
2. W3Schools CSS Tutorial  
3. CSS Tricks – Flexbox Guide  
4. FreeCodeCamp Articles