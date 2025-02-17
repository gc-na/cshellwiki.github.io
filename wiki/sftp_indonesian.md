# [Linux] Bash sftp Penggunaan: Transfer file secara aman

## Overview
Perintah `sftp` (SSH File Transfer Protocol) digunakan untuk mentransfer file secara aman antara komputer lokal dan server jarak jauh. Dengan menggunakan protokol SSH, `sftp` menyediakan cara yang aman untuk meng-upload dan mengunduh file.

## Usage
Berikut adalah sintaks dasar dari perintah `sftp`:

```bash
sftp [options] [user@]host
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `sftp`:

- `-P` : Menentukan port yang digunakan untuk koneksi.
- `-o` : Mengatur opsi SSH, seperti `-o StrictHostKeyChecking=no`.
- `-b` : Menjalankan perintah dari file batch.
- `-r` : Mengizinkan pengunduhan dan pengunggahan direktori secara rekursif.

## Common Examples

### Menghubungkan ke server SFTP
Untuk menghubungkan ke server SFTP, gunakan perintah berikut:

```bash
sftp user@hostname
```

### Mengunduh file dari server
Untuk mengunduh file dari server SFTP, gunakan perintah:

```bash
get namafile.txt
```

### Mengunggah file ke server
Untuk mengunggah file ke server SFTP, gunakan perintah:

```bash
put namafile.txt
```

### Mengunduh direktori secara rekursif
Untuk mengunduh seluruh direktori dari server, gunakan opsi `-r`:

```bash
get -r namadirektori
```

### Mengunggah direktori secara rekursif
Untuk mengunggah seluruh direktori ke server, gunakan:

```bash
put -r namadirektori
```

## Tips
- Selalu pastikan Anda terhubung ke server yang aman dengan memverifikasi kunci host.
- Gunakan opsi `-b` untuk menjalankan perintah SFTP secara otomatis dari file skrip.
- Manfaatkan opsi `-P` jika server SFTP Anda menggunakan port yang berbeda dari port default (22).
- Untuk keamanan tambahan, pertimbangkan untuk menggunakan kunci SSH daripada kata sandi saat menghubungkan ke server.