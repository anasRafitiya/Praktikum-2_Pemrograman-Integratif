# BAB 3 Basic Routing dan Migration

## LANGKAH PERCOBAAN
## Percobaan instalasi NodeJS
### 1. GET
Untuk menambahkan endpoint dengan method GET pada aplikasi kita, kita dapat mengunjungi file web.php pada folder routes. Kemudian tambahkan baris ini pada akhir file
Gambar
Setelah itu coba jalankan aplikasi dengan command 
> php -S localhost:8000 -t public

> [!NOTE]
> Pastikan buka cmd pada folder aplikasi
Setelah aplikasi berhasil dijalankan, kita dapat membuka browser dengan url, <sub>http://localhost:8000/get</sub> , path yang akan kita akses akan berbentuk demikian, <sub>http://{BASE_URL}{PATH}</sub> , jika BASE_URL kita adalah <sub>localhost:8000</sub> dan PATH kita adalah <sub>/get</sub> , maka url akan berbentuk seperti diatas.
### 2. POST, PUT, PATCH, DELETE, dan OPTIONS 
Sama halnya saat menambahkan method GET, kita dapat menambahkan methode POST, PUT, PATCH, DELETE, dan OPTIONS pada file web.php dengan code seperti ini,
Gambar
Setelah selesai menambahkan route untuk method POST, PUT, PATCH, DELETE, dan OPTIONS, kita dapat menjalankan server seperti pada saat percobaan GET. Setelah server berhasil menyala, kita dapat membuka aplikasi Postman atau Insomnia atau kita juga dapat menggunakan PowerShell (Windows)/Terminal (Linux atau Mac) untuk melakukan request ke server. Namun, pada percobaan kali ini kita akan menggunakan extensions pada VSCode yaitu Thunder Client.
#### a.	Kita dapat menginstall ekstensi dengan membuka panel extensions lalu mencari thunder client
#### b.	Setelah menginstall Thunder Client, kita akan melihat logo seperti petir pada activity bar kita (sebelah kiri).
#### c.	Kita dapat membuat request dengan menekan “New Request” pada ekstensi
#### d.	Setelah itu kita dapat memasukkan method dan url yang dituju
#### e.	Akses url yang baru saja ditambahkan pada aplikasi dengan methodnya

### 3.	Migrasi Database
#### a.	Sebelum melakukan migrasi database pastikan server database aktif kemudian pastikan sudah membuat database dengan nama <sub>lumenapi</sub>
#### b.	Kemudian ubah konfigurasi database pada file .env menjadi seperti ini
#### c.	Setelah mengubah konfigurasi pada file .env, kita juga perlu menghidupkan beberapa library bawaan dari lumen dengan membuka file app.php pada folder bootstrap dan mengubah baris ini,
Gambar
Menjadi
Gambar
#### d.	Setelah itu jalankan command berikut untuk membuat file migration,
Gambar
Setelah menjalankan 2 syntax di atas akan terbuat 2 file pada folder <sub>database/migration</sub> dengan format YYY_MM_DD_HHmmss_nama_migrasi. Pada file migrasi kita akan menemukan fungsi up() dan fungsi down(), fungsi up() akan digunakan pada saat kita melakukan migrasi, fungsi down() akan digunakan saat kita ingin me-rollback migrasi
#### e.	Ubah fungsi up pada file migrasi create_users_table
Gambar
#### f.	Ubah fungsi up pada file migrasi <ub>create_products_table</sub>
#### g.	Kemudian jalankan command,
