# [Linux] Bash md5sum Penggunaan: Mengira checksum MD5

## Overview
Perintah `md5sum` digunakan untuk mengira dan memaparkan checksum MD5 bagi fail. Ini berguna untuk memastikan integriti data dengan membandingkan checksum fail yang telah disimpan dengan checksum fail yang baru dihasilkan.

## Usage
Sintaks asas bagi perintah `md5sum` adalah seperti berikut:

```bash
md5sum [options] [arguments]
```

## Common Options
- `-b` : Mengira checksum untuk fail binari.
- `-c` : Menggunakan fail yang mengandungi checksum untuk mengesahkan fail.
- `-t` : Mengira checksum untuk input dari stdin.
- `--help` : Memaparkan maklumat bantuan tentang penggunaan perintah.

## Common Examples
1. Mengira checksum MD5 bagi satu fail:
   ```bash
   md5sum fail.txt
   ```

2. Mengira checksum MD5 bagi beberapa fail:
   ```bash
   md5sum fail1.txt fail2.txt
   ```

3. Menggunakan fail checksum untuk mengesahkan fail:
   ```bash
   md5sum -c checksum.md5
   ```

4. Mengira checksum untuk input dari stdin:
   ```bash
   echo "Hello, World!" | md5sum
   ```

## Tips
- Sentiasa simpan fail checksum bersama dengan fail asal untuk memudahkan pengesahan di masa hadapan.
- Gunakan pilihan `-b` untuk fail binari bagi mendapatkan hasil yang tepat.
- Pastikan anda menggunakan `md5sum` pada fail yang tidak diubah untuk memastikan integriti data.