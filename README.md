# Responsi_Prak.Tek.Cloud

Langkah Pertama untuk membuat dan menjalankan website-profil:

1. Buat direktori untuk website-profil: ```mkdir website-profil```

2. Buat file `index.html` untuk website-profil
   Simpan file dalam `index.html` di dalam direktori `website-profil`
   Pastikan file `foto.png` ada dalam direktori `website-profil` jika ingin menampilkan foto profil.

3. Dockerfile untuk website-profil
   Buat sebuah file bernama `Dockerfile` di dalam direktori `website-profil` lalu
   klik ```cd website-profil```
   Ini akan mengambil semua file (termasuk `index.html` dan `foto.png`) dari direktori saat ini (`.`) dan menyalinnya ke dalam direktori default Nginx di dalam container.
   
4. Build Docker image untuk website-profil
   Buka terminal, masuk ke direktori `website-profil`, lalu jalankan perintahnya
    ```docker build -t website-profil .```
   Ini akan membuat Docker image dengan nama `website-profil`.
   
5. Jalankan container untuk website-profil: ```docker run -d --name website-profil --network my-Novryeda-Wahyoenarta-network -p 8081:80 website-profil```




Langkah Kedua untuk membuat dan menjalankan website-utama:

1. Buat direktori untuk website-utama: ```mkdir website-utama```

2. Buat file `index.html` untuk website-utama
   Simpan kode HTML berikut dalam `index.html` di dalam direktori `website-utama`.
   
3. Dockerfile untuk website-utama
   Buat sebuah file bernama `Dockerfile` di dalam direktori `website-utama` dengan konten yang sama seperti untuk website-profil.
   
4. Build Docker image untuk website-utama
   klik ```cd website-utama```
  ```docker build -t website-utama .```
   Buka terminal, masuk ke direktori `website-utama`, lalu jalankan.
   
5. Selanjutnya jalankan container untuk website-utama: ```docker run -d --name website-utama --network my-Novryeda-Wahyoenarta-network -p 8080:80 website-utama```
   
6. Selesai 

Dengan langkah-langkah ini, Anda akan dapat menjalankan kedua website statis Anda menggunakan Docker dengan Nginx sebagai server web.


