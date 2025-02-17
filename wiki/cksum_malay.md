# [Linux] Bash cksum: Mengira checksum fail

## Overview
Perintah `cksum` digunakan untuk mengira dan memaparkan nilai checksum (nilai pengesahan) bagi fail. Nilai ini berguna untuk mengesahkan integriti fail dengan membandingkan checksum sebelum dan selepas pemindahan atau penyimpanan.

## Usage
Sintaks asas untuk menggunakan perintah `cksum` adalah seperti berikut:

```
cksum [options] [arguments]
```

## Common Options
- `-a, --algorithm=ALGO` : Menentukan algoritma checksum yang ingin digunakan.
- `-h, --help` : Memaparkan maklumat bantuan mengenai penggunaan perintah ini.
- `-V, --version` : Memaparkan versi perintah `cksum`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `cksum`:

1. Mengira checksum bagi satu fail:
   ```bash
   cksum nama_fail.txt
   ```

2. Mengira checksum bagi beberapa fail sekaligus:
   ```bash
   cksum fail1.txt fail2.txt
   ```

3. Menggunakan pilihan untuk memaparkan versi:
   ```bash
   cksum --version
   ```

4. Menggunakan pilihan bantuan untuk mendapatkan maklumat lanjut:
   ```bash
   cksum --help
   ```

## Tips
- Sentiasa simpan nilai checksum yang dihasilkan untuk rujukan masa depan, terutamanya sebelum memindahkan fail.
- Gunakan `cksum` bersama dengan perintah lain seperti `tar` untuk mengesahkan integriti arkib.
- Pastikan anda menggunakan fail yang tidak diubahsuai untuk mendapatkan checksum yang tepat.