# [Linux] Bash cp Penggunaan: Menyalin Fail dan Direktori

## Overview
Perintah `cp` dalam Bash digunakan untuk menyalin fail dan direktori dari satu lokasi ke lokasi yang lain. Ia adalah alat yang sangat berguna dalam pengurusan fail di sistem operasi Linux.

## Usage
Sintaks asas untuk perintah `cp` adalah seperti berikut:

```bash
cp [options] [source] [destination]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan perintah `cp`:

- `-r`: Menyalin direktori secara rekursif.
- `-i`: Meminta pengesahan sebelum menimpa fail yang sedia ada.
- `-u`: Menyalin hanya fail yang lebih baru daripada fail yang sedia ada di destinasi.
- `-v`: Menunjukkan maklumat tentang fail yang sedang disalin.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `cp`:

1. Menyalin fail dari satu lokasi ke lokasi lain:
   ```bash
   cp fail.txt /home/user/destinasi/
   ```

2. Menyalin direktori secara rekursif:
   ```bash
   cp -r direktori_sumber/ /home/user/destinasi/
   ```

3. Menyalin fail dengan pengesahan sebelum menimpa:
   ```bash
   cp -i fail.txt /home/user/destinasi/
   ```

4. Menyalin hanya fail yang lebih baru:
   ```bash
   cp -u fail.txt /home/user/destinasi/
   ```

5. Menyalin fail dan menunjukkan proses:
   ```bash
   cp -v fail.txt /home/user/destinasi/
   ```

## Tips
- Sentiasa gunakan pilihan `-i` jika anda bimbang tentang menimpa fail yang sedia ada.
- Gunakan pilihan `-r` dengan berhati-hati apabila menyalin direktori untuk memastikan semua fail dan subdirektori disalin.
- Periksa lokasi destinasi sebelum menyalin untuk mengelakkan kekeliruan dalam pengurusan fail.