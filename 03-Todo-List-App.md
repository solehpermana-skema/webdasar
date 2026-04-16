# Aplikasi Todo List Web

Aplikasi Todo List adalah aplikasi berbasis web yang memungkinkan pengguna untuk mengelola daftar tugas mereka. Dalam dokumentasi ini, kita akan membahas struktur HTML, styling CSS modern, fungsi JavaScript untuk menambahkan/menghapus/m menyelesaikan tugas, dan penerapan Local Storage. Berikut adalah langkah-langkah untuk membuat aplikasi Todo List.

## Struktur Formulir HTML

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Aplikasi Todo List</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="todo-app">
        <h1>Daftar Tugas</h1>
        <form id="todo-form">
            <input type="text" id="todo-input" placeholder="Tambah Tugas..." required>
            <button type="submit">Tambah</button>
        </form>
        <ul id="todo-list"></ul>
    </div>
    <script src="scripts.js"></script>
</body>
</html>
```

## Gaya CSS Modern

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
}

div#todo-app {
    max-width: 600px;
    margin: 50px auto;
    padding: 20px;
    background: #fff;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    border-radius: 8px;
}

form {
    display: flex;
    justify-content: space-between;
}

input[type="text"] {
    flex: 1;
    padding: 10px;
    border: 2px solid #ddd;
    border-radius: 4px;
}

button {
    padding: 10px 15px;
    background: #5cb85c;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background: #4cae4c;
}

li.completed {
    text-decoration: line-through;
    color: #999;
}
```

## Fungsi JavaScript

```javascript
// Mendapatkan elemen DOM
const todoForm = document.getElementById('todo-form');
const todoInput = document.getElementById('todo-input');
const todoList = document.getElementById('todo-list');

// Mendapatkan tugas dari Local Storage
let todos = JSON.parse(localStorage.getItem('todos')) || [];

// Memperbarui tampilan daftar tugas
function renderTodos() {
    todoList.innerHTML = '';
    todos.forEach((todo, index) => {
        const li = document.createElement('li');
        li.textContent = todo.text;
        li.className = todo.completed ? 'completed' : '';
        li.addEventListener('click', () => toggleComplete(index));
        todoList.appendChild(li);
    });
}

// Menambahkan tugas
todoForm.addEventListener('submit', (event) => {
    event.preventDefault();
    const todoText = todoInput.value;
    todos.push({ text: todoText, completed: false });
    todoInput.value = '';
    saveToLocalStorage();
    renderTodos();
});

// Menyimpan ke Local Storage
function saveToLocalStorage() {
    localStorage.setItem('todos', JSON.stringify(todos));
}

// Mengganti status tugas
function toggleComplete(index) {
    todos[index].completed = !todos[index].completed;
    saveToLocalStorage();
    renderTodos();
}

// Menampilkan daftar tugas saat aplikasi dimuat
renderTodos();
```

## Langkah-langkah Membuat Aplikasi Todo List

1. **Persiapkan Struktur HTML**: Buat file `index.html` dan salin struktur HTML di atas.
2. **Buat CSS**: Buat file `styles.css` dan salin gaya CSS di atas.
3. **Implementasikan JavaScript**: Buat file `scripts.js` dan salin kode JavaScript di atas.
4. **Jalankan Aplikasi**: Buka `index.html` di browser Anda dan mulai menambahkan tugas.
5. **Simpan Tugas**: Setelah menambahkan tugas, mereka akan disimpan di Local Storage, sehingga tetap ada meskipun aplikasi direload.

Dengan mengikuti langkah-langkah di atas, Anda dapat membuat aplikasi Todo List yang fungsional dan modern menggunakan HTML, CSS, dan JavaScript.