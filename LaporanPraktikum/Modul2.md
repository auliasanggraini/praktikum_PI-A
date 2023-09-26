# MongoDB Compass dan Shell

## MongoDB Compass
* ### Langkah 1
> Melakukan koneksi ke MongoDB menggunakan connection string.  
![img1](../SS/1.png)

* ### Langkah 2
> Membuat database dengan klik “Create Database”  
![img1](../SS/2.png)

* ### Langkah 3
> Melakukan insert buku pertama dengan klik “Add Data”, pilih “Insert Document”, isi dengan data yang diinginkan dan klik “Insert”  
![img1](../SS/3.png)

* ### Langkah 4
> Melakukan insert buku kedua dengan cara yang sama.  
![img1](../SS/4.png)

* ### Langkah 5
> Melakukan pencarian buku dengan author “Kimino Nawasaki” dengan mengisi filter yang diinginkan dan klik “Find”  
![img1](../SS/5.png)

* ### Langkah 6
> Melakukan perubahan summary pada buku “Lorem ipsum dolor sit amet” menjadi “Buku yang bagus (<NAMA>,<NIM>) dengan klik “Edit Document” (berlambang pensil), mengisi nilai summary yang baru, dan klik “Update”  
![img1](../SS/6.png)

* ### Langkah 7
> Melakukan penghapusan pada buku “I Am a Rabbit” dengan klik “Remove Document" (berlambang tong sampah) dan klik “Delete"  
![img1](../SS/7.png)

## MongoDB Shell
* ### Langkah 1
> Melakukan koneksi ke MongoDB Server dengan menjalankan perintah mongosh bagi yang menggunakan terminal build in OS sehingga tampilan terminal kalian akan menjadi seperti berikut  
![img1](../SS/8.png)

* ### Langkah 2
> Melihat list database yang ada di server dengan menjalankan perintah show dbs  
![img1](../SS/9.png)

> Berpindah ke database “bookstore” menggunakan perintah use bookstore  
![img1](../SS/10.png)

> Melihat collection yang ada pada database tersebut dengan menggunakan perintah show collections  
![img1](../SS/11.png)

* ### Langkah 3
> Melakukan insert buku “Overlord I” menggunakan perintah db.books.insertOne(<data kalian>), setelah insert buku berhasil maka MongoDB akan mengembalikan pesansebagai berikut.  
![img1](../SS/12.png)

* ### Langkah 4
> Melakukan insert buku “The Setting Sun” dan “Hujan” dengan insert many menggunakan perintah db.books.insertMany(<data kalian>) , dan akan mengembalikan pesan sebagai berikut.  
![img1](../SS/13.png)

* ### Langkah 5
> Melakukan pencarian buku dengan menggunakan perintah db.books.find() untuk pencarian semua buku.  
![img1](../SS/14.png)

* ### Langkah 6
> Menampilkan seluruh buku dengan author “Osamu Dazai” menggunakan perintah db.books.find({<filter yang ingin diisi>}).  
![img1](../SS/15.png)

* ### Langkah 7
> Melakukan perubahan summary pada buku “Hujan” menjadi “Buku yang bagus (<NAMA>,<NIM>) mengunakan perintah db.books.updateOne({<filter>}, {$set: {<data yang akan di update>}}) sehingga output yang dihasilkan oleh MongoDB akan menjadi seperti berikut.  
![img1](../SS/16.png)

* ### Langkah 8
> Melakukan perubahan publisher menjadi “Yen Press” pada semua buku “Osamu Dazai” dengan menggunakan perintah db.books.updateMany({<filter>}, {$set: {<data yang akan di update>}}).  
![img1](../SS/17.png)

* ### Langkah 9
> Melakukan penghapusan pada buku “Overlord I” dengan menggunakan perintah db.books.deleteOne({<argument>})  
![img1](../SS/18.png)

* ### Langkah 10
> Melakukan penghapusan pada semua buku “Osamu Dazai dengan menggunakan perintah db.books.deleteMany({<argument>})  
![img1](../SS/19.png)