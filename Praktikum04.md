Praktikum 4 : Basic Routing & Migration



Nama : Muhammad Yusuf Habibie

NIM : 215150701111044

Tanggal : 26 September 2023

Asisten : Iqbal Biondy


Langkah Percobaan

1. GET : menambahkan endpoint dengan method GET pada aplikasi kita.
![Alt text](SS04/image.png)

2. POST, PUT, PATCH, DELETE, dan OPTIONS : menambahkan methode POST, PUT, PATCH, DELETE, dan OPTIONS pada file web.php

a. Kita dapat menginstall ekstensi dengan membuka panel extensions lalu mencari thunder client
![Alt text](SS04/image-1.png)

b. Setelah menginstall Thunder Client, kita akan melihat logo seperti petir pada activity bar kita (sebelah kiri).
![Alt text](SS04/image-2.png)

c. Kita dapat membuat request dengan menekan "New Request" pada ekstensi
![Alt text](SS04/image-3.png)

d. Setelah itu kita dapat memasukkan method dan url yang dituju
![Alt text](SS04/image-4.png)

3. Migrasi Database

a. Sebelum melakukan migrasi database pastikan server database aktif kemudian
pastikan sudah membuat database dengan nama lumenapi

b. Kemudian ubah konfigurasi database pada file .env
![Alt text](SS04/image-6.png)

c. Setelah mengubah konfigurasi pada file .env, kita juga perlu menghidupkan
beberapa library bawaan dari lumen dengan membuka file app.php pada folder
bootstrap
![Alt text](SS04/image-7.png)

d. Setelah itu jalankan command untuk membuat file migration,
![Alt text](SS04/image-8.png)

e. Ubah fungsi up pada file migrasi create_users_table
![Alt text](SS04/image-9.png)

f. Ubah fungsi up pada file migrasi create_products_table
![Alt text](SS04/image-10.png)

g. php artisan migrate
![Alt text](SS04/image-11.png)