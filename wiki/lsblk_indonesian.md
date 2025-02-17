# [Linux] Bash lsblk Penggunaan: Menampilkan informasi blok perangkat

## Overview
Perintah `lsblk` digunakan untuk menampilkan informasi tentang perangkat blok di sistem Linux. Ini termasuk disk, partisi, dan perangkat penyimpanan lainnya. Dengan `lsblk`, pengguna dapat dengan mudah melihat struktur penyimpanan dan ukuran perangkat yang terpasang.

## Usage
Berikut adalah sintaks dasar dari perintah `lsblk`:

```bash
lsblk [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `lsblk`:

- `-a` atau `--all`: Menampilkan semua perangkat, termasuk yang tidak terpasang.
- `-f` atau `--fs`: Menampilkan informasi sistem file pada perangkat.
- `-l` atau `--list`: Menampilkan output dalam format daftar.
- `-o` atau `--output`: Menentukan kolom mana yang akan ditampilkan.
- `-p` atau `--paths`: Menampilkan jalur perangkat lengkap.

## Common Examples
Berikut adalah beberapa contoh penggunaan `lsblk`:

1. Menampilkan semua perangkat blok yang terpasang:
   ```bash
   lsblk
   ```

2. Menampilkan semua perangkat termasuk yang tidak terpasang:
   ```bash
   lsblk -a
   ```

3. Menampilkan informasi sistem file pada perangkat:
   ```bash
   lsblk -f
   ```

4. Menampilkan output dalam format daftar:
   ```bash
   lsblk -l
   ```

5. Menentukan kolom yang ditampilkan, misalnya hanya nama dan ukuran:
   ```bash
   lsblk -o NAME,SIZE
   ```

## Tips
- Gunakan opsi `-f` untuk mendapatkan informasi lebih lanjut tentang sistem file, seperti tipe dan label.
- Kombinasikan `lsblk` dengan perintah lain seperti `grep` untuk mencari perangkat tertentu.
- Periksa secara berkala perangkat blok Anda untuk memastikan tidak ada masalah dengan penyimpanan yang terpasang.