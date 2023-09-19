# Praktikum-2_Pemrograman-Integratif
Jawaban dari tugas praktikum Pemrograman Integratif pada bab CRUD MongoDB Compass dan Shell

**Nama  : Anas Rafitiya**

**NIM   : 215150700111041**

## LANGKAH PERCOBAAN
### MongoDB Compass
#### 1. Lakukan koneksi ke MongoDB menggunakan connection string 
**Berikut apabila menggunakan tidak menggunakan atlas (secara local)**
![no 1](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/1d4b44fa-06f5-44ac-bbf8-9fbd66c34f2f)

#### 2. Buat database dengan melakukan klik “Create Database”
![no 2](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/31758010-9a4f-4d49-8c92-a6d25451c680)
> [!NOTE]
> MongoDB akan membuat nilai _id secara otomatis, tidak perlu mengikuti nilai _id yang terdapat pada modul

#### 3. Lakukan insert buku pertama dengan melakukan klik “Add Data”, pilih “Insert Document”, isi dengan data yang diinginkan dan klik “Insert”
![no 3](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/7499af48-e610-4ff4-8c2d-bb61f9059349)

#### 4. Lakukan insert buku kedua dengan cara yang sama
![no 4](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/cdcb164c-ded7-4bd1-970c-e8406cb0bcee)

#### 5. Lakukan pencarian buku dengan author “Osamu Dazai” dengan mengisi filter yang diinginkan dan klik “Find”
![no 5](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/a26b83f9-4e84-4f11-8919-a40d91658bfe)

#### 6. Lakukan perubahan summary pada buku “No Longer Human” menjadi “Buku yang bagus (<NAMA>,<NIM>) dengan melakukan klik “Edit Document” (berlambang pensil), mengisi nilai summary yang baru, dan melakukan klik “Update"
![no 6](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/e5e1ae2c-5303-4b5a-9e4b-a9795d6b11ae)

#### 7. Llakukan penghapusan pada buku “I Am a Cat” dengan melakukan klik “Remove Document” (berlambang tong sampah) dan melakukan klik “Delete”
![no 7](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/a849dc16-b139-466b-99d0-1fa66e4b9db3)

### MongoDB Shell
#### 1. Lakukan koneksi ke MongoDB Server dengan menjalankan command mongosh bagi yang menggunakan terminal build in OS sehingga tampilan terminal kalian akan menjadi seperti berikut.
![no 8](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/ef37c39e-aed2-42ac-8c11-dc7ac3909052)
> [!NOTE]
> Apabila kalian menggunakan MongoDB atlas, silahkan copy connection string dari MongoDB atlas kalian masing-masing dan paste kan di terminal kalian. Namun, di sini praktikan mengakses MongoDB Shell langsung dari aplikasi MongoDB Atlas dengan cara menekan tulisan **MONGOSH** yang terletak di bagian bawah layar setelah melakukan koneksi ke database yang diinginkan.

#### 2. Mencoba melihat isi list database yang ada di server dengan menjalankan command <sub>show dbs</sub>'#ff0000'
![no 9](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/ab02a699-9344-44a8-9484-019de74b6579)
![no 9 b](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/207a1c6f-8ed9-40f7-a1d1-8aa382fa0168)
![no 9 c](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/c8522563-c180-470e-9148-5ee55ab4cbe4)
![no 10(3)](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/2ced3518-1651-43b0-a993-4e2849261cbb)
![no 11(4)](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/a4211e93-33c6-4c5a-b4f1-4dbdb9828be4)
![no 12(5)](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/42160d8d-c5a6-4ef4-b2a9-821e935f3c92)
![no 13(6)](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/f68e4610-5ddd-4836-99d2-e7db07945e85)
![no 14(7)](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/a309e6cd-d602-43fd-bb9b-9a9807cf6e0f)
![no 15(8)](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/81cc2bef-1a00-4444-8f5d-a6db996bb5e6)
![no 15_2](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/c0d2153c-1ddc-44d6-885b-a55f7f1c7ea3)
![no16(9)](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/b7597649-e3ca-4105-be42-97b4a074e8de)
![no 17(10)](https://github.com/anasRafitiya/Praktikum-2_Pemrograman-Integratif/assets/125624764/f205a88f-5a6b-45dc-87aa-3e59f14db23c)
