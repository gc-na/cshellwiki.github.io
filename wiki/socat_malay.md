# [Linux] Bash socat Penggunaan: Alat untuk pemindahan data antara aliran

## Overview
`socat` adalah alat baris perintah yang digunakan untuk menghubungkan dua aliran data. Ia membolehkan pengguna untuk membuat sambungan antara pelbagai jenis soket, fail, dan peranti, menjadikannya berguna untuk pemindahan data dan pengujian rangkaian.

## Usage
Berikut adalah sintaks asas untuk menggunakan `socat`:

```
socat [options] [arguments]
```

## Common Options
- `-u`: Menggunakan mod tidak terikat (unidirectional).
- `-v`: Mengaktifkan mod verbose untuk output yang lebih terperinci.
- `TCP4`: Menggunakan protokol TCP versi 4.
- `UDP`: Menggunakan protokol UDP.
- `FILE`: Menghubungkan ke fail.

## Common Examples
Berikut adalah beberapa contoh penggunaan `socat`:

1. **Menghubungkan dua port TCP:**
   ```bash
   socat TCP4-LISTEN:1234,fork TCP4:localhost:5678
   ```

2. **Menghantar data dari fail ke soket:**
   ```bash
   socat -u FILE:/path/to/file TCP4:localhost:1234
   ```

3. **Menerima data dari soket dan menyimpannya ke dalam fail:**
   ```bash
   socat TCP4-LISTEN:1234,fork FILE:/path/to/output/file
   ```

4. **Menggunakan UDP untuk menghantar mesej:**
   ```bash
   echo "Hello, World!" | socat - UDP:localhost:1234
   ```

## Tips
- Sentiasa gunakan pilihan `-v` untuk mendapatkan maklumat tambahan semasa pemindahan data, ini membantu dalam penyelesaian masalah.
- Pastikan port yang digunakan tidak dibuka oleh aplikasi lain untuk mengelakkan konflik.
- Gunakan `fork` untuk membenarkan sambungan pelbagai klien secara serentak.