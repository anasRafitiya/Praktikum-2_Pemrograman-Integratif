# BAB 3 Basic Routing dan Migration

## LANGKAH PERCOBAAN
### 1. GET
Untuk menambahkan endpoint dengan method GET pada aplikasi kita, kita dapat mengunjungi file web.php pada folder routes. Kemudian tambahkan baris ini pada akhir file
> ![no 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/ffbaf946-112a-45ec-8a4b-db8b964e72da)

Setelah itu coba jalankan aplikasi dengan command 
> php -S localhost:8000 -t public

> ![no 1 b](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/41110745-94ce-4ea5-9830-df6fdeae7589)

> [!NOTE]
> Pastikan buka cmd pada folder aplikasi

Setelah aplikasi berhasil dijalankan, kita dapat membuka browser dengan url, <sub>http://localhost:8000/get</sub> , path yang akan kita akses akan berbentuk demikian, <sub>http://{BASE_URL}{PATH}</sub> , jika BASE_URL kita adalah <sub>localhost:8000</sub> dan PATH kita adalah <sub>/get</sub> , maka url akan berbentuk seperti diatas.
> ![no 1 c](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f2fa2340-c764-47c8-9d98-29d99e3fb2d5)

> Tampilan setelah mengakses http://localhost:8000/get

### 2. POST, PUT, PATCH, DELETE, dan OPTIONS 
Sama halnya saat menambahkan method GET, kita dapat menambahkan methode POST, PUT, PATCH, DELETE, dan OPTIONS pada file web.php dengan code seperti ini,
> ![no 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/8db82c27-22ff-4698-81b8-344e2e4c6c15)

Setelah selesai menambahkan route untuk method POST, PUT, PATCH, DELETE, dan OPTIONS, kita dapat menjalankan server seperti pada saat percobaan GET. Setelah server berhasil menyala, kita dapat membuka aplikasi Postman atau Insomnia atau kita juga dapat menggunakan PowerShell (Windows)/Terminal (Linux atau Mac) untuk melakukan request ke server. Namun, pada percobaan kali ini kita akan menggunakan extensions pada VSCode yaitu Thunder Client.
#### a.	Kita dapat menginstall ekstensi dengan membuka panel extensions lalu mencari thunder client
> ![no 2 a](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/9fb26967-c0b0-41a5-9181-0ca44b9a8a66)

#### b.	Setelah menginstall Thunder Client, kita akan melihat logo seperti petir pada activity bar kita (sebelah kiri).
> ![no 2 breal](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/fae61c85-d628-470e-92f2-b45d6446cd80)

#### c.	Kita dapat membuat request dengan menekan “New Request” pada ekstensi
> ![no 2 c](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/cc830252-4a68-4f6b-8e01-55a259da25a5)

#### d.	Setelah itu kita dapat memasukkan method dan url yang dituju
> ![no 2 d real](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/53cb9768-909a-45bf-9091-f704a56dc9b9)

#### e.	Akses url yang baru saja ditambahkan pada aplikasi dengan methodnya
> ![no 2 e](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/a3aee757-2249-480c-97fa-88b9c3d829b8)

### 3.	Migrasi Database
#### a.	Sebelum melakukan migrasi database pastikan server database aktif kemudian pastikan sudah membuat database dengan nama <sub>lumenapi</sub>
> ![no 3 a](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/da795ff2-d712-4a57-8927-fc0fcfac726e)
> Tampilan server database aktif

> ![database lumen api](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/b854548f-2f9f-42b9-8d42-59cc0cb08956)
> Membuat database <sub>lumenapi</sub>

#### b.	Kemudian ubah konfigurasi database pada file .env menjadi seperti ini
> ![no 3 b real](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/9ada509d-f22a-41df-9ba2-c41c1b5f2c48)

#### c.	Setelah mengubah konfigurasi pada file .env, kita juga perlu menghidupkan beberapa library bawaan dari lumen dengan membuka file app.php pada folder bootstrap dan mengubah baris ini,
> ![no 3 c1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/f51c0e4c-7f24-4da3-82e5-2f7e8fc59534)

Menjadi
> ![no 3 c2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/596df9fa-44b4-43f0-8bcf-74cb64c2b347)

#### d.	Setelah itu jalankan command berikut untuk membuat file migration,
> ![no 3 d1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/5dc9c73d-1666-4383-9de5-d317231777a4)
> ![no 3 d2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/2643c2bc-a981-4bb3-abce-57c4477beb48)

Setelah menjalankan 2 syntax di atas akan terbuat 2 file pada folder <sub>database/migration</sub> dengan format YYY_MM_DD_HHmmss_nama_migrasi. Pada file migrasi kita akan menemukan fungsi up() dan fungsi down(), fungsi up() akan digunakan pada saat kita melakukan migrasi, fungsi down() akan digunakan saat kita ingin me-rollback migrasi

#### e.	Ubah fungsi up pada file migrasi create_users_table
Sebelumnya
> ![no 3 e1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/6313e37c-1d65-43cb-ac6d-165f6d463f2e)

Diubah menjadi
> ![no 3 e2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/e6dec90d-6be9-4a96-beae-b38635414fd9)

#### f.	Ubah fungsi up pada file migrasi <ub>create_products_table</sub>
Sebelumnya
> ![no 3 f1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/3197bd81-4ee2-4aa6-9023-ebe39d03692c)

Diubah menjadi
> ![no 3 f2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/0eb90b38-c65f-41fb-bf35-0eccca7f4c41)

#### g.	Kemudian jalankan command,
> ![no 3 greal](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/27458442-359c-445d-a0df-f2094924f68d)

