# BAB 5 Model, Controller dan Request-Response Handler

## LANGKAH PERCOBAAN
## Model
### 1.	Pastikan terdapat table users yang dibuat menggunakan migration pada bab sebelumnya. Berikut informasi kolom yang harus ada.
> ![no 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/243e29f5-65c3-4752-848a-a4ce879910b2)

### 2. Bershihkan isi User.php yang ada sebelumnya dan isi dengan baris kode berikut
> ![no 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/88977f1f-904a-4cb4-954d-1a54b3276c45)

## Controller
### 1.	Buatlah Salinan ExampleController.php pada folder app/Http/Controllers dengan nama HomeController.php dan buatlah fungsi index() yang berisi
> ![no 2 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/c8a2797f-ef88-41b3-9606-068e35ae942f)

### 2.	Ubah route / pada file routes/web.php menjadi seperti ini
>![no 2 2 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f3cd09a2-8448-4328-bb87-13c750e204d3)
> ![no 2 2 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f2e6ab46-b7f6-47a6-ab92-c14a2ae492b3)

### 3.	Jalankan aplikasi
> ![no 2 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/7a70f451-5b7d-4d5a-8c08-3249597aa2ef)

## Request Handler
### 1.	Lakukan import library Request dengan menambahkan baris berikut di bagian atas file
> ![no 3 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/5f10f34e-3717-4ce8-9cb1-d270b058ce6b)

### 2.	Ubah fungsi index menjadi
> ![no 3 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/231bad79-7b9f-46ff-a8ce-3e1618c3ace7)

### 3.	Jalankan aplikasi
> ![no 3 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/42f787d6-08a2-4b7a-af2d-f763c6209c9f)

## Response Handler
### 1.	Lakukan import library Response dengan menambahkan baris berikut di bagian atas file
> ![no 4 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/53a49059-494a-47ba-8e1c-1f05e98a0e77)

### 2.	Buatlah fungsi hello() yang berisi
> ![no 4 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/255dd6c9-d686-4faa-9c00-db1a14543ff4)

### 3.	Tambahkan route /hello pada file routes/web.php
> ![no 4 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/5c841023-464b-4f73-b715-40570ce746b6)

### 4.	Jalankan aplikasi pada route /hello
> ![no 4 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/98dcfd71-cc42-4cc2-9e5c-6490ea25d7f9)

## Penerapan
### 1.	Lakukan import model User dengan menambahkan baris berikut di bagian atas file
> ![no 5 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/b99fb93a-bd2a-460b-b672-a5413b524e97)

### 2.	Tambahkan ketiga fungsi berikut di HomeController.php
>![no 5 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/7fc41573-292a-4bdb-abf0-a178d097a0b7)
> ![no 5 2 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f0f61add-eb69-48f6-bc5c-9c6811e3c511)

### 3.	Tambahkan ketiga route pada file routes/web.php menggunakan group route
> ![no 5 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/03b0c8a1-caf3-4a3a-bcf6-45eb471d80d9)

### 4.	Jalankan aplikasi pada route /users/default menggunakan Postman
> ![no 5 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/dc66c1c1-5f2a-43bd-b813-1d48f4a88415)

### 5.	Jalankan aplikasi pada route /users/new dengan mengisi body sebagai berikut
> ![no 5 5](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/fd2e41cc-241d-40f3-8b34-8d13be5a322b)

### 6.	Jalankan aplikasi pada route /users/all
> ![no 5 6](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/90e86e0d-34cb-47a6-b05f-d08c77abff7c)


