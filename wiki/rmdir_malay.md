# [Linux] Bash rmdir Penggunaan: Memadam direktori kosong

## Overview
Perintah `rmdir` digunakan untuk memadam direktori yang kosong dalam sistem fail. Jika direktori yang ingin dipadam mengandungi fail atau subdirektori, perintah ini tidak akan berjaya dan akan memberikan mesej ralat.

## Usage
Sintaks asas untuk menggunakan perintah `rmdir` adalah seperti berikut:

```bash
rmdir [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan `rmdir`:

- `--ignore-fail-on-non-empty`: Mengabaikan kesalahan jika direktori tidak kosong.
- `--verbose`: Menunjukkan maklumat lanjut tentang tindakan yang dilakukan.
- `--help`: Menunjukkan bantuan tentang penggunaan perintah.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `rmdir`:

1. Memadam direktori kosong:
   ```bash
   rmdir direktori_kosong
   ```

2. Memadam beberapa direktori kosong sekaligus:
   ```bash
   rmdir direktori1 direktori2
   ```

3. Menggunakan pilihan verbose untuk melihat maklumat tambahan:
   ```bash
   rmdir --verbose direktori_kosong
   ```

4. Mengabaikan kesalahan jika direktori tidak kosong:
   ```bash
   rmdir --ignore-fail-on-non-empty direktori_tidak_kosong
   ```

## Tips
- Pastikan direktori yang ingin dipadam benar-benar kosong sebelum menggunakan `rmdir`.
- Gunakan pilihan `--verbose` untuk mendapatkan maklumat tambahan yang berguna semasa proses pemadaman.
- Jika anda ingin memadam direktori yang tidak kosong, pertimbangkan untuk menggunakan perintah `rm -r` sebagai alternatif.