# [Linux] Bash sha256sum Penggunaan: Mengira checksum SHA-256

## Overview
Perintah `sha256sum` digunakan untuk mengira dan memaparkan checksum SHA-256 bagi fail. Ini berguna untuk memastikan integriti fail dengan membandingkan checksum yang dihasilkan dengan checksum yang diketahui.

## Usage
Sintaks asas untuk perintah `sha256sum` adalah seperti berikut:

```bash
sha256sum [options] [arguments]
```

## Common Options
- `-b`: Baca fail dalam mod binari.
- `-c`: Semak checksum daripada fail yang diberikan.
- `-o`: Simpan output ke dalam fail yang ditentukan.
- `--quiet`: Jangan cetak nama fail semasa menyemak checksum.

## Common Examples

1. **Mengira checksum untuk satu fail:**
   ```bash
   sha256sum nama_fail.txt
   ```

2. **Mengira checksum untuk beberapa fail:**
   ```bash
   sha256sum fail1.txt fail2.txt
   ```

3. **Menyemak checksum daripada fail:**
   ```bash
   sha256sum -c checksum.txt
   ```

4. **Menyimpan output ke dalam fail:**
   ```bash
   sha256sum nama_fail.txt -o output.txt
   ```

## Tips
- Sentiasa simpan checksum yang dihasilkan untuk rujukan masa depan, terutamanya untuk fail penting.
- Gunakan pilihan `-c` untuk menyemak integriti fail secara berkumpulan dengan mudah.
- Pastikan anda menggunakan mod binari (`-b`) jika anda bekerja dengan fail binari untuk hasil yang tepat.