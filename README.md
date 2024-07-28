## Pengenalan Aplikasi Admin Ujian Kita
Aplikasi ini adalah aplikasi berbasis web yang bertindak sebagai database aplikasi "Ujian Kita" dan dapat digunakan secara gratis untuk sekarang.<br>
Berikut adalah cara menggunakan aplikasi ini:

## Step 1) Download Semua Template excel dan Web
Download dapat dilakukan secara manual dengan mengekstrak file .rar dari [link berikut](hh). <br>
Anda juga bisa langsung clone repository ini menggunakan git bash: <br>
```
cd {file lokasi}
git init
git clone https://github.com/muhammadzaini213/Admin-Ujian-Kita.git
```
## Upload File Excel Ke Google Spreadsheet
Anda dapat menemukan file template excel dalam folder 'templates'. Ubah nama dari file jika diperlukan.  <br>
Setelah upload selesai, anda perlu mengupload excel ke dalam google spreadsheet anda masing masing serta menyalakan 'dapat dibaca oleh semua orang yang memiliki link'
    
## Masuk Dalam Website Admin
Website admin dapat dibuka melalui [link publik](admin-iota-brown.vercel.app) maupun dengan membuka file ```index.html``` yang dapat ditemukan dalam folder yang anda download.

## Login Atau Daftar
Jika anda baru pertama kali menggunakan aplikasi ini, ketuk ```Buat akun baru``` pada website admin. Masukkan email dan password yang ingin anda daftarkan. Setelah itu email akan dikirim agar anda dapat memverifikasi email anda. <br>
PERINGATAN! UNTUK KEAMANAN DISARANKAN UNTUK MENGGUNAKAN EMAIL YANG TIDAK TERDAFTAR DENGAN AKUN PENTING! <br>
Setelah email terverifikasi, anda dapat login.

## Mempersiapkan Database
Setelah anda berhasil login. Ketuk menu 'Pengaturan' di kanan layar, anda akan dihadapkan pada 'Database Ujian'. <br>
Salin link google spreadsheet anda, jangan sampat tertukar:
```
Template Murid -> Murid
Template Ujian -> Exam
Template Sekolah -> Sekolah
```
Setelah itu ketuk tombol 'Simpan' dan tunggu hingga aplikasi berhasil menyimpan data.

## Mengatur Database Sekolah
Buka excel sekolah anda yang telah di upload dalam google spreadsheet tadi, anda bisa lakukan dengan mengetuk 'Sekolah' pada website admin, kemudian edit. <br>
Berikut beberapa hal yang harus diingat saat mengatur excel sekolah:
```
1. Kolom pertama yang berisi 'X' dan 'DATA:' tidak perlu diubah.
2. Di kolom kedua dan ketiga terdapat 'LOGO SEKOLAH' dan 'NAMA SEKOLAH', untuk logo sekolah, anda harus menempelkan url logo sekolah anda disana, sementara untuk nama sekolah, cukup ditulis biasa saja.
3. Pada kolom keempat, terdapat "BLOKIR APLIKASI", anda dapat memasukkan list aplikasi apa saja yang tidak boleh diinstall oleh murid selama ujian. Utamakan aplikasi yang dapat digunakan mencontek oleh murid. Untuk menggunakannya, anda harus memasukkan nama package aplikasi yang ingin diblokir dan masing masing dipisahkan oleh koma. Contoh: com.aplikasi.menyontek,com.floating.app
4. Kolom kelima adalah versi aplikasi yang harus digunakan oleh murid saat ujian, ini digunakan untuk memaksa murid menginstall versi aplikasi yang sudah ditentukan jikalau ada masalah keamanan pada aplikasi 'Ujian Online'.

Pastikan data sudah tersimpan di google spreadsheet sebelum meninggalkan website.
```
