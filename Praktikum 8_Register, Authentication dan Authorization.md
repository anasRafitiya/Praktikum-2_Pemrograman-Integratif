# BAB 7 REGISTER, AUTHENTICATION DAN AUTHORIZATION

## Langkah Percobaan
## Register 
### 1.	Pastikan terdapat tabel users yang dibuat menggunakan migration pada bab 3 Basic Routing dan Migration. Berikut informasi kolom yang harus ada
> ![tabel model](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/01704c0c-9236-4c4a-b591-38904410d0e7)

> berikut bukti table users telah dibuat
> ![no 1 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/8b10021f-dcee-4d8a-af35-1e7fac8cab58)

### 2.	Pastikan terdapat model User.php yang digunakan pada bab 5 Model, Controllre dan Request-Response Handler. Berikut baris kode yang harus ada
> ![no 1 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/06c876f3-765e-438c-b252-5ec3d2f9ef04)

### 3.	Buatlah file AuthController.php dan isilah dengan baris kode berikut
> ![no 1 3 fix](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/10dd9717-1444-4540-bb7b-9d66e02f7591)

### 4.	Tambahkan baris berikut pada routes/web.php
> ![no 1 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/93975886-553d-4353-817b-130fb124d508)

### 5.	Jalankan aplikasi pada endpoint /auth/register dengan body berikut 
> ![no 1 5](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/a0f19266-58ca-4781-b5e7-e69c1480ff1d)

## Authentication
### 1.	Buatlah fungsi login(Request $request) pada file AuthController.php
> ![no 2 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/1e1f005d-d1fb-45fe-80b3-0c9e58627e82)

### 2.	Tambahkan baris berikut pada routes/web.php
> ![no 2 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/a688b049-f132-4056-a9c0-741f96a94bf3)

### 3.	Jalankan aplikasi pada endpoint /auth/login dengan body berikut
> ![no 2 3 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f8bd8eac-b323-44f8-bb49-28d05d2a8fb9)

> [!Note]
> Opsional : lakukan percobaan dengan menyalahkan email atau password dan amati responnya.

> hasil menyalahkan password
> ![no 2 3 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/5ced787e-f15a-4b0a-84db-fab8bd566627)

> hasil menyalahkan email
> ![no 2 3 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/b574eb64-f068-4d12-b1d7-4955d276fe8b)

## Token
### 1.	Jalankan perintah berikut untuk membuat migrasi baru
> ![no 3 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/1ec4dbe5-a0a2-4ac1-8ee0-9339ed5ac8df)

### 2.	Tambahkan baris berikut pada migration yang baru terbuat
> ![no 3 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/805151f8-2f50-487c-bd47-806bf03fb534)

### 3.	Tambahkan atribut token di $fillable pada User.php
> ![no 3 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/a07557dc-14d8-423c-8758-35dd67c87639)

### 4.	Tambahkan baris berikut pada file AuthController.php
> ![no 3 4 awal](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/d2af8547-62e0-4539-be7e-e0ddae3b83b4)
> ![no 3 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/e364e946-f541-4bcf-a1a4-d46b831a3ec6)

### 5.	Jalankan perintah di bawah untuk menjalankan migrasi terbaru
> ![no 3 5](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/2486b2ba-ccf6-44a7-b4c9-8152c85e6439)

### 6.	Jalankan aplikasi pada endpoint /auth/login dengan body berikut. Salinlah token yang didapat ke notepad
> ![no 3 6](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/76bc610f-04d0-4b6d-91b7-3bcf4fcbf708)


## Authorization 
### 1.	Buatlah file Authorization.php pada folder App/Http/Middleware dan isilah dengan baris berikut
> ![no 4 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/05128186-3855-4db3-b807-38da57f3b26a)

### 2.	Tambahkan middleware yang baru dibuat pada bootstrap/app.php.
> ![no 4 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/e3182317-de81-4819-9dcc-24c1b4bded19)

### 3.	Buatlah fungsi home() pada HomeController.php
> ![no 4 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/49869a48-42e9-4c81-ac00-2f1ab8d62ccb)

### 4.	Tambahkan baris berikut pada routes/web.php
> ![no 4 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/a31f4341-6791-47dd-8996-82dc7f4a5e8a)

### 5.	Jalankan aplikasi pada endpoint /home dengan melampirkan nilai token yang didapat setelah login pada header
> ![no 4 5](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/58e620e8-6be0-46a3-ae8f-4dd2bcc8bae8)
