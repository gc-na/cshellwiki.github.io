# [Linux] Bash echo Penggunaan: Mencetak teks ke terminal

## Overview
Perintah `echo` dalam Bash digunakan untuk mencetak teks atau output ke terminal. Ia sering digunakan dalam skrip untuk memberikan maklumat kepada pengguna atau untuk mengesahkan nilai pembolehubah.

## Usage
Sintaks asas untuk perintah `echo` adalah seperti berikut:

```bash
echo [options] [arguments]
```

## Common Options
- `-n`: Tidak mencetak newline di akhir output.
- `-e`: Mengaktifkan interpretasi karakter khas seperti `\n` (newline) dan `\t` (tab).
- `-E`: Menonaktifkan interpretasi karakter khas (ini adalah pilihan lalai).

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `echo`:

1. Mencetak teks biasa:
   ```bash
   echo "Hello, World!"
   ```

2. Mencetak teks tanpa newline di akhir:
   ```bash
   echo -n "Hello, "
   echo "World!"
   ```

3. Menggunakan karakter khas:
   ```bash
   echo -e "Baris pertama\nBaris kedua"
   ```

4. Mencetak nilai pembolehubah:
   ```bash
   name="Ali"
   echo "Nama saya adalah $name"
   ```

5. Mencetak dengan tab:
   ```bash
   echo -e "Satu\tDua\tTiga"
   ```

## Tips
- Gunakan `-n` jika anda ingin mencetak beberapa baris tanpa ruang kosong di antara mereka.
- Pastikan untuk menggunakan `-e` jika anda ingin menggunakan karakter khas dalam output.
- Untuk mencetak pembolehubah, sentiasa gunakan tanda `$` sebelum nama pembolehubah.