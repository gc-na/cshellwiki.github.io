# [Linux] Bash clear Penggunaan: Menghapus layar terminal

## Overview
Perintah `clear` digunakan untuk menghapus konten yang ditampilkan di layar terminal. Dengan menjalankan perintah ini, Anda dapat membersihkan tampilan terminal sehingga hanya menampilkan prompt yang bersih, membuatnya lebih mudah untuk melihat output baru.

## Usage
Berikut adalah sintaks dasar dari perintah `clear`:

```bash
clear [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `clear`:

- `-x` : Menghapus layar dan juga menghapus scrollback buffer, sehingga tidak ada output sebelumnya yang dapat diakses dengan scroll.
- `--help` : Menampilkan informasi bantuan tentang penggunaan perintah `clear`.
- `--version` : Menampilkan versi dari perintah `clear`.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `clear`:

1. **Menghapus layar terminal:**
   ```bash
   clear
   ```

2. **Menghapus layar dan scrollback buffer:**
   ```bash
   clear -x
   ```

3. **Menampilkan bantuan untuk perintah clear:**
   ```bash
   clear --help
   ```

4. **Menampilkan versi dari perintah clear:**
   ```bash
   clear --version
   ```

## Tips
- Gunakan `clear` secara teratur saat bekerja di terminal untuk menjaga tampilan tetap rapi dan terorganisir.
- Anda dapat menggabungkan `clear` dengan perintah lain dalam skrip untuk membersihkan layar sebelum menampilkan output baru.
- Jika Anda menggunakan terminal yang mendukung pintasan keyboard, Anda juga dapat menggunakan `Ctrl + L` untuk mencapai efek yang sama dengan perintah `clear`.