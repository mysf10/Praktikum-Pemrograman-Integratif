Praktikum 2 : CRUD MongoDB



Nama : Muhammad Yusuf Habibie

NIM : 215150701111044

Tanggal : 12 September 2023

Asisten : Iqbal Biondy



MongoDBCompass

1. Lakukan koneksi ke MongoDB menggunakan connection string
![Alt text](SS02/image.png)

2. Buat database dengan melakukan klik “Create Database”
![Alt text](SS02/image-1.png)

3. Lakukan insert buku pertama dengan melakukan klik “Add Data”, pilih “Insert Document”, isi dengan data yang diinginkan dan klik “Insert”
![Alt text](SS02/image-2.png)

4. Lakukan insert buku kedua dengan cara yang sama.
![Alt text](SS02/image-3.png)

5. Lakukan pencarian buku dengan author “Osamu Dazai” dengan mengisi filter yang diinginkan dan klik “Find”
![Alt text]SS02/image-4.png)

6. Lakukan perubahan summary pada buku “No Longer Human” menjadi “Buku yang bagus (<NAMA>,<NIM>) dengan melakukan klik “Edit Document” (berlambang pensil), mengisi nilai summary yang baru, dan melakukan klik “Update”
![Alt text](SS02/image-5.png)

7. Lakukan penghapusan pada buku “I Am a Cat” dengan melakukan klik “Remove Document” (berlambang tong sampah) dan melakukan klik “Delete”
![Alt text](SS02/image-6.png)


MongoDB Shell

1. Lakukan koneksi ke MongoDB Server dengan menjalankan command mongosh bagi yang menggunakan terminal build in OS, Apabila kalian menggunakan MongoDB atlas, silahkan copy connection string dari MongoDB atlas kalian masing-masing dan paste kan di terminal kalian sehingga tampilan terminal kalian akan menjadi seperti berikut
![Alt text](SS02/image-7.png)

2. Mencoba melihat list database yang ada di server dengan menjalankan command show dbs
![Alt text](SS02/image-8.png)

Untuk berpindah ke database “bookstore” gunakan command use bookstore , kalian dapat memastikan telah berpindah ke database yang benar dengan melihat tulisan sebelum tanda “>”
![Alt text](SS02/image-9.png)

Cobalah untuk melihat collection yang ada pada database tersebut dengan menggunakan command show collections
![Alt text](SS02/image-10.png)

3. Lakukan insert buku “Overlord I” dengan menggunakan command db.books.insertOne(<data kalian>) , setelah insert buku berhasil maka MongoDB akan mengembalikan pesan sebagai berikut.
![Alt text](SS02/image-11.png)

4. Lakukan insert buku “The Setting Sun” dan “Hujan” dengan insert many dengan menggunakan command db.books.insertMany(<data kalian>) , dan akan mengembalikan pesan sebagai berikut.
![Alt text](SS02/image-12.png)

5. Lakukan pencarian buku dengan menggunakan command db.books.find() untuk melakukan pencarian semua buku.
![Alt text](SS02/image-13.png)

6. Tampilkan seluruh buku dengan author “Osamu Dazai” dengan mengisi argument pada find() dengan menggunakan command db.books.find({<filter yang ingin diisi>})
![Alt text](SS02/image-14.png)

7. Lakukan perubahan summary pada buku “Hujan” menjadi “Buku yang bagus (<NAMA>,<NIM>) dengan mengunakan command db.books.updateOne({<filter>}, {$set: {<data yang akan di update>}}) sehingga output yang dihasilkan oleh MongoDB akan menjadi seperti berikut
![Alt text](SS02/image-15.png)

8. Lakukan perubahan publisher menjadi “Yen Press” pada semua buku “Osamu Dazai” dengan menggunakan command db.books.updateMany({<filter>}, {$set: {<data yang akan di update>}})
![Alt text](SS02/image-16.png)

9.Lakukan penghapusan pada buku “Overlord I” dengan menggunakan command db.books.deleteOne({<argument>})
![Alt text](SS02/image-17.png)

10. Lakukan penghapusan pada semua buku “Osamu Dazai dengan menggunakan command db.books.deleteMany({<argument>})
![Alt text](SS02/image-18.png)
