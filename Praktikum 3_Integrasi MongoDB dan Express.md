# BAB 2 Integrasi MongoDB dan Express

## LANGKAH PERCOBAAN
## Percobaan instalasi NodeJS
### 1. Buka halaman
> ![no1 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/cf52d582-40aa-4a81-9f2c-7df5a5f295ac)

### 2. Download dan jalankan node setup
> ![no 1 2y](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/3d7be202-e618-48a9-b5a5-4aa85222fffe)

### 3. Setelah instalasi selesai jalankan command <sub>node -v</sub> untuk memeriksa apakah NodeJS sudah terinstall
> ![no 1 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f2453381-1cc7-4782-b0db-9f17ddc310b3)

## Inisiasi project Express dan pemasangan package
### 1. Lakukan pembuatan folder dengan nama express-mongodb dan masuk ke dalam folder tersebut lalu buka melalui text editor masing-masing
> ![no 2 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/978c9ea4-e0b1-41e6-86f0-d29f3428ac52)

### 2. Lakukan npm init untuk mengenerate file package .json dengan menggunakan command <sub>npm init -y</sub>
> ![no 2 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/2ca38764-2733-44f6-856d-3f75469d8299)

### 3. Lakukan instalasi express, mongoose, dan dotenv dengan menggunakan command <sub>npm i express mongoose dotenv</sub>
> ![no 2 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/904a197f-5d5e-4386-990f-8c660dc2f96d)

## Koneksi Express ke MongoDB
### 1. Buatlah file **index.js** pada root folder dan masukkan kode di bawah ini
> ![no 3 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/dc765e1e-80f3-41a5-b921-cf9d803529be)
Setelah itu coba jalankan aplikasi dengan command <sub>node index.js</sub>
> ![no 3 1b](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/b2110acb-43e1-4b8a-91a5-f90825929164)

> [!WARNING]
> Dikarenakan tidak menggunakan nodemon, maka setiap kali menyimpan perubahan file diharuskan untuk restart server node terlebih dahulu dengan menekan ctrl+c dan jalankan command <sub>node index.js</sub> lagi
### 2. Lakukan pembuatan file .env dan masukkan baris berikut
> PORT=5000
> 
> ![no 3 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/63849454-d7ac-4282-a89b-ab311064994e)

Setelah itu ubahlah kode pada listening port menjadi berikut dan coba jalankan aplikasi kembali
> ![no 3 2b](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/810bdfc6-0778-4dfd-a113-b57148de80b5)
> ![no 3 2c](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f3b57782-a300-4ac0-a3b6-3efd6d96badf)
> hasil setelah menjalankan aplikasi

### 3. Copy connection string yang terdapat pada compass atau atlas dan paste kan pada **.env** seperti berikut
> ![no 3 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/8275fd72-a578-4732-9aaf-1a32a1734b9c)

### 4. Tambahkan baris kode berikut pada file **index.js**
> ![no 3 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/2a552a67-8631-40b2-aadb-23f43a717425)

Setelah itu coba jalankan aplikasi kembali
> ![no 3 4b](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/c86bf347-2f33-4c6f-850b-bfb3c80957e7)

## Pembuatan routing
### 1. Lakukan pembuatan direktori routes di tingkat yang sama dengan index.js
> ![no 4 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/0cab4c30-3999-436f-96e9-bd92a2c1cc48)

### 2. Buatlah file book.route.js di dalamnya
> ![no 4 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/9bf7e038-e887-4119-a39b-6591bd07caec)

### 3. Tambahkan baris kode berikut untuk fungsi getAllBooks
> ![no 4 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/d13b8bbb-c895-4d8e-af09-eb82730f526c)

### 4. Lakukan hal yang sama untuk getOneBook createBook, updateBook, dan deleteBook
> ![no 4 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/b9de88ba-feb6-4abb-a9f5-3d7f10ac85c7)

### 5. Lakukan import book.route.js pada file index.js dan tambahkan baris kode berikut
> ![no 4 5](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/8c29996e-c6a5-48ab-a222-7d237924bf1f)

### 6. Uji salah satu endpoint dengan Postman
> ![no 4 6](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/aeeb1d92-8659-4589-9814-547db1a7e965)

## Pembuatan controller
### 1. Lakukan pembuatan direktori controllers di tingkat yang sama dengan index.js
> ![no 5 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/6bdc3af0-9feb-4701-b06d-81d71cd0a3f9)

### 2. Buatlah file book.controller.js di dalamnya
> ![no 5 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/8bbda141-6c96-418c-8cc4-a65f21ddcc08)

### 3. Salin baris kode dari routes untuk fungsi getAllBooks
> ![no 5 3real](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/dd4d9130-9cee-426e-ab81-1a3473be6f1d)

### 4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, deleteBooks
> ![no 5 4 real](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/2d773405-bfa2-400f-b195-f18d7d9160a0)

### 5. Lakukan import book.controller.js pada file book.route.js
> ![no 5 5](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/c03529ee-306f-4a88-a4a4-3c34fc8cb926)

### 6. Lakukan perubahan pada fungsi agar dapat memanggil fungsi dari book.controller.js
> ![no 5 6 real](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/48ad9f9b-b41f-4cb7-a2b7-7ed7cb69c9e4)

### 7. Lakukan pengujian kembali, pastikan response tetap sama
> ![no 5 7](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/c9ece5ac-2435-4c3e-8814-74484c779b60)

## Pembuatan model
Berikut adalah gambaran bentuk dari data dari modul sebelumnya
![model](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/5d156c50-a93a-4b8f-bdd9-0dd881eec80f)

### 1. Lakukan pembuatan direktori models di tingkat yang sama dengan index.js
> ![no 6 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/a6712d39-5583-41fd-a23a-df897bade7f8)

### 2. Buatlah file book.model.js di dalamnya
> ![no 6 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/004e733e-ecb3-4dcc-9138-8603e554543a)

### 3. Tambahkan baris kode berikut sesuai dengan tabel di atas
> ![no 6 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/e623f998-5584-43e2-9a96-a6cd63ee3ab8)

## Operasi CRUD
### 1. Hapus semua data pada collection books
> ![no 7 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/1c34c813-b502-467d-b134-fcbdbeb4b9d2)

### 2. Lakukan import book.model.js pada file book.controller.js
> ![no 7 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f66d4363-076e-448f-9a81-8a47d0c693f2)

### 3. Lakukan perubahan pada fungsi createBook
> ![no 7 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/797e2649-1d70-4d36-b003-4a7ef4645c62)

### 4. Buatlah dua buah buku dengan data di bawah ini dengan Postman
> ![no 7 4a](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/906656e4-fe20-4e0d-891a-f9e0909b0747)
> ![no 7 4b](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/b23cdcb6-296e-4cb6-8605-35193df86d50)

### 5. Lakukan perubahan pada fungsi getAllBooks
> ![no 7 5](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/60231ec3-d385-4e28-ac9c-b3ccd616fcd6)

### 6. Lakukan perubahan pada funsi getOneBook
> ![no 7 6](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/1151db19-b935-495c-b857-be25e2c7b3c3)

### 7. Tampilkan semua buku dengan Postman
> ![no 7 7](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/ce42cab4-4465-4d65-89ec-0b06092ec78c)

### 8. Tampilkan buku Dilan 1990 dengan Postman
> ![no 7 8](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/e18c51b7-9c11-4b0a-9707-caa83113d485)

### 9. Lakukan perubahan pada fungsi updateBook
> ![no 7 9](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/6a102175-981b-4f9a-8369-34e091ec6881)

### 10. Ubah judul buku Dilan 1991 menjadi "<NAMA PANGGILAN 1991>" dengan Postman
> ![no 7 10](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/4d25b897-3a76-4058-b693-5f38c2f29525)

### 11. Lakukan perubahan pada fungsi deleteBook
> ![no 7 11](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/564a5170-4516-4f97-9bc0-632f0cbfe231)

### 12. Hapus buku Dilan 1990 dengan Postman
> ![no 7 12](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/2041f9e2-3f33-45d6-b9b0-170145ddaafd)
