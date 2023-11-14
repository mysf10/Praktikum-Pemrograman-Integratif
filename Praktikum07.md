Praktikum 7 : Relasi 1-N & M-N



Nama : Muhammad Yusuf Habibie

NIM : 215150701111044

Tanggal : 17 Oktober 2023

Asisten : Iqbal Biondy


Pembuatan Tabel

1. Sebelum membuat migrasi database atau membuat tabel pastikan server database
aktif kemudian pastikan sudah membuat database dengan nama lumenpost
![Alt text](SS07/image.png)

2. Kemudian ubah konfigurasi database pada file .env
![Alt text](SS07/image-1.png)

3. Setelah mengubah konfigurasi pada file .env, kita juga perlu menghidupkan
beberapa library bawaan dari lumen dengan membuka file app.php pada folder
bootstrap dan mengubah baris
![Alt text](SS07/image-2.png)

4. Setelah itu jalankan command berikut untuk membuat file migration
![Alt text](SS07/image-3.png)

5. Ubah fungsi up() pada file migrasi create_posts_table
![Alt text](SS07/image-4.png)

6. Ubah fungsi up() pada file create_comments_table
![Alt text](SS07/image-5.png)

7. Ubah fungsi up() pada file create_tags_table
![Alt text](SS07/image-6.png)

8. Ubah fungsi up() pada file create_post_tag_table
![Alt text](SS07/image-7.png)

9. Kemudian jalankan command
![Alt text](SS07/image-8.png)


Pembuatan Model

1. Buatlah file dengan nama Post.php dan isi dengan baris kode berikut
![Alt text](SS07/image-9.png)

2. Buatlah file dengan nama Comment.php dan isi dengan baris kode berikut
![Alt text](SS07/image-10.png)

3. Buatlah file dengan nama Tag.php dan isi dengan baris kode berikut
![Alt text](SS07/image-11.png)


Relasi One-to-Many

1. Tambahkan fungsi comments() pada file Post.php
![Alt text](SS07/image-12.png)

2. Tambahkan fungsi post() dan atribut postId pada $fillable pada file Comment.php
![Alt text](SS07/image-13.png)

3. Buatlah file PostController.php dan isilah dengan baris kode berikut
![Alt text](SS07/image-14.png)

4. Buatlah file CommentController.php dan isilah dengan baris kode berikut
![Alt text](SS07/image-15.png)

5. Tambahkan baris berikut pada routes/web.php
![Alt text](SS07/image-16.png)

6. Buatlah satu post menggunakan Postman
![Alt text](SS07/image-17.png)

7. Buatlah satu comment menggunakan Postman
![Alt text](SS07/image-18.png)

8. Tampilkan post menggunakan Postman
![Alt text](SS07/image-19.png)


Relasi Many-to-Many

1. Tambahkan fungsi tags() pada file Post.php
![Alt text](SS07/image-20.png)

2. Tambahkan fungsi posts() pada file Tag.php
![Alt text](SS07/image-21.png)

3. Buatlah file TagController.php dan isilah dengan baris kode berikut
![Alt text](SS07/image-22.png)

4. Tambahkan fungsi addTag dan response tags pada PostController.php
![Alt text](SS07/image-23.png)

5. Tambahkan baris berikut pada routes/web.php
![Alt text](SS07/image-24.png)

6. Buatlah satu tag menggunakan Postman
![Alt text](SS07/image-25.png)

7. Tambahkan tag “jadul” pada post “disana engkau berdua”
![Alt text](SS07/image-26.png)

8. Tampilkan post “disana engkau berdua” menggunakan Postman
![Alt text](SS07/image-27.png)

9. Buatlah postingan “tanpamu apa artinya” menggunakan Postman
![Alt text](SS07/image-29.png)

10. Tambahkan tag “jadul” pada postingan “tanpamu apa artinya”
![Alt text](SS07/image-30.png)

11. Buatlah tag “lagu” menggunakan Postman
![Alt text](SS07/image-31.png)

12. Tambahkan tag “lagu” pada postingan “tanpamu apa artinya”
![Alt text](SS07/image-32.png)

13. Tampilkan post pertama
![Alt text](SS07/image-33.png)

14. Tampilkan post kedua
![Alt text](SS07/image-34.png)