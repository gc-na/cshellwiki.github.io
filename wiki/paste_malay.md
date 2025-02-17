# [Linux] Bash paste Penggunaan: Menggabungkan baris dari fail

## Overview
Perintah `paste` dalam Bash digunakan untuk menggabungkan baris dari satu atau lebih fail. Ia menyusun baris dari fail-fail tersebut secara mendatar, membolehkan pengguna untuk melihat data dari pelbagai sumber dalam satu pandangan.

## Usage
Sintaks asas bagi perintah `paste` adalah seperti berikut:

```bash
paste [options] [arguments]
```

## Common Options
- `-d` : Menentukan pemisah yang ingin digunakan antara baris. Secara lalai, pemisah adalah tab.
- `-s` : Menggabungkan baris secara berturut-turut dalam satu fail, bukan secara mendatar.
- `-z` : Menggunakan null sebagai pemisah antara baris.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `paste`:

1. **Menggabungkan dua fail secara mendatar**:
   ```bash
   paste fail1.txt fail2.txt
   ```

2. **Menggunakan pemisah khusus**:
   ```bash
   paste -d ',' fail1.txt fail2.txt
   ```

3. **Menggabungkan baris secara berturut-turut**:
   ```bash
   paste -s fail1.txt
   ```

4. **Menggunakan null sebagai pemisah**:
   ```bash
   paste -z fail1.txt fail2.txt
   ```

## Tips
- Pastikan fail yang ingin digabungkan mempunyai bilangan baris yang sama untuk hasil yang lebih teratur.
- Gunakan pilihan `-d` untuk menyesuaikan pemisah mengikut keperluan data anda.
- Untuk data yang besar, pertimbangkan untuk menggunakan `paste` bersama dengan alat lain seperti `sort` atau `uniq` untuk analisis yang lebih mendalam.