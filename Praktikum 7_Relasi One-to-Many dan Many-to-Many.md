# BAB 6 RELASI ONE-TO-MANY DAN MANY-TO-MANY

## Langkah Percobaan
## Pembuatan Tabel
Berikut adalah table yang akan digunakan pada percobaan ini
> ![tabel 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/6354a6d6-c2a3-4184-a425-6803322b0c06)

### 1.	Sebelum membuat migrasi database atau membuat tabel pastikan server database aktif kemudian pastikan sudah membuat database dengan nama <sub>lumenpost</sub>
> ![no 1 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/ad51f3d3-485c-4cb3-94fb-fe96fb690d2b)

### 2.	Kemudian ubah konfigurasi database pada file .env menjadi seperti berikut
> ![no 1 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/29d9035e-6f70-4a78-a0af-50b4cb4135bd)

### 3.	Setelah mengubah konfigurasi pada file .env, kita juga perlu menghidupkan beberapa library bawaan dari lumen dengan membuka file app.php pada folder bootstrap dan mengubah baris ini
> ![no 1 3 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/272615d9-5c03-4fde-8e9c-b55a02b68d56)

menjadi
> ![no 1 3 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/7a6a7602-135b-4369-bed9-43ee3ba18e67)

### 4.	Setelah itu jalankan command berikut untuk membuat file migration
> ![no 1 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/bbaba3fa-6dd9-4ae2-9caf-dd40a4834328)

### 5.	Ubah fungsi <sub>up()</sub> pada file <sub>migrasi create_post_table</sub>
sebelumnya
> ![no 1 5 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/ceeaf0df-9458-4040-b369-f60ec362064b)

diubah menjadi
> ![no 1 5 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/203a2c4f-c283-40bb-9786-824778ba8335)

### 6.	Ubah fungsi <sub>up()</sub> pada file <sub>create_comments_table</sub>
sebelumnya
> ![no 1 6 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/7cc2e30e-f232-4d9d-9e7e-79091ade8232)

diubah menjadi
> ![no 1 6 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f76e0997-0a68-4261-a65d-d4575dc5162b)

### 7.	Ubah fungsi <sub>up()</sub> pada file <sub>create_tags_table</sub>
sebelumnya
> ![no 1 7 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/50e5d116-afcd-4132-b843-0a9dc11f2217)

diubah menjadi
> ![no 1 7 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/bde3b55f-c62e-4a96-870a-28a4d4624efc)

### 8.	Ubah fungsi <sub>up()</sub> pada file <sub>create_post_tag_table</sub>
sebelumnya
> ![no 1 8 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/611fcb9d-ba9d-4cf4-9b42-c9b21804ff64)

diubah menjadi
> ![no 1 8 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/292355e4-deb5-4090-92c7-b3d8fb028d41)

### 9.	Kemudian jalankan command
> ![no 1 9](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/54ded5ac-1a79-4c64-98d0-6e16b23c3010)

## Pembuatan Model
### 1.	Buatlah file dengan nama Post.php dan isi dengan baris kode berikut
> ![no 2 1 fix](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/abf10e22-a3c1-4639-9785-09f979b51582)

### 2.	Buatlah file dengan nama Comment.php dan isi dengan baris kode berikut
> ![no 2 2 fix](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/25da1c47-b8ae-4886-9171-dc7aa6d2eb1d)

### 3.	Buatlah file dengan nama Tag.php dan isi dengan baris kode berikut
> ![no 2 3 fix](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/028bd074-a294-40a7-a6f3-ef435fd2c10c)

## Relasi One-to-Many
### 1.	Tambahkan fungsi comments() pada file Post.php
> ![no 3 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/2a2fd63d-5b71-4b20-b335-d97630129049)

### 2.	Tambahkan fungsi post() dan atribut postId pada $fillable pada file Comment.php
> ![no 3 2 fix](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/99d4873e-280a-481c-880b-93cce357cf20)

### 3.	Buatlah file PostController.php dan isilah dengan baris kode berikut
> ![no 3 3 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/b06e60c9-cc3c-429d-8bb9-f33072774aaa)
> ![no 3 3 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/ce18f2e8-1435-469d-88a3-ac92415f46e5)

### 4.	Buatlah file CommentController.php dan isilah dengan baris kode berikut
> ![no 3 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f01214a6-ed03-4da6-b340-cff8f4a778b3)

### 5.	Tambahkan baris berikut pada routes/web.php
> ![no 3 5 fix](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/706546e6-21a8-4382-9ac5-94d90635795a)

### 6.	Buatlah satu post menggunakan Postman
> ![no 3 6](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/8a7a45a9-6a25-4e08-9392-e3bda9b2296d)

### 7.	Buatlah satu comment menggunakan Postman
> ![no 3 7](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/2f8138e5-bd42-4cb5-9d9e-63514df0c214)

### 8.	Tampilkan post menggunakan Postman
> ![no 3 8](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/d387e38b-bbf2-4283-b07d-772df765be06)

## Relasi Many-to-Many
### 1.	Tambahkan fungsi tags() pada file Post.php
> ![no 4 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/a2fb60c2-25d2-4f9b-81d5-ecd5da9ad590)

### 2.	Tambahkan funsi posts() pada file Tag.php
> ![no 4 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/45d4cfe9-ba66-486a-a34b-e26b66a52855)

### 3.	Buatlah file TagController.php dan isilah dengan baris kode berikut
> ![no 4 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/05526f58-d966-4e28-9197-61a73ce90dd7)

### 4.	Tambahkan fungsi addTag dan response tags pada PostController.php
> ![no 4 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/e3ad5aa3-2d42-4f00-aadf-c981e50df288)

### 5.	Tambahkan baris berikut pada routes/web.php
> ![no 4 5 new](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/0f7f7264-ef9e-437e-b7ce-93f2f7319609)

### 6.	Buatlah satu tag menggunakan Postman
> ![no 4 6](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/0f68cc9b-c364-45fa-a217-1c19c2c9149f)

### 7.	Tambahkan tag “jadul” pada post “disana engkau berdua”
> ![no 4 7 fix](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/7b20ddfb-cdb6-49e2-a9ab-405d1a074377)

### 8.	Tampilkan post “disana engkau berdua” menggunakan Postman
> ![no 4 8](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/cfd02e18-6831-41cf-8a34-32c22f428b51)

### 9.	Buatlah postingan “tanpamu apa artinya” menggunakan Postman
> ![no 4 9 fix](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/c944b157-cc08-4378-bdd4-9a3ad565955d)

### 10.	Tambahkan tag “jadul” pada postingan “tanpamu apa artinya”
> ![no 4 10 fix](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/a47a8c01-0558-4925-8a4f-be6328c4a340)

### 11.	Buatlah tag “lagu” menggunakan Postman
> ![no 4 11](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/11676e8c-2945-4e29-a5ff-80a32e0a6b96)

### 12.	Tambahkan tag “lagu” pada postingan “tanpamu apa artinya”
> ![no 4 12 fix](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/773f1bb6-80ff-405c-9116-ee1d101164ac)
 
### 13.	Tampilkan post pertama
> ![no 4 13](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/9beefd67-c2be-477f-8a8b-556bf2858588)

### 14.	Tampilkan post kedua
> ![no 4 14](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/ba601f14-ef04-41ad-951b-0f83a25cfee1)

> [!NOTE]
> Tag “jadul” yang berada pada dua post menunjukkan **satu** tag dapat berada di **banyak** post

> [!NOTE]
> Post “tanpamu apa artinya” yang memiliki dua tag menunjukkan **satu** post dapat memiliki banyak **tag**


