# Halaman Profil Sederhana

## Pendahuluan

Dokumentasi ini memberikan panduan langkah demi langkah untuk membuat halaman profil sederhana menggunakan HTML, CSS, dan JavaScript. Halaman ini akan mencakup struktur HTML dasar, styling CSS, dan interaksi JavaScript.

## Struktur HTML

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profil Sederhana</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Nama Anda</h1>
        <img src="profil.jpg" alt="Foto Profil" class="profil-gambar">
        <p>Deskripsi singkat tentang diri Anda.</p>
        <button id="infoButton">Lihat Info Tambahan</button>
        <div id="moreInfo" style="display: none;">
            <p>Informasi tambahan akan ditampilkan di sini.</p>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

## Styling CSS

Buat file `styles.css` dengan konten berikut untuk menambahkan gaya ke halaman:

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
    margin: 0;
    padding: 0;
}

.container {
    max-width: 600px;
    margin: auto;
    padding: 20px;
    background: white;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

.profil-gambar {
    width: 150px;
    border-radius: 50%;
}
```

## Interaktivitas JavaScript

Buat file `script.js` dengan konten berikut untuk menambahkan interaktivitas:

```javascript
document.getElementById('infoButton').onclick = function() {
    var moreInfo = document.getElementById('moreInfo');
    if (moreInfo.style.display === 'none') {
        moreInfo.style.display = 'block';
        this.innerText = 'Sembunyikan Info Tambahan';
    } else {
        moreInfo.style.display = 'none';
        this.innerText = 'Lihat Info Tambahan';
    }
};
```

## Langkah-langkah Membuat Halaman Profil
1. **Buat file HTML**: Salin dan tempel kode HTML di atas ke dalam file baru bernama `index.html`.
2. **Buat file CSS**: Salin dan tempel kode CSS ke dalam file baru bernama `styles.css`.
3. **Buat file JavaScript**: Salin dan tempel kode JavaScript ke dalam file baru bernama `script.js`.
4. **Gambar Profil**: Siapkan gambar profil dan simpan sebagai `profil.jpg` di direktori yang sama.
5. **Buka di Browser**: Buka file `index.html` di browser Anda untuk melihat hasilnya.

## Kesimpulan

Dengan mengikuti langkah-langkah di atas, Anda telah berhasil membuat halaman profil sederhana. Anda dapat menyesuaikan kontennya lebih lanjut dan menambahkan fitur sesuai kebutuhan.