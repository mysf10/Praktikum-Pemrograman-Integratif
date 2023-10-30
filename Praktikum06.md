Praktikum 6 : Model Controller & Request Response



Nama : Muhammad Yusuf Habibie

NIM : 215150701111044

Tanggal : 10 Oktober 2023

Asisten : Iqbal Biondy


Model

1. Pastikan terdapat tabel users yang dibuat menggunakan migration pada bab
sebelumnya.
![Alt text](image.png)

2. Bersihkan isi User.php yang ada sebelumnya dan isi dengan baris kode berikut
![Alt text](image-1.png)


Controller

1. Buatlah salinan ExampleController.php pada folder app/Http/Controllers dengan
nama HomeController.php dan buatlah fungsi index()
![Alt text](image-2.png)

2. Ubah route / pada file routes/web.php menjadi seperti ini
![Alt text](image-4.png)

3. Jalankan aplikasi
![Alt text](image-3.png)

Request Handler

1. Lakukan import library Request dengan menambahkan baris berikut di bagian atas
file
![Alt text](image-5.png)

2. Ubah fungsi index menjadi
![Alt text](image-6.png)

3. Jalankan aplikasi
![Alt text](image-7.png)


Response Handler

1. Lakukan import library Response dengan menambahkan baris berikut di bagian
atas file
![Alt text](image-8.png)

2. Buatlah fungsi hello() yang berisi
![Alt text](image-9.png)

3. Tambahkan route /hello pada file routes/web.php
![Alt text](image-10.png)

4. Jalankan aplikasi pada route /hello
![Alt text](image-11.png)


Penerapan

1. Lakukan import model User dengan menambahkan baris berikut di bagian atas file
![Alt text](image-12.png)

2. Tambahkan ketiga fungsi berikut di HomeController.php
![Alt text](image-13.png)

3. Tambahkan ketiga route pada file routes/web.php menggunakan group route
![Alt text](image-14.png)

4. Jalankan aplikasi pada route /users/default menggunakan Postman
![Alt text](image-15.png)

5. Jalankan aplikasi pada route /users/new dengan mengisi body
![Alt text](image-16.png)

6. Jalankan aplikasi pada route /users/all
![Alt text](image-17.png)