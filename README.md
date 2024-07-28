## Pengenalan Aplikasi Admin Ujian Kita
Aplikasi ini adalah aplikasi berbasis web yang bertindak sebagai database aplikasi "Ujian Kita" dan dapat digunakan secara gratis untuk sekarang.<br>
Berikut adalah cara menggunakan aplikasi ini:

## Step 1) Download Semua Template excel dan Web
Download dapat dilakukan secara manual dengan mengekstrak file .rar dari [link berikut](https://github.com/muhammadzaini213/Admin-Ujian-Kita/archive/refs/heads/main.zip). <br>
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

2. Di kolom kedua dan ketiga terdapat 'LOGO SEKOLAH' dan 'NAMA SEKOLAH', untuk logo sekolah,
   anda harus menempelkan url logo sekolah anda disana, sementara untuk nama sekolah, cukup ditulis biasa saja.

3. Pada kolom keempat, terdapat "BLOKIR APLIKASI", anda dapat memasukkan list aplikasi apa saja
   yang tidak boleh diinstall oleh murid selama ujian. Utamakan aplikasi yang dapat digunakan
   mencontek oleh murid. Untuk menggunakannya, anda harus memasukkan nama package aplikasi
   yang ingin diblokir dan masing masing dipisahkan oleh koma.
   Contoh: com.aplikasi.menyontek,com.floating.app

4. Kolom kelima adalah versi aplikasi yang harus digunakan oleh murid saat ujian, ini digunakan
   untuk memaksa murid menginstall versi aplikasi yang sudah ditentukan jikalau ada masalah
   keamanan pada aplikasi 'Ujian Online'.
```
Pastikan data sudah tersimpan di google spreadsheet sebelum meninggalkan file spreadsheet.

## Database Murid
Database murid dapat dibuka dengan mengetuk menu 'Murid' pada web admin maupun membukanya langsung menggunakan link yang anda salik tadi. <br>
Berikut cara untuk mengatur database murid:<br>
```
1. Nama, Kelas, maupun Status harus tetap diisi dengan benar.
2. Username dan password adalah hal paling penting disini karena diperlukan
   murid untuk login di aplikasi 'Ujian Kita', jangan pernah membuat username yang sama.
```
Setelah database murid selesai, pastikan data tersimpan dan tinggalkan file spreadsheet.

## Database Ujian
Anda dapat membuka database ujian melalui menu "Ujian" di web admin maupun membukanya melalui url spreadsheet anda. <br>
Berikut adalah cara untuk membuat Ujian: <br>
```
1. NAMA TEST dan KELAS tidak memiliki aturan yang pasti. Meskipun begitu,
   anda harus tetap menuliskan ini di tiap baris spreadsheet.

2. TANGGAL ditulis dengan format hari(2 angka)-bulan(2 angka)-tahun(4 angka).
   Contoh: 01-01-2001 (untuk 1 Januari 2001).

3. WAKTU ditulis menggunakan format jam(2 angka)-menit(2 angka).
   Contoh: 08:00 (untuk pukul 8 tepat).

4. DURASI ditulis menggunakan angka dan dihutung per menit,
   Contoh: 60 -> 60 menit atau 1 jam.

5. LOGO diisi dengan url gambar, anda bisa menggunakan URL logo sekolah
   jika anda tidak ingin mengisi ini.

6. URL adalah Url/Link dari google form yang ingin anda gunakan.

7. STATUS harus diisi dengan AKTIF jika ingin mengaktifkan ujian dan tidak
   perlu diisi jika tidak ingin ujian ditampilkan sekarang.

8. KODE MASUK/KODE RESET adalah kode yang harus digunakan murid untuk masuk kembali,
   kode ini harus dirahasiakan agar murid tidak semudah itu keluar masuk aplikasi untuk
   menyontek. KODE MASUK hanya memperbolehkan murid masuk kembali, sementara KODE RESET
   akan mereset semua pelanggaran yang dilakukan oleh murid.

9. Murid tidak akan bisa masuk ke dalam ujian jika belum masuk waktu ujian.

10. Untuk menambah ujian baru, anda cukup membuat bari baru dibawah ujian yang ada sekarang.

11. Jangan lupa untuk mengetes ujian sebelum menyuruh murid mengerjakannya agar
    tidak ada gangguan saat ujian.
```

## Sekian
Aplikasi android 'Ujian Kita' dapat di ditemukan di [repositori](https://github.com/muhammadzaini213/Ujian_Kita).<br>

### TERIMAKASIH SUDAH BERKUNJUNG!!!
