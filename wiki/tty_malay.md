# [Linux] Bash tty Penggunaan: Menunjukkan nama terminal

## Overview
Perintah `tty` dalam Bash digunakan untuk menunjukkan nama terminal yang sedang digunakan oleh pengguna. Ia memberikan maklumat tentang peranti terminal yang sedang aktif, yang berguna dalam pelbagai situasi, terutamanya ketika bekerja dengan skrip atau dalam sesi terminal yang berbeza.

## Usage
Berikut adalah sintaks asas untuk perintah `tty`:

```bash
tty [options]
```

## Common Options
- `-s`: Menghasilkan output yang ringkas. Jika terminal sedang aktif, tiada output akan dipaparkan, tetapi kod keluar akan menunjukkan kejayaan.
- `--help`: Menunjukkan bantuan ringkas tentang penggunaan perintah `tty`.
- `--version`: Menunjukkan versi perintah `tty`.

## Common Examples

1. **Menunjukkan nama terminal aktif:**
   ```bash
   tty
   ```
   Output mungkin seperti `/dev/pts/0`, menunjukkan terminal yang sedang digunakan.

2. **Menggunakan pilihan ringkas:**
   ```bash
   tty -s
   ```
   Tiada output jika terminal aktif, tetapi kod keluar boleh diperiksa menggunakan `echo $?`.

3. **Menunjukkan bantuan:**
   ```bash
   tty --help
   ```
   Ini akan memaparkan maklumat tentang cara menggunakan perintah `tty`.

4. **Menunjukkan versi:**
   ```bash
   tty --version
   ```
   Ini akan memberikan maklumat tentang versi perintah `tty` yang sedang digunakan.

## Tips
- Gunakan `tty` dalam skrip untuk memastikan anda tahu terminal mana yang digunakan, terutamanya jika anda menjalankan perintah yang memerlukan interaksi pengguna.
- Jika anda menggunakan sesi SSH, `tty` boleh membantu anda mengenal pasti terminal jarak jauh yang sedang digunakan.
- Sentiasa gunakan pilihan `-s` jika anda hanya memerlukan maklumat kejayaan tanpa output tambahan.