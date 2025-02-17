# [Linux] Bash rsync Penggunaan: Menyalin dan menyinkronkan file

## Overview
Perintah `rsync` adalah alat yang sangat berguna untuk menyalin dan menyinkronkan file dan direktori antara lokasi yang berbeda, baik secara lokal maupun melalui jaringan. Dengan `rsync`, Anda dapat menghemat bandwidth dengan hanya mentransfer bagian file yang telah berubah.

## Usage
Berikut adalah sintaks dasar dari perintah `rsync`:

```
rsync [options] [source] [destination]
```

## Common Options
Berikut adalah beberapa opsi umum yang digunakan dengan `rsync`:

- `-a`: Mode arsip; menyalin file dan direktori secara rekursif dan mempertahankan atribut file.
- `-v`: Menampilkan informasi proses secara rinci (verbose).
- `-z`: Mengompresi data saat mentransfer untuk menghemat bandwidth.
- `-r`: Menyalin direktori secara rekursif.
- `--delete`: Menghapus file di tujuan yang tidak ada di sumber.

## Common Examples
Berikut adalah beberapa contoh penggunaan `rsync`:

1. Menyalin file dari direktori lokal ke direktori lokal lain:
   ```bash
   rsync -av /path/to/source/ /path/to/destination/
   ```

2. Menyalin file dari direktori lokal ke server jarak jauh:
   ```bash
   rsync -av /path/to/local/file user@remote_host:/path/to/remote/destination/
   ```

3. Menyalin direktori secara rekursif dan mengompresi data:
   ```bash
   rsync -az /path/to/local/directory/ user@remote_host:/path/to/remote/directory/
   ```

4. Menyalin file sambil menghapus file yang tidak ada di sumber:
   ```bash
   rsync -av --delete /path/to/source/ /path/to/destination/
   ```

## Tips
- Selalu gunakan opsi `-n` (dry run) untuk melihat apa yang akan dilakukan `rsync` sebelum menjalankan perintah sesungguhnya.
- Pastikan untuk menambahkan garis miring (`/`) di akhir direktori sumber jika Anda ingin menyalin isi direktori tersebut, bukan direktori itu sendiri.
- Gunakan `--progress` untuk melihat kemajuan transfer file saat proses berlangsung.