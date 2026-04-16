# Building a To-Do List Web Application

## Introduction
In this tutorial, we will create a simple To-Do List web application using HTML, CSS, and JavaScript. This application will allow users to add tasks, mark them as complete, and delete them. By the end of this tutorial, you will have a fully functional to-do list app.

## Prerequisites
- Basic knowledge of HTML, CSS, and JavaScript
- A text editor (like VSCode, Sublime Text, etc.)
- A browser (like Chrome, Firefox, etc.)

## Step 1: Set Up Your Project
1. Create a folder named `TodoListApp`.
2. Inside this folder, create three files: `index.html`, `style.css`, and `script.js`.

## Step 2: Create the HTML Structure
Open `index.html` and add the following code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>To-Do List App</title>
</head>
<body>
    <div class="container">
        <h1>To-Do List</h1>
        <input type="text" id="task-input" placeholder="Add a new task...">
        <button id="add-task">Add Task</button>
        <ul id="task-list"></ul>
    </div>
    <script src="script.js"></script>
</body>
</html>
``` 

## Step 3: Add Some Styles
Open `style.css` and add the following styles:
```css
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
}
.container {
    width: 300px;
    margin: auto;
    padding: 20px;
    background: white;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
h1 {
    text-align: center;
}
#task-input {
    width: calc(100% - 70px);
    padding: 10px;
    margin-bottom: 10px;
}
button {
    padding: 10px;
}
ul {
    list-style-type: none;
    padding: 0;
}
li {
    padding: 10px;
    background-color: #e6e6e6;
    margin-bottom: 10px;
    display: flex;
    justify-content: space-between;
}
li.completed {
    text-decoration: line-through;
    background-color: #d3ffd3;
}
``` 

## Step 4: Implement JavaScript Functionality
Open `script.js` and add the following code:
```javascript
document.getElementById('add-task').addEventListener('click', function() {
    const taskInput = document.getElementById('task-input');
    const taskText = taskInput.value.trim();
    if (taskText === '') return;

    const li = document.createElement('li');
    li.textContent = taskText;
    li.addEventListener('click', function() {
        li.classList.toggle('completed');
    });
    li.addEventListener('dblclick', function() {
        li.remove();
    });
    document.getElementById('task-list').appendChild(li);
    taskInput.value = '';
});
```

## Step 5: Test the Application
1. Open `index.html` in your browser.
2. Add tasks using the input field and clicking the 'Add Task' button.
3. Click on a task to mark it as complete (will be displayed with a strikethrough).
4. Double-click on a task to delete it.

## Conclusion
Congratulations! You've created a simple To-Do List application using HTML, CSS, and JavaScript. Feel free to enhance this application by adding more features like saving tasks in local storage or adding deadlines to tasks.