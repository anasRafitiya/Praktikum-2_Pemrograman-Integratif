# BAB 4 Dynamic Route dan Middleware

## LANGKAH PERCOBAAN
### 1.	Dynamic Route
Dynamic route adalah route yang dapat berubah-ubah, contohnya pada saat kita membuka suatu halaman web, kadang kita melihat <sub>/users/1</sub> atau <sub>/users/2</sub>, hal ini yang dinamakan dynamic routes.
Untuk menambahkan dynamic routes pada aplikasi lumen kita, kita dapat menggunakan syntax berikut,
> ![no 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/891e945c-fb9d-4615-866f-412b5cdb3db6)

Saat menambahkan parameter pada routes, kita tidak terbatas pada 1 variable saja, namun kita dapat menambahkan sebanyak yang diperlukan seperti kode berikut,
> ![no 1 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/ee5c902e-3350-4756-9e9d-15316d0f5d04)

Pada dynamic routes kita juga bisa menambahkan optional routes, yang mana optional routes tidak mengharuskan kita untuk memberi variabel pada endpoint kita, namun saat kita memanggil endpoint, dapat menggunakan parameter variable ataupun tidak, seperti pada kode di bawah ini,
> ![no 1 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/34d4d8f4-34cd-473b-a178-0072157189ef)

### 2.	Aliases Route
Aliases Route digunakan untuk memberi nama pada route yang telah kita buat, hal ini dapat membantu kita, saat kita ingin memanggil route tersebut pada aplikasi kita. Berikut syntax untuk menambahkan aliases route
> ![no 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/273eed8d-df49-4435-b45d-12c5541e0a52)

### 3.	Group Route
Pada lumen, kita juga dapat memberikan grouping pada routes kita agar lebih mudah pada saat penulisan route pada web.php kita. Kita dapat melakukan grouping dengan menggunakan syntax berikut,
> ![no 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/cd59f0b1-1b1d-4714-9a4f-eb93c9c54809)

Selain dapat mengelompokkan prefix, kita juga dapat mengelompokkan middleware dan namespace pada kelompok routes kita

### 4.	Middleware
Middleware adalah penengah antara komunikasi aplikasi dan client. Middleware biasanya digunakan untuk membatasi siapa yang dapat berinteraksi dengan aplikasi kita dan semacamnya, kita dapat menambahkan middleware dengan menambahkan file pada folder <sub>app/Http/Middleware</sub>. Pada folder tersebut terdapat file <sub>ExampleMiddleware</sub>, kita dapat men-copy file tersebut untuk membuat middleware baru.
Pada praktikum kali ini akan dibuat middeware Age dengan isi,
> ![no 4 1](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/a8268129-d75f-4bf3-a7eb-18d735a7ff7b)

Kemudian, setelah menambahkan filter pada <sub>AgeMiddleware</sub>, kita harus mendaftarkan <sub>AgeMiddleware</sub> pada aplikasi kita, pada file <sub>bootstrap/app.php</sub> seperti berikut ini,
> ![no 4 2](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/fa2fd74d-0269-41a5-a397-be8fe2f1acae)

Pada baris 65 terdapat comment mengenai proses mendaftarkan suatu middleware dalam aplikasi kita. Untuk menambahkan middleware pada aplikasi kita, kita dapat men-uncomment baris 75 hingga 77, kemudian menambahkan age middleware ke dalamnya. Namun, karena kita hanya ingin menambahkan middleware pada route tertentu kita akan menghapus comment pada baris 79 hingga 81, kemudian menambahkan middleware age di dalamnya.
Lalu, kita dapat menambahkan middleware pada routes kita dengan menambahkan opsi middleware pada salah satu route, contohnya,
> ![no 4 3](https://github.com/anasRafitiya/Praktikum-Pemrograman-Integratif/assets/125624764/c45f73bc-7def-4a14-bed6-ae2a8c544e2c)


