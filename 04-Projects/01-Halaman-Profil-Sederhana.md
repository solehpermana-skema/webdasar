# Tutorial: Creating a Simple Profile Page using HTML, CSS, and JavaScript

## Introduction
In this tutorial, we'll create a simple profile page using HTML, CSS, and JavaScript. This page will display user information such as name, profile picture, and a brief description.

## Prerequisites
Make sure you have a basic understanding of HTML, CSS, and JavaScript.

## Step 1: Setting Up Your HTML
Create an HTML file named `index.html`. This file will structure our profile page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profile Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="profile-container">
        <img src="profile.jpg" alt="Profile Picture" class="profile-img">
        <h1 class="profile-name">John Doe</h1>
        <p class="profile-description">Web Developer and Designer</p>
        <button id="editBtn">Edit Profile</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

## Step 2: Adding CSS
Create a CSS file named `styles.css` to style the profile page.

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.profile-container {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    text-align: center;
}

.profile-img {
    width: 150px;
    height: 150px;
    border-radius: 50%;
}

.profile-name {
    font-size: 24px;
    margin: 10px 0;
}

.profile-description {
    color: #555;
}

#editBtn {
    padding: 10px 15px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

#editBtn:hover {
    background-color: #0056b3;
}
```

## Step 3: Adding JavaScript Functionality
Create a JavaScript file named `script.js` to add interactivity.

```javascript
document.getElementById('editBtn').addEventListener('click', function() {
    alert('Edit profile functionality coming soon!');
});
```

## Conclusion
Now you have a simple profile page that you can expand upon. Feel free to customize it further and implement additional features as needed!