Percobaan instalasi NodeJS

1. Buka halaman https://nodejs.org/en
![Alt text](image.png)

2. Download dan jalankan node setup
![Alt text](image-1.png)

3. Setelah instalasi selesai jalankan command node -v untuk memeriksa apakah NodeJS sudah terinstall
![Alt text](image-2.png)


Inisiasi project Express dan pemasangan package

1. Lakukan pembuatan folder dengan nama express-mongodb dan masuk ke dalam folder tersebut lalu buka melalui text editor masing-masing
![Alt text](image-3.png)

2. Lakukan npm init untuk mengenerate file package.json dengan menggunakan command npm init -y
![Alt text](image-4.png)

3. Lakukan instalasi express, mongoose, dan dotenv dengan menggunakan command npm i express mongoose dotenv
![Alt text](image-5.png)


Koneksi Express ke MongoDB

1. Buatlah file index.js pada root folder dan masukkan kode di bawah ini

require('dotenv').config();

const express = require('express');

const mongoose = require('mongoose');

const app = express();

app.use(express.json());

app.get('/', (req, res) => {

res.status(200).json({

message: '<nama>,<nim>'

})

})

const PORT = 8000;

app.listen(PORT, () => {

console.log(`Running on port ${PORT}`);

})
![Alt text](image-6.png)

   Setelah itu coba jalankan aplikasi dengan command node index.js
   ![Alt text](image-7.png)

2. Lakukan pembuatan file .env dan masukkan baris berikut

PORT=5000
![Alt text](image-8.png)

Setelah itu ubahlah kode pada listening port menjadi berikut dan coba jalankan aplikasi kembali

...


const PORT = process.env.PORT || 8000;

app.listen(PORT, () => {

console.log(`Running on port ${PORT}`);

})
![Alt text](image-9.png)

3. Copy connection string yang terdapat pada compas atau atlas dan paste kan pada .env seperti berikut

MONGO_URI=<Connection string masing-masing>
![Alt text](image-10.png)

4. Tambahkan baris kode berikut pada file index.js

require('dotenv').config();

const express = require('express');

const mongoose = require('mongoose');

mongoose.connect(process.env.MONGO_URI);

const db = mongoose.connection;

db.on('error', (error) => {

console.log(error);

});

db.once('connected', () => {

console.log('Mongo connected');

})
![Alt text](image-11.png)

    Setelah itu coba jalankan aplikasi kembali
![Alt text](image-12.png)


Pembuatan routing

1. Lakukan pembuatan direktori routes di tingkat yang sama dengan index.js
![Alt text](image-13.png)

2. Buatlah file book.route.js di dalamnya
![Alt text](image-14.png)

3. Tambahkan baris kode berikut untuk fungsi getAllBooks

const router = require('express').Router();

router.get('/', function getAllBooks(req, res) {

res.status(200).json({

message: 'mendapatkan semua buku'

})

})

module.exports = router;
![Alt text](image-15.png)

4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan deleteBook
![Alt text](image-16.png)

5. Lakukan import book.route.js pada file index.js
![Alt text](image-17.png)

6. Uji salah satu endpoint dengan Postman
![Alt text](image-18.png)


Pembuatan controller

1. Lakukan pembuatan direktori controllers di tingkat yang sama dengan index.js
![Alt text](image-19.png)

2. Buatlah file book.controller.js di dalamnya
![Alt text](image-20.png)

3. Salin baris kode dari routes untuk fungsi getAllBooks
![Alt text](image-21.png)

4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan deleteBook
![Alt text](image-22.png)

5. Lakukan import book.controller.js pada file book.route.js
![Alt text](image-23.png)

6. Lakukan perubahan pada fungsi agar dapat memanggil fungsi dari book.controller.js
![Alt text](image-24.png)

7. Lakukan pengujian kembali, pastikan response tetap sama
![Alt text](image-25.png)


Pembuatan model

1. Lakukan pembuatan direktori models di tingkat yang sama dengan index.js
![Alt text](image-26.png)

2. Buatlah file book.model.js di dalamnya
![Alt text](image-27.png)

3. Tambahkan baris kode berikut sesuai dengan tabel di atas
![Alt text](image-28.png)


Operasi CRUD

1. Hapus semua data pada collection books
![Alt text](image-29.png)

2. Lakukan import book.model.js pada file book.controller.js
![Alt text](image-30.png)

3. Lakukan perubahan pada fungsi createBook
![Alt text](image-31.png)

4. Buatlah dua buah buku dengan data di bawah ini dengan Postman
