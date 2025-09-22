Nama	:	Wahyu Andika
Nim	:	312410182
Kelas	:	TI. 24. A2
Mata Kuliah	:	Pemograman Web 1
Dosen Pengampu	:	Agung Nugroho, S.Kom., M.Kom

TUGAS PRAKTIKUM HTML DASAR

Jawab Pertanyaan Berikut :
1. Lakukan perubahan pada kode sesuai dengan keinginan anda, amati perubahannya adakah 
error ketika terjadi kesalahan penulisan tag? 
2. Apa perbedaan dari tag `<p>` dengan tag `<br>`,berikan penjelasannya! 
3. Apa perbedaan atribut title dan alt pada tag <img>, berikan penjelasannya! 
4. Untuk mengatur ukuran gambar, digunakan atribut width dan height. Agar tampilan gambar 
   proporsional sebaiknya kedua atribut tersebut diisi semua atau tidak? Berikan penjelasannya! 
5. Pada link tambahkan atribut target dengan nilai atribut bervariasi ( _blank, _self, _top, 
   _parent ), apa yang terjadi pada masing-masing nilai antribut tersebut?

   <!DOCTYPE html>
<html>

<head>
    <h1>Belajar Dasar HTML<h1>
</head> 
<body> 
    <p>Kami sedang belajar HTML dasar, pada matakuliah Pemrograman Web di Prodi 
Teknik Informatika Universitas Pelita Bangsa. Pelajaran pertama yang kami dapat 
adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar 
HTML.</p> 
        <h2>Paragraf pada HTML<h2>
    <>Ini merupakan sebuah paragraf yang terdiri dari beberapa kalimat yang saling 
mendukung sehingga menjadi satu kesatuan. Paragraf dibuat dengan menggunakan 
tag dasar html.</>
</body>  

<h3>Menambahkan Gambar</h3> 
<img src="upb.jpg" width="200" title="Logo Univeritas Pelita Bangsa">

<nav> 
href="lab1_tag_dasar.html">Dasar HTML</href=> 
< href="lab1_halaman2.html">Halaman 2</> 
<a href="http://www.google.com"></a> 
</nav> 
<hr>

1. Apa yang terjadi jika ada kesalahan penulisan tag?
HTML memang toleran terhadap error (error-tolerant), sehingga jika ada kesalahan penulisan tag (misalnya <h1> tidak ditutup, atribut salah, atau elemen salah tulis), browser tidak akan berhenti menampilkan halaman. Browser tetap mencoba merender sebisa mungkin.
Tapi konsekuensinya:
•	Tampilan jadi berantakan (heading, paragraf, gambar bisa tidak sesuai harapan).
•	Struktur dokumen invalid saat divalidasi dengan W3C Validator.
•	Aksesibilitas terganggu, screen reader bisa salah membaca.
•	SEO menurun, mesin pencari bisa salah mengindeks.
•	Pemeliharaan sulit, error kecil bisa menimbulkan bug besar dalam proyek besar.
Analisis : Inilah kenapa disiplin menulis HTML yang benar penting. Di industri, error kecil pada tag bisa berdampak pada user experience dan branding perusahaan.

2. Bedakan <p> dengan <br>.
•	<p> → digunakan untuk membuat paragraf penuh (block-level element). Browser otomatis memberi jarak (margin) di atas dan bawahnya.
•	<br> → digunakan untuk pindah baris saja (inline element), tanpa memulai blok baru.
Analisis kritis:
•	<p> lebih semantik dan baik untuk SEO + aksesibilitas.
•	<br> sebaiknya dipakai hanya untuk kebutuhan formatting (alamat, puisi).
•	Jadi, <p> untuk konten, <br> untuk layout sederhana.
•	
3. Apa perbedaan atribut title dan alt pada <img>?
•	alt (alternative text):
o	Ditampilkan jika gambar gagal dimuat.
o	Dibaca oleh screen reader untuk aksesibilitas.
o	Penting untuk SEO (mesin pencari mengenali isi gambar lewat alt).
•	title:
o	Ditampilkan sebagai tooltip saat kursor diarahkan ke gambar.
o	Lebih ke pengalaman pengguna, bukan pengganti utama.
 Analisis kritis: alt adalah wajib untuk web inklusif dan standar WCAG, sedangkan title hanya opsional.

4. Apakah width dan height harus diisi keduanya?
Tidak wajib. Kalau hanya salah satu diisi, browser menyesuaikan sisi lain proporsional dengan aspect ratio asli gambar.
•	Kalau isi keduanya tapi tidak sesuai rasio → gambar bisa distorsi.
•	Dalam web modern, lebih baik pakai CSS (max-width: 100%; height: auto;) agar gambar responsif.
Analisis kritis: Untuk layout konsisten, developer profesional biasanya hanya menetapkan width saja (misalnya 200px), dan biarkan height menyesuaikan otomatis.

5. Apa fungsi atribut target pada hyperlink?
•	_blank → buka link di tab baru (sering dipakai untuk link eksternal, harus aman dengan rel="noopener noreferrer").
•	_self → buka link di tab yang sama (default).
•	_top → buka link di jendela utama, menimpa semua frame.
•	_parent → buka link di parent frame (kalau pakai iframe).
Analisis kritis:
•	_blank bagus untuk eksternal tapi rawan tabnabbing attack kalau tanpa rel.
•	_self paling aman untuk navigasi internal.
•	_top dan _parent jarang dipakai di web modern.
Kesalahan pada Kode Kamu
Dari kode yang kamu kasih, ada beberapa kesalahan serius:
1.	Heading <h1> di dalam <head> →  salah. Heading hanya boleh ada di <body>.
2.	<head>
3.	    <h1>Belajar Dasar HTML<h1>
4.	</head>
→ Seharusnya <h1> pindah ke dalam <body>, dan tag penutup harus </h1>.
5.	Penutup tag salah di <h1> dan <h2>
Kamu tulis <h1>...<h1> dan <h2>...<h2> → salah.
→ Harusnya <h1>...</h1> dan <h2>...</h2>.
6.	Tag kosong <> ... </>
Tidak ada tag <></> dalam HTML →  invalid.
→ Seharusnya pakai <p>...</p>.
7.	Elemen <h3> di luar <body>
Kamu tulis <h3> setelah </body>. → salah. Semua konten harus ada di dalam <body>.
8.	Tag <nav> berisi link salah format
o	Kamu tulis:
o	href="lab1_tag_dasar.html">Dasar HTML</href=>
→ salah. Tidak ada tag <href>.
o	Harusnya:
o	<a href="lab1_tag_dasar.html">Dasar HTML</a>
9.	Link kosong ke Google
Kamu tulis:
10.	<a href="http://www.google.com"></a>
→  salah, karena tidak ada teks/link yang bisa diklik.

