Praktikum 1 : Instalasi Lumen, MongoDB dan Konfigurasi APP Key



Nama : Muhammad Yusuf Habibie

NIM : 215150701111044

Tanggal : 3 September 2023

Asisten : Iqbal Biondy



Instalasi MongoDB

a. Buka halaman https://www.mongodb.com/try/download/community dan klik Download
![Alt text](SS01/image.png)

b. Jalankan mongodb-windows-x86_64-6.0.1-signed.msi
![Alt text](SS01/image-1.png)

c. Pada welcome screen klik Next
![Alt text](SS01/image-2.png)

d. Pada bagian End-User License Agreement centang “I accept the terms in the License Agreement” dan klik Next
![Alt text](SS01/image-3.png)

e. Pada bagian Choose Setup Type klik Complete
![Alt text](SS01/image-4.png)

f. Pada bagian Service Configuration tanpa mengubah apapun klik Next
![Alt text](SS01/image-5.png)

g. Pastikan “Install MongoDB Compass” tercentang
![Alt text](SS01/image-6.png)

h. Pada langkah terakhir klik Install
![Alt text](SS01/image-7.png)

i. Tunggu hingga tahap instalasi selesai
![Alt text](SS01/image-8.png)

j. MongoDB Compass akan terbuka secara otomatis
![Alt text](SS01/image-9.png)

k. Klik Finish untuk menutup dialog instalasi



Instalasi Lumen

a. Buka folder yang diinginkan pada file explorer
![Alt text](SS01/image-10.png)

b. Copy path dari folder yang diinginkan
![Alt text](SS01/image-11.png)

c. Buka cmd
![Alt text](SS01/image-12.png)

d. Buka path pada cmd (cd )
![Alt text](SS01/image-13.png)

e. Jalankan command untuk menginstall lumen pada folder tersebut (composer create-project --prefer-dist laravel/lumen lumenapi)
![Alt text](SS01/image-14.png)

f. Buka folder projek lumen kita dan jalankan projek kita (php -S localhost:8000 -t public)
![Alt text](SS01/image-15.png)

Konfigurasi APP_KEY

a. Buka file web.php pada folder routes, kemudian buat endpoint yang akan mengembalikan random string dengan panjang 32 :

$router->get('/key', function () {

return Str::random(32);

});
![Alt text](SS01/image-16.png)

b. Melakukan generate dari website https://pinetools.com/random-string-generator
![Alt text](SS01/image-17.png)

c. Setelah mendapat random string kita akan memasukkan random string tersebut ke file .env kita pada bagian APP_KEY (APP_KEY=<<random_string>>)
![Alt text](SS01/image-18.png)