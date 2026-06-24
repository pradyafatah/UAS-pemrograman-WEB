# Praktikum Pemrograman Web 2

## Identitas Mahasiswa

**Nama :** Pradya Muhamad Fatah  
**NIM :** 312410408  
**Kelas :** TI.24.C1

---

# Deskripsi Repository

Repository ini berisi kumpulan tugas Praktikum Pemrograman Web 2 yang dikerjakan menggunakan Framework CodeIgniter 4 dan VueJS. Praktikum dimulai dari implementasi AJAX untuk komunikasi asynchronous, pengembangan REST API, integrasi frontend menggunakan VueJS, penerapan Single Page Application (SPA), hingga implementasi sistem keamanan menggunakan Authentication, Navigation Guards, Token Authentication, dan Axios Interceptors.

Tujuan dari seluruh rangkaian praktikum ini adalah memahami proses pengembangan aplikasi web modern yang memisahkan frontend dan backend sehingga aplikasi menjadi lebih fleksibel, responsif, dan aman.

---

# Daftar Praktikum

| No | Praktikum | Materi |
|----|-----------|---------|
| 11 | VueJS Frontend API | Integrasi VueJS dengan REST API |
| 12 | VueJS Components & Routing | Single Page Application (SPA) |
| 13 | Authentication & Navigation Guards | Login dan Proteksi Halaman |
| 14 | API Security & Axios Interceptors | Keamanan API Berbasis Token |

---


# Praktikum 11 – VueJS Frontend API

## Penjelasan

Pada praktikum ini dibuat aplikasi frontend menggunakan VueJS 3 yang terhubung dengan REST API CodeIgniter 4. VueJS digunakan untuk membangun antarmuka pengguna yang dinamis, sedangkan Axios digunakan sebagai media komunikasi antara frontend dan backend.

Aplikasi yang dibuat memiliki fitur CRUD artikel. Data artikel ditampilkan dalam bentuk tabel dan seluruh proses tambah, ubah, serta hapus data dilakukan melalui request ke REST API.

Karena menggunakan VueJS dan Axios, perubahan data dapat langsung terlihat tanpa perlu memuat ulang halaman sehingga aplikasi menjadi lebih interaktif dan modern.

## Hasil

Frontend VueJS berhasil mengambil data dari REST API dan menampilkannya ke dalam halaman web. Seluruh fitur CRUD dapat berjalan dengan baik dan perubahan data dapat langsung terlihat secara realtime.

### Dokumentasi

- Screenshot Daftar Artikel
  <img width="1024" height="640" alt="111" src="https://github.com/user-attachments/assets/6fcc3e4f-7cf9-4670-bf47-c894b5055027" />


- Screenshot Tambah Data
- Screenshot Edit Data
- Screenshot Hapus Data

---

# Praktikum 12 – VueJS Components dan Routing (SPA)

## Penjelasan

Pada praktikum ini aplikasi VueJS dikembangkan menjadi Single Page Application (SPA) menggunakan Vue Router. Konsep SPA memungkinkan perpindahan halaman dilakukan tanpa reload browser sehingga pengalaman pengguna menjadi lebih baik.

Struktur aplikasi dipisahkan menjadi beberapa komponen seperti Home, Artikel, dan About. Setiap komponen memiliki fungsi masing-masing sehingga kode program menjadi lebih terorganisir dan mudah dikelola.

Vue Router digunakan untuk mengatur navigasi antar halaman. Dengan routing ini, pengguna dapat berpindah halaman secara cepat tanpa harus meminta ulang seluruh halaman kepada server.

## Hasil

Aplikasi berhasil menerapkan konsep Single Page Application (SPA). Perpindahan halaman berlangsung cepat tanpa refresh browser dan seluruh komponen dapat berjalan sesuai fungsinya. Halaman About juga berhasil ditambahkan sebagai bagian dari tugas praktikum.

### Dokumentasi

- Screenshot Halaman Beranda
- Screenshot Kelola Artikel
- Screenshot Halaman About
- Screenshot Routing SPA

---

# Praktikum 13 – Authentication dan Navigation Guards

## Penjelasan

Pada praktikum ini ditambahkan sistem autentikasi pengguna menggunakan API Login yang dibuat pada backend CodeIgniter 4. Data username dan password dikirim ke server menggunakan Axios untuk diverifikasi. Jika data valid, server akan mengirimkan token yang kemudian disimpan ke Local Storage browser.

Selain autentikasi, diterapkan Navigation Guards menggunakan Vue Router. Fitur ini berfungsi untuk membatasi akses ke halaman tertentu agar hanya dapat dibuka oleh pengguna yang telah login.

Ketika pengguna mencoba mengakses halaman yang diproteksi tanpa autentikasi, sistem akan menolak akses dan mengarahkan pengguna ke halaman login.

## Hasil

Sistem login berhasil berjalan dengan baik. Pengguna yang belum login tidak dapat mengakses halaman Kelola Artikel maupun About. Setelah login berhasil, seluruh halaman yang diproteksi dapat diakses dan menu Login berubah menjadi Logout secara otomatis.

### Dokumentasi

- Screenshot Form Login
- Screenshot Akses Ditolak
- Screenshot Login Berhasil
- Screenshot Halaman Artikel
- Screenshot Logout

---

# Praktikum 14 – API Security dan Axios Interceptors

## Penjelasan

Pada praktikum terakhir ini dilakukan peningkatan keamanan aplikasi menggunakan Token-Based Authentication. Sebelumnya keamanan hanya diterapkan pada sisi client menggunakan Navigation Guards, namun endpoint API masih dapat diakses langsung menggunakan aplikasi seperti Postman.

Untuk mengatasi hal tersebut dibuat ApiAuthFilter pada CodeIgniter 4 yang bertugas memeriksa token yang dikirim melalui HTTP Header Authorization. Selain itu digunakan Axios Interceptors pada frontend VueJS untuk menyisipkan token secara otomatis ke setiap request yang dikirim ke server.

Dengan kombinasi kedua mekanisme tersebut, keamanan aplikasi menjadi lebih baik karena proteksi dilakukan baik pada sisi client maupun server.

## Hasil

Endpoint API berhasil diamankan dari akses yang tidak memiliki token. Pengujian menggunakan Postman menunjukkan bahwa request tanpa token ditolak dengan status 401 Unauthorized. Setelah pengguna login melalui aplikasi VueJS, seluruh proses CRUD dapat berjalan normal karena token dikirim otomatis oleh Axios Interceptors.

### Dokumentasi

- Screenshot ApiAuthFilter
- Screenshot Route API Protected
- Screenshot Error 401 Unauthorized
- Screenshot Axios Interceptors
- Screenshot Authorization Bearer Token
- Screenshot CRUD Artikel

---

# Kesimpulan

Berdasarkan seluruh rangkaian praktikum yang telah dilakukan, berhasil dibuat sebuah aplikasi web modern menggunakan CodeIgniter 4 dan VueJS. Pengembangan dimulai dari implementasi AJAX untuk komunikasi data secara asynchronous, pembuatan REST API sebagai backend service, integrasi frontend menggunakan VueJS, hingga penerapan konsep Single Page Application (SPA).

Selain itu, sistem juga dilengkapi dengan fitur autentikasi pengguna menggunakan Login API, Navigation Guards untuk membatasi akses halaman tertentu, serta Token-Based Authentication yang diperkuat dengan Axios Interceptors dan ApiAuthFilter. Dengan penerapan teknologi tersebut, aplikasi menjadi lebih interaktif, responsif, terstruktur, dan aman untuk digunakan dalam pengelolaan data berbasis web.
