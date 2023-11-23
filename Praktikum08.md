Praktikum 8 : Register, Authentication dan Authorization



Nama : Muhammad Yusuf Habibie

NIM : 215150701111044

Tanggal : 24 Oktober 2023

Asisten : Iqbal Biondy


Register

1. Pastikan terdapat tabel users yang dibuat menggunakan migration pada bab 3 Basic Routing dan Migration.
![Alt text](SS08/image.png)

2. Pastikan terdapat model User.php yang digunakan pada bab 5 Model, Controller dan Request-Response Handler.
![Alt text](SS08/image-1.png)

3. Buatlah file AuthController.php dan isilah dengan baris kode berikut
![Alt text](SS08/image-2.png)

4. Tambahkan baris berikut pada routes/web.php
![Alt text](SS08/image-3.png)

5. Jalankan aplikasi pada endpoint /auth/register dengan body berikut
![Alt text](SS08/image-4.png)


Authentication

1. Buatlah fungsi login(Request $request) pada file AuthController.php
![Alt text](SS08/image-5.png)

2. Tambahkan baris berikut pada routes/web.php
![Alt text](SS08/image-6.png)

3. Jalankan aplikasi pada endpoint /auth/login dengan body berikut
![Alt text](SS08/image-7.png)


Token

1. Jalankan perintah berikut untuk membuat migrasi baru
![Alt text](SS08/image-8.png)

2. Tambahkan baris berikut pada migration yang baru terbuat
![Alt text](SS08/image-9.png)

3. Tambahkan atribut token di $fillable pada User.php
![Alt text](SS08/image-10.png)

4. Tambahkan baris berikut pada file AuthController.php
![Alt text](SS08/image-11.png)

5. Jalankan perintah di bawah untuk menjalankan migrasi terbaru
![Alt text](SS08/image-12.png)

6. Jalankan aplikasi pada endpoint /auth/login dengan body berikut. Salinlah token yang didapat ke notepad
![Alt text](SS08/image-13.png)


Authorization

1. Buatlah file Authorization.php pada folder App/Http/Middleware dan isilah dengan baris berikut
![Alt text](SS08/image-14.png)

2. Tambahkan middleware yang baru dibuat pada bootstrap/app.php.
![Alt text](SS08/image-15.png)

3. Buatlah fungsi home() pada HomeController.php
![Alt text](SS08/image-16.png)

4. Tambahkan baris berikut pada routes/web.php
![Alt text](SS08/image-17.png)

5. Jalankan aplikasi pada endpoint /home dengan melampirkan nilai token yang
didapat setelah login pada header
![Alt text](SS08/image-18.png)