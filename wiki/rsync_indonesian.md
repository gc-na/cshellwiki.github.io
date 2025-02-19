# [Sistem Operasi] C Shell (csh) rsync: Menyalin dan menyinkronkan file

## Overview
Perintah `rsync` digunakan untuk menyalin dan menyinkronkan file atau direktori antara dua lokasi, baik di dalam sistem yang sama maupun antara sistem yang berbeda. `rsync` sangat efisien karena hanya mentransfer bagian file yang telah berubah, sehingga menghemat bandwidth dan waktu.

## Usage
Berikut adalah sintaks dasar dari perintah `rsync`:

```csh
rsync [options] [arguments]
```

## Common Options
Beberapa opsi umum yang dapat digunakan dengan `rsync` meliputi:

- `-a`: Menyalin file dalam mode arsip, yang mencakup semua atribut file.
- `-v`: Menampilkan informasi lebih detail selama proses transfer.
- `-z`: Mengompresi data saat mentransfer untuk menghemat bandwidth.
- `-r`: Menyalin direktori secara rekursif.
- `--delete`: Menghapus file di tujuan yang tidak ada di sumber.

## Common Examples
Berikut adalah beberapa contoh penggunaan `rsync`:

1. Menyalin file dari direktori lokal ke direktori tujuan:
   ```csh
   rsync -av /path/to/source/ /path/to/destination/
   ```

2. Menyalin file dari server jarak jauh ke lokal:
   ```csh
   rsync -av user@remote_host:/path/to/remote/source/ /path/to/local/destination/
   ```

3. Menyalin file sambil mengompresi data:
   ```csh
   rsync -avz /path/to/source/ /path/to/destination/
   ```

4. Menyinkronkan direktori dan menghapus file yang tidak ada di sumber:
   ```csh
   rsync -av --delete /path/to/source/ /path/to/destination/
   ```

## Tips
- Selalu gunakan opsi `-n` (dry run) untuk melihat apa yang akan dilakukan `rsync` sebelum benar-benar menjalankannya.
- Pastikan untuk menambahkan trailing slash (`/`) pada direktori sumber jika ingin menyalin isi direktori, bukan direktori itu sendiri.
- Gunakan opsi `-h` untuk menampilkan ukuran file dalam format yang lebih mudah dibaca.