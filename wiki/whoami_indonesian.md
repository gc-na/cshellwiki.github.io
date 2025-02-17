# [Linux] Bash whoami Penggunaan: Menampilkan nama pengguna saat ini

## Overview
Perintah `whoami` digunakan dalam Bash untuk menampilkan nama pengguna yang sedang aktif di terminal. Ini berguna untuk mengetahui identitas pengguna saat ini, terutama ketika bekerja dengan beberapa akun atau saat menggunakan skrip.

## Usage
Berikut adalah sintaks dasar dari perintah `whoami`:

```bash
whoami [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `whoami`:

- `--help`: Menampilkan informasi bantuan tentang penggunaan perintah.
- `--version`: Menampilkan versi dari perintah `whoami`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `whoami`:

1. **Menampilkan nama pengguna saat ini:**
   ```bash
   whoami
   ```

2. **Menampilkan informasi bantuan:**
   ```bash
   whoami --help
   ```

3. **Menampilkan versi perintah:**
   ```bash
   whoami --version
   ```

## Tips
- Gunakan `whoami` untuk memverifikasi identitas pengguna sebelum menjalankan perintah yang memerlukan hak akses tertentu.
- Perintah ini sangat berguna dalam skrip untuk memastikan bahwa skrip dijalankan oleh pengguna yang tepat.
- Kombinasikan `whoami` dengan perintah lain menggunakan subshell untuk mendapatkan informasi lebih lanjut, seperti:
  ```bash
  echo "Pengguna saat ini adalah: $(whoami)"
  ```