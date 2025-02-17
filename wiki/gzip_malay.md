# [Linux] Bash gzip Penggunaan: Memampatkan fail

## Overview
Perintah `gzip` digunakan untuk memampatkan fail dalam sistem operasi Linux. Ia mengurangkan saiz fail dengan menggunakan algoritma pemampatan, menjadikannya lebih mudah untuk disimpan dan dihantar.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `gzip`:

```bash
gzip [options] [arguments]
```

## Common Options
- `-d` : Menguraikan fail yang telah dimampatkan.
- `-k` : Menyimpan fail asal selepas pemampatan.
- `-v` : Menunjukkan maklumat terperinci semasa pemampatan.
- `-r` : Memampatkan fail dalam direktori secara rekursif.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `gzip`:

1. **Memampatkan fail**:
   ```bash
   gzip fail.txt
   ```

2. **Menguraikan fail yang telah dimampatkan**:
   ```bash
   gzip -d fail.txt.gz
   ```

3. **Mampatkan fail dan simpan fail asal**:
   ```bash
   gzip -k fail.txt
   ```

4. **Mampatkan semua fail dalam direktori**:
   ```bash
   gzip -r direktori/
   ```

5. **Menunjukkan maklumat pemampatan**:
   ```bash
   gzip -v fail.txt
   ```

## Tips
- Sentiasa semak saiz fail selepas pemampatan untuk memastikan ia berkurang dengan ketara.
- Gunakan pilihan `-k` jika anda ingin mengekalkan fail asal semasa memampatkan.
- Untuk pemampatan yang lebih baik, pertimbangkan untuk menggunakan `gzip` bersama dengan `tar` untuk mengarkibkan dan memampatkan fail secara serentak.