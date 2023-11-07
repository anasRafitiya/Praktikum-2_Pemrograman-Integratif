# BAB 8 JSON WEB TOKEN (JWT)

## Langkah Percobaan
### Penyesuaian Database
#### 1. Lakukan perubahan pada length kolom token dengan menghapus parameter 72 di belakangnya
> ![no 1 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/30cf79a2-9d95-42a2-95d5-0354ba5256c8)

#### 2. Jalankan perintah di bawah untuk memperbaharui migrasi dan menghapus data yang lama
> ![no 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/1f4f1e14-d200-4bbb-adfa-3f500c6c03d5)

#### 3. Jalankan aplikasi pada endpoint /auth/register dengan body berikut.
> ![no 1 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/56fca527-ef16-4332-914c-a017c6b885eb)

### JWT Manual
#### 1. Tambahkan ketiga fungsi berikut pada AuthController.php
> ![no 2 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/6789b037-798b-43de-9a4d-ffb3fde5ae85)

#### 2. Lakukan perubahan pada fungsi login
> ![no 2 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/05f8a44e-ca97-4bc9-9e12-8996b0fd67d1)

#### 3. Tambahkan keempat fungsi berikut pada Middleware/Authorization.php
> ![no 2 3 real](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/3ab9d482-c006-4e55-8ffe-d2cbb78146f4)

#### 4. Lakukan perubahan pada fungsi handle
> ![no 2 4 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/46694605-35d1-48e2-8651-e490a439a4eb)
![no 2 4 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/07838742-4180-429d-ac2f-96bd1c8eb661)

#### 5. Jalankan aplikasi pada endpoint /auth/login dengan body berikut. Salinlah token yang didapat ke notepad.
> ![no 2 5](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/30efa394-0f33-496a-8b1c-5f6ad90107fd)

#### 6. Jalankan aplikasi pada endpoint /home dengan melampirkan nilai token yang didapat setelah login pada header
> ![no 2 6](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/e3c1ae5a-60a4-4d1b-a7c0-7ad2b82a42a8)

### JWT Library
#### 1. Lakukan generate jwt key secara online menggunakan website [Djecrety ― Django Secret Key Generator](https://djecrety.ir/).
> ![no 3 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/352a1613-bcb3-46e6-bce0-9fe633ad8f24)

> Setelah mendapatkan secret key kita akan memasukkan secret key tersebut pada file <sub>.env</sub> dengan membuat variable baru bernama <sub>JWT_SECRET</sub>.
> ![no 3 1 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/62146945-52fb-41cb-9eeb-2ac0f1dcf72c)

#### 2. Lakukan instalasi package jwt firebase dengan menggunakan command berikut
> ![no 3 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/49120809-e826-4495-8a81-3a41d6a169da)

#### 3. Tambahkan fungsi berikut pada file AuthController
> ![no 3 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/31a6fe8d-c182-4759-805e-f1102ee51393)

#### 4. Lakukan perubahan pada fungsi login menjadi seperti berikut
> ![no 3 4](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/39c99273-d7fe-42f9-83cd-3e1c82ec4add)

#### 5. Buatlah file JwtMiddleware.php dan isikan baris code berikut
> ![no 3 5](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/c9fe314f-e707-4f83-81d4-7a365ff9f17a)

#### 6. Daftarkan middleware yang telah dibuat pada <sub>bootstrap/app.php</sub>
> ![no 3 6](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/db0cd568-cafa-485a-9b57-c730e2d167ef)

#### 7. Tambahkan baris berikut pada file web.php
> ![no 3 7](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/8f8a54d0-f454-4a88-9f85-2f8ac2f38f18)

#### 8. Jalankan aplikasi pada endpoint /auth/login dengan body berikut. Salinlah token yang didapat ke notepad
>

#### 9. Jalankan aplikasi pada endpoint /home dengan melampirkan nilai token yang didapat setelah login pada header
>

