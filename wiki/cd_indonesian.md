# [Linux] Bash cd Penggunaan: Navigasi direktori

## Overview
Perintah `cd` (change directory) digunakan untuk berpindah antara direktori di sistem file. Dengan menggunakan `cd`, pengguna dapat mengakses folder yang berbeda untuk menjalankan perintah atau mengelola file.

## Usage
Berikut adalah sintaks dasar dari perintah `cd`:

```bash
cd [options] [arguments]
```

## Common Options
- `..` : Pindah ke direktori induk (parent directory).
- `-` : Kembali ke direktori sebelumnya.
- `~` : Pindah ke direktori home pengguna saat ini.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `cd`:

1. **Pindah ke direktori induk:**
   ```bash
   cd ..
   ```

2. **Pindah ke direktori home:**
   ```bash
   cd ~
   ```

3. **Pindah ke direktori tertentu:**
   ```bash
   cd /path/to/directory
   ```

4. **Kembali ke direktori sebelumnya:**
   ```bash
   cd -
   ```

5. **Pindah ke subdirektori:**
   ```bash
   cd Documents
   ```

## Tips
- Gunakan `cd -` untuk dengan cepat kembali ke direktori yang baru saja Anda tinggalkan.
- Anda dapat menggunakan tab untuk menyelesaikan nama direktori secara otomatis, yang dapat menghemat waktu dan mengurangi kesalahan pengetikan.
- Selalu periksa lokasi Anda saat ini dengan perintah `pwd` (print working directory) setelah berpindah direktori untuk memastikan Anda berada di tempat yang diinginkan.