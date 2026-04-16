# Galeri Foto

Galeri foto adalah sebuah komponen penting untuk menampilkan gambar di website. Pada tutorial ini, kita akan membuat galeri foto interaktif menggunakan HTML, CSS, dan JavaScript.

## 1. Struktur HTML
Kita akan mulai dengan membuat struktur HTML menggunakan grid layout untuk menampilkan gambar.

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Galeri Foto</title>
</head>
<body>
    <div class="gallery">
        <div class="gallery-item" onclick="openLightbox();currentSlide(1)">
            <img src="image1.jpg" alt="Gambar 1">
        </div>
        <div class="gallery-item" onclick="openLightbox();currentSlide(2)">
            <img src="image2.jpg" alt="Gambar 2">
        </div>
        <!-- Tambahkan lebih banyak item sesuai kebutuhan -->
    </div>

    <!-- Lightbox untuk menampilkan gambar lebih besar -->
    <div id="lightbox" class="lightbox">
        <span class="close" onclick="closeLightbox()">&times;</span>
        <div class="lightbox-content">
            <div class="mySlides">
                <img src="image1.jpg" alt="Gambar 1">
            </div>
            <div class="mySlides">
                <img src="image2.jpg" alt="Gambar 2">
            </div>
            <!-- Tambahkan lebih banyak slide sesuai kebutuhan -->
            <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
            <a class="next" onclick="plusSlides(1)">&#10095;</a>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
```

## 2. Styling CSS
Mari kita tambahkan CSS untuk mempercantik tampilan galeri kita.

```css
body {
    font-family: Arial, sans-serif;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 10px;
    padding: 10px;
}

.gallery-item img {
    width: 100%;
    border-radius: 8px;
    transition: transform 0.2s;
}

.gallery-item img:hover {
    transform: scale(1.05);
}

.lightbox {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgb(0,0,0);
    background-color: rgba(0,0,0,0.9);
}

.lightbox-content {
    position: relative;
    margin: auto;
    padding: 10px;
    max-width: 700px;
}

.mySlides {
    display: none;
}

img {
    max-width: 100%;
    height: auto;
}
```

## 3. JavaScript Lightbox Functionality
Sekarang kita tambahkan fungsionalitas JavaScript untuk mengatur lightbox.

```javascript
let slideIndex = 1;
showSlides(slideIndex);

function openLightbox() {
    document.getElementById('lightbox').style.display = "block";
}

function closeLightbox() {
    document.getElementById('lightbox').style.display = "none";
}

function plusSlides(n) {
    showSlides(slideIndex += n);
}

function currentSlide(n) {
    showSlides(slideIndex = n);
}

function showSlides(n) {
    let i;
    const slides = document.getElementsByClassName("mySlides");
    if (n > slides.length) {slideIndex = 1}
    if (n < 1) {slideIndex = slides.length}
    for (i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
    }
    slides[slideIndex - 1].style.display = "block";
}
```

## 4. Penjelasan Langkah
- Buat file HTML, CSS, dan JavaScript sesuai dengan kode di atas.
- Ganti `image1.jpg` dan `image2.jpg` dengan gambar yang Anda miliki.
- Simpan semua file tersebut dalam satu folder dan buka file HTML di browser untuk melihat hasilnya.

Dengan mengikuti langkah-langkah di atas, Anda dapat membuat galeri foto interaktif yang menarik.