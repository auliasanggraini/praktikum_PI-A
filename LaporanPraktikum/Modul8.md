# Register, Authentication dan Authorization  

## Langkah Percobaan    
* ### Register   
1. Pastikan terdapat tabel users yang dibuat menggunakan migration pada bab 3️⃣Basic Routing dan Migration  
![img1](../SS/Modul8/1.png)  
2. Pastikan terdapat model User.php yang digunakan pada bab 5️⃣Model, Controller dan Request-Response Handler.  
![img1](../SS/Modul8/2.png)  
3. Buatlah file AuthController.php dan isilah dengan baris kode berikut  
![img1](../SS/Modul8/3.png)  
4. Tambahkan baris berikut pada routes/web.php   
![img1](../SS/Modul8/4.png)  
a. Jalankan aplikasi pada endpoint /auth/register dengan body berikut  
![img1](../SS/Modul8/5.png)  

* ### Authentication  
1. Buatlah fungsi login(Request $request) pada file AuthController.php  
![img1](../SS/Modul8/6.png)  
2. Tambahkan baris berikut pada routes/web.php  
![img1](../SS/Modul8/7.png)  
3. Jalankan aplikasi pada endpoint /auth/login dengan body berikut  
![img1](../SS/Modul8/8.png)  

* ### Token  
1. Jalankan perintah berikut untuk membuat migrasi baru  
![img1](../SS/Modul8/11.png)  
2. Tambahkan baris berikut pada migration yang baru terbuat  
![img1](../SS/Modul8/12.png)  
3. Tambahkan atribut token di $fillable pada User.php  
![img1](../SS/Modul8/13.png)  
4. Tambahkan baris berikut pada file AuthController.php  
![img1](../SS/Modul8/14.png)  
5. Jalankan perintah di bawah untuk menjalankan migrasi terbaru  
![img1](../SS/Modul8/15.png)  
6. Jalankan aplikasi pada endpoint /auth/login dengan body berikut. Salinlah token yang didapat ke notepad  
![img1](../SS/Modul8/16.png)  

* ### Authorization  
1. Buatlah file Authorization.php pada folder App/Http/Middleware  
![img1](../SS/Modul8/9.png)  
2. Tambahkan middleware yang baru dibuat pada bootstrap/app.php.  
![img1](../SS/Modul8/17.png)  
3. Buatlah fungsi home() pada HomeController.php  
![img1](../SS/Modul8/18.png)  
4. Tambahkan baris berikut pada routes/web.php  
![img1](../SS/Modul8/10.png)  