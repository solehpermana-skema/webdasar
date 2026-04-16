# Tutorial: Creating a Photo Gallery using HTML, CSS, and JavaScript

## Introduction  
In this tutorial, we will create a simple photo gallery using HTML for structure, CSS for styling, and JavaScript for functionality.

## Prerequisites  
- Basic knowledge of HTML, CSS, and JavaScript.

## Step 1: Setting Up the HTML  
First, create an HTML file named `index.html` and add the following code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Photo Gallery</title>
</head>
<body>
    <div class="gallery">
        <img src="img1.jpg" alt="Image 1">
        <img src="img2.jpg" alt="Image 2">
        <img src="img3.jpg" alt="Image 3">
        <!-- Add more images as needed -->
    </div>
    <script src="script.js"></script>
</body>
</html>
```

## Step 2: Adding CSS Styles  
Next, create a CSS file named `styles.css` with the following code:
```css
body {
    font-family: Arial, sans-serif;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 10px;
}

.gallery img {
    width: 100%;
    height: auto;
    border-radius: 5px;
    transition: transform 0.2s;
}

.gallery img:hover {
    transform: scale(1.05);
}
```

## Step 3: Adding JavaScript Functionality  
Finally, create a JavaScript file named `script.js` and add the following code:
```javascript
// You can add interactive functionality here if needed
console.log('Photo Gallery loaded');
```

## Conclusion  
You have successfully created a simple photo gallery using HTML, CSS, and JavaScript. Customize it further by adding more styles and functionalities!
