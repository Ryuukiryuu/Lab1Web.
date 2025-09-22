**Nama   :** Wahyu Andika  
**NIM    :** 312410182  
**Kelas  :** TI.24.A2  
**Matkul :** Pemrograman Web 1  
**Dosen Pengampu :** Agung Nugroho, S.Kom., M.Kom


### 1. Apa yang terjadi jika ada kesalahan penulisan tag?

Pada file **`praktikum_salah.html`**, terlihat ada beberapa kesalahan, misalnya:

* Tag `<h1>` diletakkan di dalam `<head>`.
* Tag `<h2>` tidak ditutup dengan benar.
* Ada simbol `<>` nyasar sebelum paragraf.
* Struktur `<nav>` ditulis salah, sehingga link tidak muncul.

Hasilnya, browser tetap berusaha menampilkan halaman (karena HTML toleran terhadap error), tetapi tampilan menjadi tidak rapi: teks heading bercampur dengan paragraf, ada teks “<>” muncul, dan link navigasi tidak dapat digunakan.

**Kesimpulan:** Kesalahan penulisan tag tidak membuat halaman gagal total, tetapi menyebabkan tampilan tidak sesuai yang diharapkan.

### 2. Perbedaan `<p>` dengan `<br>`

Dalam **`praktikum_benar.html`**, paragraf ditulis dengan `<p>`:

```html
<p>Nama : Wahyu Andika</p>
<p>NIM : 312410182</p>
```

Setiap `<p>` menghasilkan blok paragraf baru dengan jarak otomatis di atas dan bawah.

Jika menggunakan `<br>` hasilnya hanya pindah baris, tanpa jarak tambahan. Contoh:

```html
<p>UNIVERSITAS PELITA BANGSA<br>MEGAH<br>CIKARANG</p>
```

**Kesimpulan:** `<p>` digunakan untuk paragraf utuh (struktur teks), sedangkan `<br>` hanya untuk pindah baris di dalam paragraf.

### 3. Perbedaan atribut `title` dan `alt` pada `<img>`

Pada **`praktikum_benar.html`**, gambar ditulis:

```html
<img src="upb.jpg" width="200" title="Logo Universitas Pelita Bangsa" alt="Logo UPB">
```

* **`alt="Logo UPB"`** → jika file `upb.jpg` hilang, browser akan menampilkan teks *Logo UPB*. Atribut ini juga dibaca screen reader, sehingga sangat penting untuk aksesibilitas.
* **`title="Logo Universitas Pelita Bangsa"`** → saat mouse diarahkan ke gambar, muncul tooltip dengan teks tersebut.

**Kesimpulan:** `alt` untuk menggantikan gambar saat tidak tampil, sedangkan `title` hanya memberi keterangan tambahan saat gambar tampil.

### 4. Agar proporsional, apakah `width` dan `height` harus diisi semua?

Di kode yang benar pada gambar ditulis:

```html
<img src="upb.jpg" width="200" ... >
```

Hanya `width` yang diisi, sementara `height` dibiarkan kosong. Hasilnya gambar tetap proporsional, karena browser otomatis menyesuaikan tinggi sesuai rasio asli.

Jika **kedua atribut (`width` dan `height`) diisi tetapi tidak sesuai rasio gambar**, maka gambar bisa terlihat gepeng atau melebar.

**Kesimpulan:** cukup isi salah satu atribut (biasanya `width`) agar gambar tetap proporsional, atau gunakan CSS (`max-width:100%; height:auto;`) untuk lebih fleksibel.

### 5. Perbedaan penggunaan `target="_blank"`, `_self`, `_top`, `_parent` pada link

Di bagian **`praktikum_benar.html`**, link ditulis seperti ini:

```html
<a href="http://www.google.com" target="_blank" rel="noopener noreferrer">
   Halaman Web Eksternal Google
</a>
```

* **`_blank`** → link Google terbuka di tab baru.
* **`_self`** → membuka link di tab yang sama (default, dipakai misalnya di link ke halaman YouTube).
* **`_top`** → membuka link di jendela penuh, menimpa semua frame (berguna jika pakai frameset).
* **`_parent`** → membuka link di frame induk, dipakai bila halaman ada dalam iframe.

menambahkan `rel="noopener noreferrer"` pada `_blank` → ini best practice untuk keamanan, agar tab baru tidak bisa mengakses halaman utama (mencegah tabnabbing).

**Kesimpulan:** pilihan target menentukan bagaimana navigasi berjalan. `_blank` cocok untuk link eksternal, `_self` untuk navigasi internal, sedangkan `_top` dan `_parent` relevan di halaman dengan frame/iframe.
