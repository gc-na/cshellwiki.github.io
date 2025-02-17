# [Linux] Bash sha512sum Penggunaan: Mengira checksum SHA-512

## Overview
Perintah `sha512sum` digunakan untuk mengira dan memaparkan checksum SHA-512 bagi fail. Ia berguna untuk memastikan integriti data dengan membandingkan checksum yang dihasilkan dengan checksum yang diketahui.

## Usage
Sintaks asas untuk perintah ini adalah seperti berikut:

```bash
sha512sum [options] [arguments]
```

## Common Options
- `-b` : Mengira checksum untuk fail binari.
- `-c` : Memeriksa checksum berdasarkan fail yang disediakan.
- `-h` : Memaparkan maklumat bantuan tentang perintah ini.
- `--tag` : Menghasilkan output dalam format yang boleh dibaca oleh manusia.

## Common Examples
Berikut adalah beberapa contoh penggunaan `sha512sum`:

1. Mengira checksum bagi fail:
   ```bash
   sha512sum fail.txt
   ```

2. Menyimpan checksum ke dalam fail:
   ```bash
   sha512sum fail.txt > checksum.txt
   ```

3. Memeriksa checksum menggunakan fail yang telah disimpan:
   ```bash
   sha512sum -c checksum.txt
   ```

4. Mengira checksum untuk fail binari:
   ```bash
   sha512sum -b fail.bin
   ```

5. Menghasilkan output dalam format tag:
   ```bash
   sha512sum --tag fail.txt
   ```

## Tips
- Sentiasa simpan checksum yang dihasilkan untuk fail penting agar anda boleh memeriksa integritinya di masa hadapan.
- Gunakan pilihan `-c` untuk memeriksa checksum secara berkumpulan dengan mudah.
- Pastikan anda menggunakan `sha512sum` pada fail yang tidak diubahsuai untuk mendapatkan hasil yang tepat.