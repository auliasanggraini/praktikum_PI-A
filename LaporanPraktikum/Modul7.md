# Relasi One-to-Many dan Many-to-Many  

## Langkah Percobaan    
* ### Model   
1. Sebelum membuat migrasi database atau membuat tabel pastikan server database aktif kemudian pastikan sudah membuat database dengan nama lumenpost  
![img1](../SS/Modul7/1.png)  
Membuat database lumenpost  
2. Kemudian ubah konfigurasi database pada file .env menjadi seperti berikut  
![img1](../SS/Modul7/2.png)  
Mengubah konfigurasi database pada file .env  
3. Setelah mengubah konfigurasi pada file .env, kita juga perlu menghidupkan beberapa library bawaan dari lumen dengan membuka file app.php pada folder bootstrap dan diubah.  
![img1](../SS/Modul7/3.png)  
Menghidupkan library bawaan dari lumen pada file app.php  
4. Setelah itu jalankan command berikut untuk membuat file migration  
![img1](../SS/Modul7/4.png)  
Membuat file migration  
5. Ubah fungsi up() pada file migrasi create_posts_table  
![img1](../SS/Modul7/5.png)  
Mengubah fungsi up() pada file create_posts_table.php  
6. Ubah fungsi up() pada file create_comments_table  
![img1](../SS/Modul7/6.png)  
Mengubah fungsi up() pada file create_comments_table.php  
7. Ubah fungsi up() pada file create_tags_table  
![img1](../SS/Modul7/7.png)  
Mengubah fungsi up() pada file create_tags_table.php  
8. Ubah fungsi up() pada file create_post_tag_table  
![img1](../SS/Modul7/8.png)  
Mengubah fungsi up() pada file create_post_tak_table.php  
9. Kemudian jalankan command  
![img1](../SS/Modul7/9.png)  
Berhasil menyimpan perubahan yang dilakukan  

* ### Pembuatan Model   
10. Buatlah file dengan nama Post.php dan isi dengan baris kode berikut  
![img1](../SS/Modul7/10.png)  
Membuat file pada folder Models dengan nama Post.php  
11. Buatlah file dengan nama Comment.php dan isi dengan baris kode berikut  
![img1](../SS/Modul7/11.png)  
Membuat file pada folder Models dengan nama Comment.php  
12. Buatlah file dengan nama Tag.php dan isi dengan baris kode berikut  
![img1](../SS/Modul7/12.png)  
Membuat file dengan nama Tak.php pada filder Models  

* ### Relasi One-to-Many   
1. Tambahkan fungsi comments() pada file Post.php  
![img1](../SS/Modul7/13.png)  
Menambahkan fungsi comments() pada file Post.php  
2. Tambahkan fungsi post() dan atribut postId pada $fillable pada file Comment.php  
![img1](../SS/Modul7/14.png)  
Menambahkan fungsi post() dan atribut postId pada bagian $fillable di file Comment.php  
3. Buatlah file PostController.php dan isilah dengan baris kode berikut  
![img1](../SS/Modul7/15.png)  
Membuat file PostController.php pada folder Controllers dan mengisi baris kode yang diberikan  
4. Buatlah file CommentController.php dan isilah dengan baris kode berikut  
![img1](../SS/Modul7/16.png)  
Membuat file CommentController.php pada folder Controllers dan mengisi baris kode yang diberikan  
5. Tambahkan baris berikut pada routes/web.php  
![img1](../SS/Modul7/17.png)  
Menambahkan baris kode pada file web.php di folder routes  
6. Buatlah satu post menggunakan Postman  
![img1](../SS/Modul7/18.png)  
Membuat satu post menggunakan Postman  
7. Buatlah satu comment menggunakan Postman  
![img1](../SS/Modul7/19.png)  
Membuat satu comment pada Postman  
8. Tampilkan post menggunakan Postman  
![img1](../SS/Modul7/20.png)  
Menampilkan list post yang tersimpan  

* ### Relasi Many-to-Many  
1. Tambahkan fungsi tags() pada file Post.php  
![img1](../SS/Modul7/21.png)  
Menambahkan fungsi tags() pada Post.php  
2. Tambahkan fungsi posts() pada file Tag.php  
![img1](../SS/Modul7/22.png)  
Menambahkan fungsi posts() pada Tag.php  
3. Buatlah file TagController.php dan isilah dengan baris kode berikut  
![img1](../SS/Modul7/23.png)  
Membuat file TagController.php dan mengisi baris kode yang diberikan  
4. Tambahkan fungsi addTag dan response tags pada PostController.php  
![img1](../SS/Modul7/24.png)  
Menambahkan baris fungsi addTag dan response tags pada PostController.php  
5. Tambahkan baris berikut pada routes/web.php  
![img1](../SS/Modul7/25.png)  
Menambahkan routes tag pada web.php  
6. Buatlah satu tag menggunakan Postman  
![img1](../SS/Modul7/26.png)  
Membuat satu tak dengan isi “jadul”  
7. Tambahkan tag “jadul” pada post “disana engkau berdua”  
![img1](../SS/Modul7/27.png)  
Menambahkan tag “jadul” pada post “disana engkau berada”  
8. Tampilkan post “disana engkau berdua” menggunakan Postman  
![img1](../SS/Modul7/28.png)  
9. Buatlah postingan “tanpamu apa artinya” menggunakan Postman  
![img1](../SS/Modul7/29.png)  
Membuat postingan “tanpamu apa artinya” di Postman  
10. Tambahkan tag “jadul” pada postingan “tanpamu apa artinya”  
![img1](../SS/Modul7/30.png)  
Menambahkan tak “jadul” pada postingan 2  
11. Buatlah tag “lagu” menggunakan Postman  
![img1](../SS/Modul7/31.png)  
12. Tambahkan tag “lagu” pada postingan “tanpamu apa artinya”  
![img1](../SS/Modul7/32.png)  
13. Tampilkan post pertama  
![img1](../SS/Modul7/33.png)  
14. Tampilkan post kedua  
![img1](../SS/Modul7/34.png)    
Tag “jadul” yang berada pada dua post menunjukkan satu tag dapat berada di banyak post.  
Post “tanpamu apa artinya” yang memiliki dua tag menunjukkan satu post dapat memiliki banyak tag  