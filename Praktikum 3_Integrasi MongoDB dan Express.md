# BAB 2 Integrasi MongoDB dan Express

## LANGKAH PERCOBAAN
## Percobaan instalasi NodeJS
### 1. Buka halaman
### 2. Download dan jalankan node setup
### 3. Setelah instalasi selesai jalankan command <sub>node -v</sub> untuk memeriksa apakah NodeJS sudah terinstall
## Inisiasi project Express dan pemasangan package
### 1. Lakukan pembuatan folder dengan nama express-mongodb dan masuk ke dalam folder tersebut lalu buka melalui text editor masing-masing
### 2. Lakukan npm init untuk mengenerate file package .json dengan menggunakan command <sub>npm init -y</sub>
### 3. Lakukan instalasi express, mongoose, dan dotenv dengan menggunakan command <sub>npm i express mongoose dotenv</sub>
## Koneksi Express ke MongoDB
### 1. Buatlah file **index.js** pada root folder dan masukkan kode di bawah ini
Setelah itu coba jalankan aplikasi dengan command <sub>node index.js</sub>
>![Warning]
>Dikarenakan tidak menggunakan nodemon, maka setiap kali menyimpan perubahan file diharuskan untuk restart server node terlebih dahulu dengan menekan ctrl+c dan jalankan command <sub>node index.js</sub> lagi
### 2. Lakukan pembuatan file .env dan masukkan baris berikut
> PORT=5000
> Setelah itu ubahlah kode pada listening port menjadi berikut dan coba jalankan aplikasi kembali
>
### 3. Copy connection string yang terdapat pada compass atau atlas dan paste kan pada **.env** seperti berikut
### 4. Tambahkan baris kode berikut pada file **index.js**
Setelah itu coba jalankan aplikasi kembali
##Pembuatan routing
### 1. Lakukan pembuatan direktori routes di tingkat yang sama dengan index.js
### 2. Buatlah file book.route.js di dalamnya
### 3. Tambahkan baris kode berikut untuk fungsi getAllBooks
### 4. Lakukan hal yang sama untuk getOneBook createBook, updateBook, dan deleteBook
### 5. Uji salah satu endpoint dengan Postman
## Pembuatan controller
### 1. Lakukan pembuatan direktori controllers di tingkat yang sama dengan index.js
### 2. Buatlah file book.controller.js di dalamnya
### 3. Salin baris kode dari routes untuk fungsi getAllBooks
### 4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, deleteBooks
### 5. Lakukan import book.controller.js pada file book.route.js
### 6. Lakukan perubahan pada fungsi agar dapat memanggil fungsi dari book.controller.js
### 7. Lakukan pengujian kembali, pastikan response tetap sama
## Pembuatan model
Berikut adalah gambaran bentuk dari data dari modul sebelumnya
| title  | string |
| author | string |
| year   | number |
| pages  | number |
| summary | string |
| publisher | string |
### 1. Lakukan pembuatan direktori models di tingkat yang sama dengan index.js
### 2. Buatlah file book.model.js di dalamnya
### 3. Tambahkan baris kode berikut sesuai dengan tabel di atas
## Operasi CRUD
### 1. Hapus semua data pada collection books
### 2. Lakukan import book.model.js pada file book.controller.js
### 3. Lakukan perubahan pada fungsi createBook
### 4. Buatlah dua buah buku dengan data di bawah ini dengan Postman
### 5. Lakukan perubahan pada fungsi getAllBooks
### 6. Lakukan perubahan pada funsi getOneBook
### 7. Tampilkan semua buku dengan Postman
### 8. Tampilkan buku Dilan 1990 dengan Postman
### 9. Lakukan perubahan pada fungsi updateBook
### 10. Ubah judul buku Dilan 1991 menjadi "<NAMA PANGGILAN 1991>" dengan Postman
### 11. Lakukan perubahan pada fungsi deleteBook
### 12. Hapus buku Dilan 1990 dengan Postman
