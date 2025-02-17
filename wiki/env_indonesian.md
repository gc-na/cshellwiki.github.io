# [Linux] Bash env Penggunaan: Mengelola Variabel Lingkungan

## Overview
Perintah `env` digunakan untuk menampilkan atau mengatur variabel lingkungan dalam sistem operasi berbasis Unix. Ini memungkinkan pengguna untuk menjalankan program dalam lingkungan yang ditentukan, serta melihat variabel yang sedang aktif.

## Usage
Berikut adalah sintaks dasar dari perintah `env`:

```bash
env [options] [arguments]
```

## Common Options
- `-i`: Menjalankan perintah dalam lingkungan kosong, tanpa variabel lingkungan yang ada.
- `-u`: Menghapus variabel lingkungan yang ditentukan sebelum menjalankan perintah.
- `VAR=value`: Menetapkan variabel lingkungan baru untuk perintah yang akan dijalankan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `env`:

1. **Menampilkan semua variabel lingkungan:**
   ```bash
   env
   ```

2. **Menjalankan perintah dengan lingkungan kosong:**
   ```bash
   env -i bash
   ```

3. **Menghapus variabel lingkungan tertentu:**
   ```bash
   env -u USER bash
   ```

4. **Menetapkan variabel lingkungan baru saat menjalankan perintah:**
   ```bash
   env MY_VAR=hello bash -c 'echo $MY_VAR'
   ```

5. **Menjalankan skrip dengan variabel lingkungan yang ditentukan:**
   ```bash
   env PATH=/usr/local/bin:$PATH ./myscript.sh
   ```

## Tips
- Gunakan `env` untuk menghindari konflik variabel lingkungan saat menjalankan skrip atau aplikasi.
- Memanfaatkan opsi `-i` sangat berguna untuk debugging, karena Anda dapat melihat bagaimana program berfungsi tanpa variabel lingkungan yang ada.
- Selalu periksa variabel lingkungan yang aktif dengan `env` sebelum menjalankan perintah yang sensitif terhadap lingkungan.