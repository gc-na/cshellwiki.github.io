# [Linux] Bash ftp Penggunaan: Mengelola Transfer File

## Overview
Perintah `ftp` (File Transfer Protocol) digunakan untuk mentransfer file antara komputer melalui jaringan. Dengan `ftp`, pengguna dapat meng-upload, mengunduh, dan mengelola file di server jarak jauh.

## Usage
Berikut adalah sintaks dasar untuk menggunakan perintah `ftp`:

```bash
ftp [options] [arguments]
```

## Common Options
- `-i`: Menonaktifkan mode interaktif, sehingga tidak meminta konfirmasi untuk setiap file yang ditransfer.
- `-n`: Mencegah ftp dari otomatis login ke server.
- `-v`: Menampilkan informasi lebih detail tentang proses transfer.
- `-p`: Menggunakan mode pasif untuk koneksi, berguna saat berada di belakang firewall.

## Common Examples

### Menghubungkan ke Server FTP
Untuk menghubungkan ke server FTP, gunakan perintah berikut:

```bash
ftp ftp.example.com
```

### Meng-upload File
Untuk meng-upload file ke server, setelah terhubung, gunakan perintah:

```bash
put nama_file.txt
```

### Mengunduh File
Untuk mengunduh file dari server, gunakan perintah:

```bash
get nama_file.txt
```

### Menggunakan Mode Interaktif
Jika Anda ingin meng-upload beberapa file tanpa konfirmasi, aktifkan mode non-interaktif:

```bash
ftp -i ftp.example.com
```

### Menampilkan Daftar File
Setelah terhubung, untuk melihat daftar file di direktori saat ini, gunakan:

```bash
ls
```

## Tips
- Selalu pastikan untuk menggunakan koneksi yang aman, seperti SFTP, jika data yang ditransfer bersifat sensitif.
- Gunakan opsi `-v` untuk mendapatkan informasi lebih lanjut jika terjadi kesalahan saat transfer.
- Jika Anda sering terhubung ke server yang sama, pertimbangkan untuk menyimpan kredensial dalam file konfigurasi untuk kemudahan akses.