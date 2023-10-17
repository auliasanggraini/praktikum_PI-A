# Basic Routing dan Migration  

## Langkah Percobaan  
* ### 1. GET
Untuk menambahkan endpoint dengan method GET pada aplikasi kita, kita dapat mengunjungi file web.php pada folder routes. Kemudian tambahkan baris ini pada akhir file  
![img1](../SS/Modul4/1.png)  
Setelah itu coba jalankan aplikasi dengan command,  
![img1](../SS/Modul4/2.png)  
Setelah aplikasi berhasil dijalankan, kita dapat membuka browser dengan url, http://localhost:8000/get , path yang akan kita akses akan berbentuk demikian, http://{BASE_URL}{PATH} ,  
![img1](../SS/Modul4/3.png)  
jika BASE_URL kita adalah localhost:8000 dan PATH kita adalah /get , maka url akan berbentuk seperti diatas.  

* ### 2. POST, PUT, PATCH, DELETE, dan OPTIONS
Sama halnya saat menambahkan method GET, kita dapat menambahkan methode POST, PUT, PATCH, DELETE, dan OPTIONS pada file web.php dengan code seperti ini,   
![img1](../SS/Modul4/4.png)  
Setelah selesai menambahkan route untuk method POST, PUT, PATCH, DELETE, dan OPTIONS, kita dapat menjalankan server seperti pada saat percobaan GET. Setelah server berhasil menyala, kita dapat membuka aplikasi Postman atau Insomnia atau kita juga dapat menggunakan PowerShell (Windows) / Terminal (Linux atau Mac) untuk melakukan request ke server. Namun, pada percobaan kali ini kita akan menggunakan extensions pada VSCode yaitu Thunder Client.  

a. Menginstall ekstensi dengan membuka panel extensions lalu mencari thunder client  
![img1](../SS/Modul4/5.png)  

b. Setelah menginstall Thunder Client, akan melihat logo seperti petir pada activity bar kita (sebelah kiri).  
![img1](../SS/Modul4/6.png)  

c. Membuat request dengan menekan "New Request" pada ekstensi  
![img1](../SS/Modul4/7.png)  

d. Setelah itu kita dapat memasukkan method dan url yang dituju  
![img1](../SS/Modul4/8.png)  

e. Akses url yang baru saja ditambahkan pada aplikasi dengan methodnya  
![img1](../SS/Modul4/9.png)  
![img1](../SS/Modul4/10.png)

* ### Migrasi Database
a. Sebelum melakukan migrasi database pastikan server database aktif kemudian pastikan sudah membuat database dengan nama lumenapi  
![img1](../SS/Modul4/11.png)  
b. Kemudian ubah konfigurasi database pada file .env menjadi seperti ini  
![img1](../SS/Modul4/12.png)  

c. Setelah mengubah konfigurasi pada file .env, kita juga perlu menghidupkan beberapa library bawaan dari lumen dengan membuka file app.php pada folder bootstrap dan mengubah baris ini,  
//$app->withFacades();  
//$app->withEloquent();  

Menjadi,  

$app->withFacades();  
$app->withEloquent();  
![img1](../SS/Modul4/13.png)  

d. Setelah itu jalankan command berikut untuk membuat file migration,  
php artisan make:migration create_users_table # membuat migrasi untuk tabel users  
php artisan make:migration create_products_table # membuat migrasi untuk tabel products  

![img1](../SS/Modul4/14.png)  
![img1](../SS/Modul4/15.png)  

Setelah menjalankan 2 syntax diatas akan terbuat 2 file pada folder database/migrations dengan format YYYY_MM_DD_HHmmss_nama_migrasi. Pada file migrasi kita akan menemukan fungsi up() dan fungsi down(), fungsi up() akan digunakan pada saat kita melakukan migrasi, fungsi down() akan digunakan saat kita ingin me-rollback migrasi  

e. Ubah fungsi up pada file migrasi create_users_table  
![img1](../SS/Modul2/16.png)  

f. Ubah fungsi up pada file migrasi create_products_table  
![img1](../SS/Modul4/17.png)  

g. Kemudian jalankan command,  

php artisan migrate  
![img1](../SS/Modul4/18.png)  
