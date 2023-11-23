Praktikum 9 : JSON Web Token



Nama : Muhammad Yusuf Habibie

NIM : 215150701111044

Tanggal : 31 Oktober 2023

Asisten : Iqbal Biondy


Penyesuaian Database

1. Lakukan perubahan pada length kolom token dengan menghapus parameter 72 di belakangnya
![Alt text](SS09/image.png)

2. Jalankan perintah di bawah untuk memperbaharui migrasi dan menghapus data yang lama
![Alt text](SS09/image-1.png)

3. Jalankan aplikasi pada endpoint /auth/register dengan body berikut.
![Alt text](SS09/image-2.png)


JWT Manual

1. Tambahkan ketiga fungsi berikut pada AuthController.php
![Alt text](SS09/image-3.png)

2. Lakukan perubahan pada fungsi login
![Alt text](SS09/image-4.png)

3. Tambahkan keempat fungsi berikut pada Middleware/Authorization.php
![Alt text](SS09/image-5.png)

4. Lakukan perubahan pada fungsi handle
![Alt text](SS09/image-6.png)

5. Jalankan aplikasi pada endpoint /auth/login dengan body berikut. Salinlah token yang didapat ke notepad
![Alt text](SS09/image-7.png)

6. Jalankan aplikasi pada endpoint /home dengan melampirkan nilai token yang didapat setelah login pada header
![Alt text](SS09/image-8.png)


JWT Library

1. Lakukan generate jwt key secara online menggunakan website Djecrety ― Django Secret Key Generator
![Alt text](SS09/image-9.png)

2. Lakukan instalasi package jwt firebase dengan menggunakan command berikut
![Alt text](SS09/image-10.png)

3. Tambahkan fungsi berikut pada file AuthController
![Alt text](SS09/image-11.png)

4. Lakukan perubahan pada fungsi login menjadi seperti berikut
![Alt text](SS09/image-12.png)

5. Buatlah file JwtMiddleware.php dan isikan baris code berikut
![Alt text](SS09/image-13.png)

6. Daftarkan middleware yang telah dibuat pada bootstrap/app.php
![Alt text](SS09/image-14.png)

7. Tambahkan baris berikut pada file web.php
![Alt text](SS09/image-15.png)

8. Jalankan aplikasi pada endpoint /auth/login dengan body berikut. Salinlah token yang didapat ke notepad
![Alt text](SS09/image-16.png)

9. Jalankan aplikasi pada endpoint /home dengan melampirkan nilai token yang didapat setelah login pada header
![Alt text](SS09/image-17.png)