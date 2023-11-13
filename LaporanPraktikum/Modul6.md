# Model, Controller dan Request-Response Handler  

## Langkah Percobaan    
* ### Model   
1. Pastikan terdapat tabel users yang dibuat menggunakan migration pada bab sebelumnya.  
![img1](../SS/Modul6/1.png)  
Tabel user yang berisi informasi ide, created_at, update_at, name, email, password.  
2. Bersihkan isi User.php yang ada sebelumnya dan isi dengan baris kode berikut.  
![img1](../SS/Modul6/2.png)  
Mengganti isi User.php dengan syntax yang diberikan.  

* ### Model   
1. Membuat salinan ExampleController.php pada folder app/Http/Controllers dengan nama HomeController.php dan membuat fungsi index().  
![img1](../SS/Modul6/3.png)  
Membuat salinan dari file ExampleController dan mengganti nya dengan nama HomeController kemudian menambahkan fungsi index().  
2. Mengubah route / pada file routes/web.php menjadi seperti ini  
![img1](../SS/Modul6/4.png)  
Menambahkan route yang merujuk ke fungsi index pada HomeController.php.  
3. Menjalankan aplikasi  
![img1](../SS/Modul6/5.png)  
Menampilkan kalimat "Hello, from lumen!"  

* ### Request Handler  
1. Melakukan import library Request dengan menambahkan baris berikut di bagian atas file HomeController.php  
![img1](../SS/Modul6/6.png)  
Melakukan import library Request  
2. Mengubah fungsi index  dengan paramater request  
![img1](../SS/Modul6/7.png)  
3. Menjalankan aplikasi  
![img1](../SS/Modul6/8.png)  
Menampilkan kalimat “Hello, from lumen! We got your request from endpoint: test” dimana kata “test” diambil dari request pada url localhost  

* ### Response Handler  
1. Melakukan import library Response dengan menambahkan baris berikut di bagian atas file Controllers  
![img1](../SS/Modul6/9.png)  
Melakukan import library Response  
2. Membuat fungsi hello()  
![img1](../SS/Modul6/10.png)  
Menambahkan fungsi hello() pada HomeController.php  
3. Menambahkan route /hello pada file routes/web.php  
![img1](../SS/Modul6/11.png)  
4. Menjalankan aplikasi pada route /hello  
![img1](../SS/Modul6/13.png)  
* ### Response Handler  
1. Melakukan import model User dengan menambahkan baris berikut di bagian atas file  Controllers  
![img1](../SS/Modul6/14.png)  
Menambahkan import model User pada HomeController.php  
2. Menambahkan ketiga fungsi berikut di HomeController.php  
![img1](../SS/Modul6/15.png)  
Menambahkan tiga fungsi sesuai perintah soal yaitu defaultUser(), createUser(), dan getUsers().  
3. Menambahkan ketiga route pada file routes/web.php menggunakan group route  
![img1](../SS/Modul6/16.png)  
4. Menjalankan aplikasi pada route /users/default menggunakan Postman  
![img1](../SS/Modul6/17.png)  
![img1](../SS/Modul6/18.png)  
![img1](../SS/Modul6/19.png)  