# [Linux] Bash sha256sum Penggunaan: Menghitung checksum SHA-256

## Overview
Perintah `sha256sum` digunakan untuk menghitung dan memverifikasi checksum SHA-256 dari file. Ini berguna untuk memastikan integritas data dengan membandingkan checksum yang dihasilkan dengan checksum yang diketahui.

## Usage
Berikut adalah sintaks dasar dari perintah `sha256sum`:

```bash
sha256sum [options] [arguments]
```

## Common Options
- `-b`, `--binary`: Menghitung checksum dalam mode biner.
- `-c`, `--check`: Memeriksa checksum dari file yang telah dihitung sebelumnya.
- `-h`, `--help`: Menampilkan bantuan penggunaan perintah.
- `-o`, `--output`: Menentukan file output untuk menyimpan hasil checksum.

## Common Examples
Berikut adalah beberapa contoh penggunaan `sha256sum`:

1. Menghitung checksum dari sebuah file:
   ```bash
   sha256sum file.txt
   ```

2. Menghitung checksum dari beberapa file sekaligus:
   ```bash
   sha256sum file1.txt file2.txt
   ```

3. Menyimpan hasil checksum ke dalam file:
   ```bash
   sha256sum file.txt > checksum.txt
   ```

4. Memeriksa checksum dari file menggunakan file checksum:
   ```bash
   sha256sum -c checksum.txt
   ```

5. Menghitung checksum dalam mode biner:
   ```bash
   sha256sum -b file.bin
   ```

## Tips
- Selalu simpan file checksum di tempat yang aman untuk memudahkan verifikasi di masa mendatang.
- Gunakan opsi `-c` untuk memverifikasi file setelah diunduh atau dipindahkan untuk memastikan tidak ada kerusakan data.
- Untuk file besar, pertimbangkan untuk menghitung checksum di latar belakang dengan menggunakan `&` agar tidak mengganggu pekerjaan lain.