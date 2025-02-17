# [Linux] Bash wget Penggunaan: Memuat turun fail dari web

## Overview
Perintah `wget` adalah alat baris perintah yang digunakan untuk memuat turun fail dari internet. Ia menyokong pelbagai protokol seperti HTTP, HTTPS, dan FTP, menjadikannya sangat berguna untuk mendapatkan data dari pelbagai sumber dalam talian.

## Usage
Sintaks asas untuk menggunakan `wget` adalah seperti berikut:

```bash
wget [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `wget` beserta penjelasan ringkas:

- `-O [file]`: Menyimpan fail yang dimuat turun dengan nama yang ditentukan.
- `-c`: Melanjutkan muat turun yang terputus.
- `-q`: Menjalankan wget dalam mod senyap (quiet), tanpa output ke konsol.
- `--limit-rate=[rate]`: Menghadkan kelajuan muat turun.
- `-r`: Memuat turun secara rekursif, termasuk semua fail yang berkaitan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `wget`:

1. **Muat turun fail tunggal:**
   ```bash
   wget https://example.com/file.zip
   ```

2. **Menyimpan fail dengan nama berbeza:**
   ```bash
   wget -O myfile.zip https://example.com/file.zip
   ```

3. **Melanjutkan muat turun yang terputus:**
   ```bash
   wget -c https://example.com/largefile.zip
   ```

4. **Muat turun secara rekursif:**
   ```bash
   wget -r https://example.com/directory/
   ```

5. **Menghadkan kelajuan muat turun:**
   ```bash
   wget --limit-rate=100k https://example.com/file.zip
   ```

## Tips
- Sentiasa semak URL sebelum memuat turun untuk memastikan ia sah dan selamat.
- Gunakan pilihan `-q` jika anda ingin menjalankan muat turun dalam latar belakang tanpa output yang mengganggu.
- Untuk muat turun yang besar, pertimbangkan untuk menggunakan pilihan `-c` agar anda boleh menyambung semula jika sambungan terputus.
- Jika anda memuat turun banyak fail, pertimbangkan untuk menggunakan pilihan `-r` dengan bijak untuk mengelakkan memuat turun terlalu banyak data sekaligus.