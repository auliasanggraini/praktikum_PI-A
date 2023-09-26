# Integrasi MongoDB dan Express

## Percobaan instalasi NodeJS
* ### Langkah 1
> Membuka halaman

* ### Langkah 2
> Download dan jalankan node setup  

* ### Langkah 3
> Setelah instalasi selesai jalankan command node -v untuk memeriksa apakah NodeJS sudah terinstall.  
![img1](../SS/Modul3/1.png)

## Inisiasi project Express dan pemasangan package
* ### Langkah 1
> Melakukan pembuatan folder dengan nama express-mongodb dan masuk ke dalam folder tersebut lalu buka melalui text editor masing-masing

* ### Langkah 2
> Melakukan npm init untuk mengenerate file package.json dengan menggunakan command npm init -y
![img1](../SS/Modul3/2.png)  

* ### Langkah 3
> Melakukan instalasi express, mongoose, dan dotenv dengan menggunakan command npm i express mongoose dotenv. 
![img1](../SS/Modul3/3.png)

## Koneksi Express ke MongoDB
* ### Langkah 1
>Buatlah file index.js pada root folder dan masukkan kode di bawah ini
![img1](../SS/Modul3/4.png)

* ### Langkah 2
> Melakukan pembuatan file .env dan masukkan baris berikut
![img1](../SS/Modul3/5.png)  
>Setelah itu ubahlah kode pada listening port menjadi berikut dan coba jalankan aplikasi kembali
![img1](../SS/Modul3/6.png) 
![img1](../SS/Modul3/7.png) 

* ### Langkah 3
> Copy connection string yang terdapat pada compas atau atlas dan paste kan pada .env seperti berikut 
![img1](../SS/Modul3/8.png)

* ### Langkah 4
> Menambahkan baris kode berikut pada file index.js
![img1](../SS/Modul3/9.png)
![img1](../SS/Modul3/10.png)

## Pembuatan Routing
* ### Langkah 1
>Melakukan pembuatan direktori routes di tingkat yang sama dengan index.js
![img1](../SS/Modul3/11.png)

* ### Langkah 2
> Buatlah file book.route.js di dalamnya
![img1](../SS/Modul3/12.png)  

* ### Langkah 3
> Menambahkan baris kode berikut untuk fungsi getAllBooks 
![img1](../SS/Modul3/13.png)

* ### Langkah 4
> Melakukan hal yang sama untuk getOneBook, createBook, updateBook, dan deleteBook
![img1](../SS/Modul3/14.png)

* ### Langkah 5
> Melakukan import book.route.js pada file index.js dan Menambahkan baris kode berikut 
![img1](../SS/Modul3/15.png)
![img1](../SS/Modul3/16.png)

* ### Langkah 6
> Uji salah satu endpoint dengan Postman 
![img1](../SS/Modul3/17.png)

## Pembuatan Controller
* ### Langkah 1
>Melakukan pembuatan direktori controllers di tingkat yang sama dengan index.js
![img1](../SS/Modul3/18.png)

* ### Langkah 2
> Buatlah file book.controller.js di dalamnya
![img1](../SS/Modul3/19.png)  

* ### Langkah 3
> Salin baris kode dari routes untuk fungsi getAllBooks 
![img1](../SS/Modul3/20.png)

* ### Langkah 4
> Melakukan hal yang sama untuk getOneBook, createBook, updateBook, dan deleteBook
![img1](../SS/Modul3/21.png)

* ### Langkah 5
> Melakukan import book.controller.js pada file book.route.js 
![img1](../SS/Modul3/22.png)

* ### Langkah 6
> Melakukan perubahan pada fungsi agar dapat memanggil fungsi dari book.controller.js 
![img1](../SS/Modul3/23.png)

* ### Langkah 7
> Melakukan pengujian kembali, pastikan response tetap sama
![img1](../SS/Modul3/24.png)

## Pembuatan Model
* ### Langkah 1
>Melakukan pembuatan direktori models di tingkat yang sama dengan index.js
![img1](../SS/Modul3/25.png)

* ### Langkah 2
> Buatlah file book.model.js di dalamnya
![img1](../SS/Modul3/19.png)  

* ### Langkah 3
> Menambahkan baris kode berikut sesuai dengan tabel di atas 
![img1](../SS/Modul3/20.png)

## Operasi CRUD
* ### Langkah 1
>Hapus semua data pada collection books
![img1](../SS/Modul3/26.png)

* ### Langkah 2
> Melakukan import book.model.js pada file book.controller.js
![img1](../SS/Modul3/27.png)  

* ### Langkah 3
> Melakukan perubahan pada fungsi createBook
![img1](../SS/Modul3/28.png)

* ### Langkah 4
> Buatlah dua buah buku dengan data di bawah ini dengan Postman
![img1](../SS/Modul3/29.png)
![img1](../SS/Modul3/30.png)

* ### Langkah 5
> Melakukan perubahan pada fungsi getAllBooks 
![img1](../SS/Modul3/32.png)

* ### Langkah 6
> Melakukan perubahan pada fungsi getOneBook 
![img1](../SS/Modul3/33.png)

* ### Langkah 7
> Menampilkan semua buku dengan Postman dengan perintah GET lalu masukkan url localhost:5000/books untuk mencari semua buku
![img1](../SS/Modul3/34.png)

* ### Langkah 8
> Menampilkan buku Dilan 1990 dengan Postman menggunakan perintah GET dan masukkan id buku Dilan 1990 
![img1](../SS/Modul3/36.png)

* ### Langkah 9
> Melakukan perubahan pada fungsi updateBook dengan syntax berikut 
![img1](../SS/Modul3/37.png)

* ### Langkah 10
> Mengubah judul buku Dilan 1991 menjadi “<NAMA PANGGILAN> 1991” dengan Postman, disini saya mengganti dengan nama “SAnggi 1991” 
![img1](../SS/Modul3/38.png)

* ### Langkah 11
>Melakukan perubahan pada fungsi deleteBook dengan syntax berikut 
![img1](../SS/Modul3/39.png)

* ### Langkah 12
> Menghapus buku Dilan 1990 dengan Postman menggunakan perintah DELETE lalu masukkan id dari buku 
![img1](../SS/Modul3/40.png)