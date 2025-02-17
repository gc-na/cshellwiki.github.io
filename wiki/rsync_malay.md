# [Linux] Bash rsync Penggunaan: Menyalin dan menyegerakkan fail

## Overview
Perintah `rsync` adalah alat yang sangat berguna dalam sistem Linux untuk menyalin dan menyegerakkan fail dan direktori antara lokasi yang berbeza. Ia berfungsi dengan cara yang efisien dengan hanya memindahkan perubahan yang dibuat, menjadikannya lebih cepat dan menjimatkan ruang penyimpanan.

## Usage
Sintaks asas untuk menggunakan perintah `rsync` adalah seperti berikut:

```bash
rsync [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum yang boleh digunakan dengan `rsync`:

- `-a`: Mengaktifkan mod arkib, yang menyalin fail dan direktori secara rekursif dan mengekalkan atribut fail.
- `-v`: Menunjukkan output yang lebih terperinci semasa proses pemindahan.
- `-z`: Mengaktifkan pemampatan data semasa pemindahan, menjadikannya lebih cepat untuk fail besar.
- `--delete`: Menghapus fail di destinasi yang tidak ada di sumber.
- `-r`: Menyalin direktori secara rekursif.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `rsync`:

1. Menyalin fail dari satu direktori ke direktori lain:
   ```bash
   rsync -av /path/to/source/ /path/to/destination/
   ```

2. Menyalin fail ke pelayan jauh menggunakan SSH:
   ```bash
   rsync -avz -e ssh /path/to/local/file user@remote_host:/path/to/remote/directory/
   ```

3. Menyegerakkan dua direktori dan menghapus fail yang tidak ada di sumber:
   ```bash
   rsync -av --delete /path/to/source/ /path/to/destination/
   ```

4. Menyalin fail dengan pemampatan:
   ```bash
   rsync -avz /path/to/source/ /path/to/destination/
   ```

## Tips
- Sentiasa gunakan pilihan `-n` (dry run) untuk melihat apa yang akan dilakukan sebelum melaksanakan perintah `rsync`.
- Pastikan untuk menambah garis miring (`/`) di akhir direktori sumber jika anda ingin menyalin isi direktori tersebut, bukan direktori itu sendiri.
- Gunakan pilihan `-h` untuk memaparkan saiz fail dalam format yang lebih mudah dibaca. 

Dengan menggunakan `rsync`, anda dapat mengurus fail dan direktori dengan lebih efisien dan berkesan.